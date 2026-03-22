# GLSL Behavior Snippets

Ready-to-use shader code for glitchcore artifact drivers.

## Purpose

This file provides actual GLSL shader code snippets for implementing glitchcore artifact drivers.

Each snippet includes:
- Vertex shader (if needed)
- Fragment shader
- Uniform declarations
- Parameter explanations
- Usage notes

---

## 1. Channel Split (RGB Displacement)

### Fragment Shader

```glsl
// Channel Split - RGB Displacement
// Separates color channels with offset

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uChannelSplitStrength; // 0.0 - 1.0
uniform float uEdgeBias;             // 0.0 - 1.0 (wider at edges)
uniform vec2 uRedOffset;             // Red channel offset
uniform vec2 uGreenOffset;           // Green channel offset
uniform vec2 uBlueOffset;            // Blue channel offset

vec2 uv = gl_FragCoord.xy / uResolution;

// Calculate distance from center for edge bias
vec2 center = vec2(0.5);
float distFromCenter = distance(uv, center);
float edgeFactor = smoothstep(0.0, 0.7, distFromCenter) * uEdgeBias;

// Apply edge bias to offset strength
float effectiveStrength = uChannelSplitStrength * (0.3 + 0.7 * edgeFactor);

// Sample each channel with offset
vec2 redUV = uv + uRedOffset * effectiveStrength;
vec2 greenUV = uv + uGreenOffset * effectiveStrength;
vec2 blueUV = uv + uBlueOffset * effectiveStrength;

float r = texture2D(uSourceTexture, redUV).r;
float g = texture2D(uSourceTexture, greenUV).g;
float b = texture2D(uSourceTexture, blueUV).b;

gl_FragColor = vec4(r, g, b, 1.0);
```

### Audio-Reactive Version

```glsl
// Add to uniforms:
uniform float uBass; // 0.0 - 1.0

// Modify effective strength:
float effectiveStrength = uChannelSplitStrength * (0.3 + 0.7 * edgeFactor) * (0.5 + 0.5 * uBass);
```

---

## 2. Bloom / Glow

### Fragment Shader

```glsl
// Bloom - Light bleed and glow
// Creates luminous glow around bright areas

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uBloomThreshold;  // 0.0 - 1.0 (brightness threshold)
uniform float uBloomRadius;     // 0.0 - 0.5 (glow spread)
uniform float uBloomIntensity;  // 0.0 - 2.0 (glow brightness)

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample source
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Calculate luminance
float luminance = dot(source, vec3(0.299, 0.587, 0.114));

// Extract bright areas
vec3 bright = source * smoothstep(uBloomThreshold, uBloomThreshold + 0.1, luminance);

// Blur bright areas (simplified box blur)
vec3 bloom = vec3(0.0);
float samples = 0.0;
for(float x = -4.0; x <= 4.0; x += 1.0) {
    for(float y = -4.0; y <= 4.0; y += 1.0) {
        vec2 offset = vec2(x, y) * uBloomRadius / uResolution;
        vec3 sampleColor = texture2D(uSourceTexture, uv + offset).rgb;
        float sampleLuma = dot(sampleColor, vec3(0.299, 0.587, 0.114));
        bloom += sampleColor * smoothstep(uBloomThreshold, uBloomThreshold + 0.1, sampleLuma);
        samples += 1.0;
    }
}
bloom /= samples;

// Combine source with bloom
gl_FragColor = vec4(source + bloom * uBloomIntensity, 1.0);
```

---

## 3. Overprint Stacking

### Fragment Shader

```glsl
// Overprint Stacking - Duplicate layers
// Creates multiple semi-transparent copies

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform int uLayerCount;           // 2 - 10
uniform float uOffsetDistance;     // 0.0 - 0.1
uniform float uOpacityFalloff;     // 0.0 - 1.0
uniform vec2 uOffsetDirection;     // Direction of offset

vec2 uv = gl_FragCoord.xy / uResolution;

vec3 result = texture2D(uSourceTexture, uv).rgb;
float totalWeight = 1.0;

for(int i = 1; i <= 10; i++) {
    if(i >= uLayerCount) break;
    
    float layerOffset = float(i) * uOffsetDistance;
    float layerOpacity = pow(uOpacityFalloff, float(i));
    
    vec2 layerUV = uv + uOffsetDirection * layerOffset;
    vec3 layerColor = texture2D(uSourceTexture, layerUV).rgb;
    
    // Screen blend mode
    result = result + layerColor * layerOpacity * (1.0 - result);
    totalWeight += layerOpacity;
}

gl_FragColor = vec4(result, 1.0);
```

---

## 4. Temporal Echo / Motion Trails

### Fragment Shader (with history buffer)

```glsl
// Temporal Echo - Frame history trails
// Requires history buffer setup in application

uniform sampler2D uCurrentFrame;
uniform sampler2D uHistoryFrame1;
uniform sampler2D uHistoryFrame2;
uniform sampler2D uHistoryFrame3;
uniform vec2 uResolution;
uniform float uEcho1Weight;    // 0.0 - 1.0
uniform float uEcho2Weight;    // 0.0 - 1.0
uniform float uEcho3Weight;    // 0.0 - 1.0

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample current and history
vec3 current = texture2D(uCurrentFrame, uv).rgb;
vec3 echo1 = texture2D(uHistoryFrame1, uv).rgb;
vec3 echo2 = texture2D(uHistoryFrame2, uv).rgb;
vec3 echo3 = texture2D(uHistoryFrame3, uv).rgb;

// Weighted blend (exponential fade)
vec3 result = current;
result = mix(result, echo1, uEcho1Weight * 0.5);
result = mix(result, echo2, uEcho2Weight * 0.3);
result = mix(result, echo3, uEcho3Weight * 0.15);

gl_FragColor = vec4(result, 1.0);
```

---

## 5. Scanline Contour

### Fragment Shader

```glsl
// Scanline Contour - CRT-style banding
// Creates horizontal lines that follow image contours

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uLineSpacing;      // Pixels between lines
uniform float uLineThickness;    // 0.0 - 1.0
uniform float uContourFollowing; // 0.0 - 1.0
uniform vec3 uPhosphorColor;     // CRT phosphor color

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample source
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Calculate edge/gradient for contour following
vec2 texel = 1.0 / uResolution;
vec3 right = texture2D(uSourceTexture, uv + vec2(texel.x, 0.0)).rgb;
vec3 up = texture2D(uSourceTexture, uv + vec2(0.0, texel.y)).rgb;
float edge = length(source - right) + length(source - up);

// Create scanline pattern
float lineIndex = floor(gl_FragCoord.y / uLineSpacing);
float linePos = fract(gl_FragCoord.y / uLineSpacing);
float lineMask = smoothstep(0.0, uLineThickness, linePos) * 
                 smoothstep(1.0, 1.0 - uLineThickness, linePos);

// Modulate by contour
float contourMod = 1.0 - edge * uContourFollowing * 2.0;
lineMask *= contourMod;

// Apply phosphor glow on lines
vec3 lineGlow = uPhosphorColor * lineMask * 2.0;

// Combine
gl_FragColor = vec4(source + lineGlow, 1.0);
```

---

## 6. Compression Artifacts

### Fragment Shader

```glsl
// Compression Chew - Macroblock artifacts
// Simulates digital compression damage

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uBlockSize;        // 4.0 - 32.0
uniform float uQuality;          // 0.0 - 1.0 (lower = worse)
uniform float uChromaBleed;      // 0.0 - 1.0
uniform float uEdgeBuzz;         // 0.0 - 1.0

vec2 uv = gl_FragCoord.xy / uResolution;

// Calculate block coordinates
vec2 blockCoord = floor(gl_FragCoord.xy / uBlockSize) * uBlockSize;
vec2 blockUV = blockCoord / uResolution;

// Sample block center (quantization)
vec3 blockColor = texture2D(uSourceTexture, blockUV + vec2(uBlockSize * 0.5) / uResolution).rgb;

// Sample actual position
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Mix based on quality
vec3 quantized = mix(source, blockColor, 1.0 - uQuality);

// Chroma bleed (color separation)
vec2 texel = 1.0 / uResolution;
vec3 right = texture2D(uSourceTexture, uv + vec2(texel.x * uChromaBleed * 4.0, 0.0)).rgb;
vec3 left = texture2D(uSourceTexture, uv - vec2(texel.x * uChromaBleed * 4.0, 0.0)).rgb;
vec3 chromaBleed = (right + left) * 0.5;
quantized.gb = mix(quantized.gb, chromaBleed.gb, uChromaBleed);

// Edge buzz
float edge = length(source - right) + length(source - left);
float buzz = sin(uv.y * 100.0 + edge * 10.0) * uEdgeBuzz * 0.1;
quantized += buzz;

gl_FragColor = vec4(quantized, 1.0);
```

---

## 7. Noise / Static

### Fragment Shader

```glsl
// Noise Veil - Static and grain
// Adds film/TV static texture

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uNoiseIntensity;   // 0.0 - 1.0
uniform float uNoiseScale;       // 1.0 - 100.0

// Simplex noise function (simplified)
float random(vec2 st) {
    return fract(sin(dot(st.xy, vec2(12.9898, 78.233))) * 43758.5453123);
}

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample source
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Generate noise
vec2 noiseUV = uv * uNoiseScale;
float noise = random(noiseUV + fract(uTime * 0.1));
noise = noise * 2.0 - 1.0; // -1 to 1

// Apply noise
vec3 result = source + vec3(noise) * uNoiseIntensity;

gl_FragColor = vec4(result, 1.0);
```

---

## 8. Sparkle / Glitter

### Fragment Shader

```glsl
// Sparkle Static - Glitter particles
// Adds specular sparkle highlights

uniform sampler2D uSourceTexture;
uniform vec2 uResolution;
uniform float uSparkleDensity;   // 0.0 - 1.0
uniform float uSparkleSize;      // 0.5 - 3.0
uniform float uSparkleBrightness;// 0.5 - 2.0

// Random function
float random(vec2 st) {
    return fract(sin(dot(st.xy, vec2(12.9898, 78.233))) * 43758.5453123);
}

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample source
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Generate sparkle grid
vec2 gridUV = floor(uv * uResolution / uSparkleSize) / (uResolution / uSparkleSize);
float sparkleRandom = random(gridUV + floor(uTime * 10.0));

// Threshold for sparkle
float sparkleThreshold = 1.0 - uSparkleDensity * 0.1;
float sparkle = sparkleRandom > sparkleThreshold ? 1.0 : 0.0;

// Distance from sparkle center
vec2 sparkleCenter = gridUV + vec2(0.5) / (uResolution / uSparkleSize);
float dist = distance(uv, sparkleCenter);
float sparkleFalloff = smoothstep(uSparkleSize / uResolution.x, 0.0, dist);

// Apply sparkle
vec3 sparkleColor = vec3(1.0) * sparkle * sparkleFalloff * uSparkleBrightness;
vec3 result = source + sparkleColor;

gl_FragColor = vec4(result, 1.0);
```

---

## 9. Text Debris

### Fragment Shader (simplified)

```glsl
// Text Interface Debris - Text fragments
// Requires text texture atlas

uniform sampler2D uSourceTexture;
uniform sampler2D uTextAtlas;
uniform vec2 uResolution;
uniform float uTextDensity;      // 0.0 - 1.0
uniform float uTextOverlap;      // 0.0 - 1.0

// Random function
float random(vec2 st) {
    return fract(sin(dot(st.xy, vec2(12.9898, 78.233))) * 43758.5453123);
}

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample source
vec3 source = texture2D(uSourceTexture, uv).rgb;

// Generate text positions
vec2 textGrid = floor(uv * 10.0) / 10.0;
float textRandom = random(textGrid);

// Place text fragments
if(textRandom < uTextDensity * 0.1) {
    vec2 textUV = fract(uv * 10.0);
    vec4 textColor = texture2D(uTextAtlas, textUV);
    
    // Blend text over source
    float blend = textColor.a * uTextOverlap;
    source = mix(source, textColor.rgb, blend);
}

gl_FragColor = vec4(source, 1.0);
```

---

## 10. Full Pass Combiner

### Fragment Shader

```glsl
// Final composite - Combine all passes
// Applies anchor protection

uniform sampler2D uSourcePass;
uniform sampler2D uEffectPass;
uniform sampler2D uAnchorMask;   // Mask for protected zones
uniform vec2 uResolution;
uniform float uAnchorProtection; // 0.0 - 1.0

vec2 uv = gl_FragCoord.xy / uResolution;

// Sample all passes
vec3 source = texture2D(uSourcePass, uv).rgb;
vec3 effect = texture2D(uEffectPass, uv).rgb;
float anchorMask = texture2D(uAnchorMask, uv).r;

// Blend based on anchor protection
float protection = anchorMask * uAnchorProtection;
vec3 result = mix(effect, source, protection);

gl_FragColor = vec4(result, 1.0);
```

---

## 11. Utility Functions

### Common Header

```glsl
// Utility functions for glitchcore shaders

// Random number generation
float random(vec2 st) {
    return fract(sin(dot(st.xy, vec2(12.9898, 78.233))) * 43758.5453123);
}

// Noise function
float noise(vec2 st) {
    vec2 i = floor(st);
    vec2 f = fract(st);
    float a = random(i);
    float b = random(i + vec2(1.0, 0.0));
    float c = random(i + vec2(0.0, 1.0));
    float d = random(i + vec2(1.0, 1.0));
    vec2 u = f * f * (3.0 - 2.0 * f);
    return mix(a, b, u.x) + (c - a) * u.y * (1.0 - u.x) + (d - b) * u.x * u.y;
}

// Luminance calculation
float luminance(vec3 color) {
    return dot(color, vec3(0.299, 0.587, 0.114));
}

// Screen blend mode
vec3 screen(vec3 a, vec3 b) {
    return 1.0 - (1.0 - a) * (1.0 - b);
}

// Overlay blend mode
vec3 overlay(vec3 a, vec3 b) {
    return mix(2.0 * a * b, 1.0 - 2.0 * (1.0 - a) * (1.0 - b), step(0.5, a));
}
```

---

## 12. Summary

GLSL behavior snippets provide:
- Ready-to-use shader code
- Artifact driver implementations
- Audio-reactive modifications
- Utility functions
- Composite techniques

Copy, modify, and combine these snippets to build complete glitchcore shaders.

---

## 13. Short Anchor Rule

Start with working code, then make it yours.
