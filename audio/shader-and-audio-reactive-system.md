# Shader and Audio-Reactive System

How to drive glitchcore effects through shaders and audio-reactive behavior.

## Purpose

This file defines how glitchcore effects should be implemented in shader systems and how they should respond to audio input.

Its job is to bridge:
- The abstract glitchcore style system
- Actual shader implementation (GLSL, HLSL, etc.)
- Real-time audio analysis
- Performance considerations

---

## 1. Shader Architecture

### 1.1 Pass-Based System

Glitchcore shaders should use a multi-pass architecture:

```
PASS 0: Source Input
   ↓
PASS 1: Primary Driver (channel split, temporal echo, etc.)
   ↓
PASS 2: Secondary Drivers (bloom, overprint, etc.)
   ↓
PASS 3: Palette Application
   ↓
PASS 4: Anchor Protection / Composite
   ↓
OUTPUT: Final Image
```

---

### 1.2 Shader Families

Organize shaders by artifact driver:

| Family | Description |
|--------|-------------|
| Channel Displacement | RGB split, chromatic aberration |
| Temporal Feedback | Frame delay, echo, motion trails |
| Bloom Halation | Glow, light bleed, halation |
| Overprint Layers | Duplicate copies, multi-exposure |
| Scanline Raster | CRT lines, contour banding |
| Compression Damage | Block artifacts, codec corruption |
| Text Debris | Font rendering, text overlay |
| Noise Texture | Static, grain, interference |
| Color Processing | Palette application, color grading |

---

## 2. Audio-Reactive Architecture

### 2.1 Audio Analysis Pipeline

```
AUDIO INPUT
   ↓
FFT Analysis (frequency bands)
   ↓
Feature Extraction (bass, mids, highs, transients)
   ↓
Smoothing/Decay (prevent jitter)
   ↓
Parameter Mapping (audio → visual)
   ↓
SHADER UNIFORMS
```

---

### 2.2 Frequency Bands

Standard 4-band analysis:

| Band | Range | Typical Use |
|------|-------|-------------|
| Bass | 20-250Hz | Structural distortion |
| Low Mids | 250-500Hz | Duplicate spacing |
| High Mids | 500-2000Hz | Edge activity |
| Highs | 2000-8000Hz | Sparkle, fringe |

Extended 8-band for precision:

| Band | Range | Use |
|------|-------|-----|
| Sub Bass | 20-60Hz | Heavy structural |
| Bass | 60-250Hz | Standard structural |
| Low Mids | 250-500Hz | Echo spacing |
| Mids | 500-2000Hz | Edge emphasis |
| High Mids | 2000-4000Hz | Detail activity |
| Highs | 4000-8000Hz | Sparkle density |
| Air | 8000-16000Hz | Fine detail |
| Transients | Peaks | Rupture events |

---

### 2.3 Audio Feature Types

**Amplitude:**
- Overall loudness
- Drives global intensity

**Frequency Energy:**
- Per-band levels
- Drives specific visual parameters

**Transients:**
- Sharp attacks
- Trigger rupture events

**Onset Detection:**
- Beat identification
- Trigger state changes

**Spectral Centroid:**
- "Brightness" of sound
- Drives color temperature

**Spectral Flux:**
- How much spectrum changes
- Drives chaos/instability

---

## 3. Audio-to-Visual Mapping

### 3.1 Universal Mappings

These apply across most subtypes:

| Audio Feature | Visual Parameter |
|---------------|------------------|
| Bass amplitude | Primary driver strength |
| Transients | Rupture/glitch events |
| Highs | Sparkle/noise density |
| Spectral centroid | Color temperature |
| Overall amplitude | Global intensity |

---

### 3.2 Subtype-Specific Mappings

**Candy Broadcast (Spectrum Reactive):**
```
Bass → RGB offset width
Low Mids → Duplicate spacing
High Mids → Bloom intensity
Highs → Sparkle density
Transients → Channel snap jumps
```

**Ghost-Frame (Trail Reactive):**
```
Beat → Reinforce present frame
Low Mids → Echo count
Pads → Trail persistence
Transients → Stutter copies
Amplitude → Trail brightness
```

**Text-Screen (Semantic Reactive):**
```
Speech presence → Text emission
Emotional peaks → Face-text overlap
Silence → Ghost text lingering
Amplitude → Phrase density
High Mids → Text clarity
```

**Candy-Crash (Compression Reactive):**
```
Bass → Block size
Transients → Packet loss
High Mids → Edge buzz
Vocals → Face zone smear
Amplitude → Compression pressure
```

**CRT Contour (Pulse Reactive):**
```
Bass → Contour thickness
Highs → Scanline shimmer
Sustained tones → Halo build
Transients → Row jitter
Vocals → Face contour emphasis
```

---

## 4. Shader Implementation Notes

### 4.1 Performance Considerations

**Frame Budget:**
- Target 60fps minimum
- 30fps acceptable for complex effects
- Audio analysis: every frame or every 2-3 frames

**Texture Memory:**
- Reuse render targets
- Limit history buffer size for temporal effects
- Use appropriate texture formats

**Shader Complexity:**
- Keep fragment shaders lean
- Move heavy computation to vertex shaders where possible
- Use lookup textures for complex functions

---

### 4.2 Uniform Strategy

Standard uniforms for all glitchcore shaders:

```glsl
// Time
uniform float uTime;

// Resolution
uniform vec2 uResolution;

// Source texture
uniform sampler2D uSourceTexture;

// Audio features
uniform float uBass;
uniform float uLowMids;
uniform float uHighMids;
uniform float uHighs;
uniform float uTransients;
uniform float uAmplitude;

// Style parameters
uniform float uIntensity;        // 0.0 - 1.0
uniform float uDensity;          // 0.0 - 1.0
uniform vec3 uDominantColor;
uniform vec3 uCollisionColor;
uniform vec3 uAccentColor;

// Driver strengths
uniform float uChannelSplitStrength;
uniform float uBloomStrength;
uniform float uOverprintStrength;
uniform float uTemporalStrength;
uniform float uCompressionStrength;
uniform float uTextStrength;

// Anchor protection
uniform float uFaceProtection;   // 0.0 - 1.0
uniform float uEyeProtection;    // 0.0 - 1.0
uniform float uMouthProtection;  // 0.0 - 1.0
```

---

### 4.3 Audio Smoothing

Prevent jitter with exponential smoothing:

```glsl
// In CPU/audio thread
float smoothedBass = lerp(previousBass, currentBass, 0.3);

// Or in shader
float smoothBass = mix(uBass, uBassPrev, 0.7);
```

Attack/decay times:
- Fast attack (10-30ms) for transients
- Slow decay (100-500ms) for sustained features

---

## 5. State Management

### 5.1 Musical Section Detection

Detect and respond to song structure:

| Section | Visual Response |
|---------|-----------------|
| Intro | Minimal, establish anchors |
| Verse | Balanced, preserve clarity |
| Pre-Chorus | Build tension |
| Chorus | Maximum density |
| Bridge | Experimental, different drivers |
| Breakdown | Sparse with intense moments |
| Build | Increasing pressure |
| Drop | Explosion then recovery |
| Outro | Fading, lingering ghosts |

---

### 5.2 State Transition Rules

```
IF chorus_detected AND current_density < target_chorus_density
  → Gradually increase density over 2-4 beats

IF verse_detected AND current_density > target_verse_density
  → Gradually decrease density over 2-4 beats

IF drop_detected
  → Brief spike to maximum
  → Recover over 1-2 beats
```

---

## 6. Platform Considerations

### 6.1 Web (WebGL/Three.js)

- Use ping-pong render targets for feedback
- Limit shader complexity for mobile
- Consider WebGL 2.0 for compute shaders

### 6.2 Mobile (OpenGL ES)

- Reduce texture sizes
- Simplify shaders
- Lower frame rate acceptable
- Battery-aware throttling

### 6.3 Desktop (OpenGL/Vulkan/DirectX)

- Full feature set
- Multiple render targets
- Compute shaders for audio analysis
- Higher quality settings

---

## 7. Debugging & Tuning

### 7.1 Audio Visualization

Show audio features as overlays:

```
[Bass ████████░░] 0.78
[LowM ██████░░░░] 0.62
[HiMid ████░░░░░░] 0.41
[High █████░░░░░] 0.55
[Trans ▓▓▓▓▓▓▓▓▓▓] 0.92
```

### 7.2 Parameter Monitoring

Show current shader uniforms:

```
Channel Split: 0.72
Bloom: 0.45
Overprint: 0.38
Temporal: 0.21
Compression: 0.15
Text: 0.08
```

---

## 8. Summary

The shader and audio-reactive system provides:
- Multi-pass shader architecture
- Audio analysis pipeline
- Frequency-to-visual mappings
- Performance guidelines
- Platform considerations
- State management
- Debugging tools

This enables real-time glitchcore effects that respond musically and perform well.

---

## 9. Short Anchor Rule

The music should conduct the corruption, not just trigger it.
