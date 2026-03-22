# Compression and Codec Corruption

Digital artifact systems that simulate file damage and codec breakdown.

## Purpose

This file defines compression and codec corruption in glitchcore — how digital file damage becomes aesthetic, how codec artifacts create emotional texture, and how "bad quality" becomes beautiful.

This is the part that helps the app stop going:
"make it look low quality"
and start going:
"macroblock breakup with chroma smear, one beauty zone preserved, bratty internet-broken energy."

The compression system here is designed to make digital damage emotionally intelligent — not just bad quality, but meaningful quality.

---

## 1. Compression Philosophy

### 1.1 Core Principle

Compression damage in glitchcore is not about making things look bad. It's about making things look *broken in a specific way*.

The damage should feel:
- Intentional, not accidental
- Aesthetic, not just technical
- Emotional, not just degraded
- Beautiful, not just low-quality

**Wrong:**
- Generic low resolution
- Uniform blur
- Simple pixelation
- No preservation

**Right:**
- Specific codec artifacts
- Macroblock patterns
- Chroma bleeding
- One beauty zone preserved

---

### 1.2 The Beauty vs Damage Tension

The key to compression glitchcore is tension:

```
One zone = beautiful, clear, hot
Everything else = broken, compressed, damaged
```

This tension creates:
- Emotional contrast
- Aesthetic interest
- Narrative (what's being protected?)
- Bratty defiance (I'm broken but still beautiful)

---

## 2. Compression Artifact Types

### 2.1 Macroblock Breakup

**What It Is:**
Visible compression blocks (usually 8x8 or 16x16 pixels) that break apart and misalign.

**Visual Character:**
- Grid-like block patterns
- Blocks misaligned from original position
- Visible at edges and motion areas
- Classic "MPEG artifact" look

**Parameters:**
```
block_size: 8, 16, 32      # Size of compression blocks
misalignment: 0.0-1.0      # How far blocks shift
edge_preference: 0.0-1.0   # More blocks at edges
motion_bias: 0.0-1.0       # More blocks in motion areas
```

**Best For:**
- Candy crash compression
- Internet-broken aesthetic
- Bratty energy
- Visible digital damage

---

### 2.2 Chroma Smear

**What It Is:**
Color information (chroma) bleeds and smears while luminance stays relatively clear.

**Visual Character:**
- Colors bleed beyond edges
- Rainbow edges on high contrast
- Color information lags behind motion
- "Color trailing" effect

**Parameters:**
```
smear_amount: 0.0-1.0      # How much colors bleed
edge_sensitivity: 0.0-1.0  # How edges trigger smear
motion_smear: 0.0-1.0      # Smear follows motion
color_separation: 0.0-1.0  # RGB channels separate
```

**Best For:**
- Colorful compression
- Digital coldness
- Chroma-heavy subtypes
- Rainbow edge effects

---

### 2.3 Quantization Banding

**What It Is:**
Visible bands of color where smooth gradients should be, caused by aggressive compression.

**Visual Character:**
- Stair-step gradients
- Visible color bands
- Sky and skin show it most
- "Posterization" effect

**Parameters:**
```
band_visibility: 0.0-1.0   # How visible the bands are
gradient_sensitivity: 0.0-1.0 # How gradients trigger banding
band_softness: 0.0-1.0     # Hard vs soft bands
color_depth: 2-8           # Simulated bit depth
```

**Best For:**
- Sky corruption
- Skin degradation
- Atmospheric damage
- Retro-digital aesthetic

---

### 2.4 Edge Buzz

**What It Is:**
High-frequency corruption at edges, creating a buzzing, vibrating effect.

**Visual Character:**
- Edges appear to vibrate
- High-frequency noise at boundaries
- Motion-like static on edges
- Electric, unstable feeling

**Parameters:**
```
buzz_intensity: 0.0-1.0    # How strong the buzz is
edge_detection: 0.0-1.0    # How edges are detected
frequency: float           # Buzz frequency
motion_correlation: 0.0-1.0 # Buzz follows motion
```

**Best For:**
- Electric energy
- Unstable moments
- Edge emphasis
- High-tension scenes

---

### 2.5 Packet Loss Puncture

**What It Is:**
Sudden, sharp moments of data loss — blocks of image just disappear or corrupt dramatically.

**Visual Character:**
- Sharp rectangular corruptions
- Sudden color blocks
- "Digital dropout" moments
- Intermittent, transient

**Parameters:**
```
loss_frequency: 0.0-1.0    # How often packet loss occurs
loss_size: 0.0-1.0         # Size of loss blocks
loss_duration: float       # How long losses last
recovery_speed: 0.0-1.0    # How fast image recovers
```

**Best For:**
- Streaming damage
- Network failure moments
- Transient chaos
- Audio-reactive punctures

---

### 2.6 DCT Block Artifacts

**What It Is:**
Artifacts from Discrete Cosine Transform compression — the mathematical basis of JPEG and MPEG.

**Visual Character:**
- Blocky patterns within blocks
- "Mosquito noise" around edges
- Ringing artifacts
- Mathematical corruption patterns

**Parameters:**
```
mosquito_noise: 0.0-1.0    # Edge ringing intensity
ringing: 0.0-1.0           # Halo around edges
block_visibility: 0.0-1.0  # How visible block structure is
compression_ratio: 0.0-1.0 # Simulated compression level
```

**Best For:**
- Technical accuracy
- JPEG/MPEG simulation
- Mathematical beauty
- Codec-specific aesthetics

---

## 3. Codec-Specific Behaviors

### 3.1 JPEG Artifacts

**Characteristics:**
- 8x8 block structure
- DCT ringing
- Chroma subsampling visible
- Quality 0-100 scale

**Visual Markers:**
- Blocky degradation
- Color bleeding
- Ringing at edges
- Progressive quality loss

---

### 3.2 MPEG/H.264 Artifacts

**Characteristics:**
- Motion compensation blocks
- Reference frame errors
- Temporal propagation
- I/P/B frame differences

**Visual Markers:**
- Motion-block patterns
- Error propagation
- Keyframe pulses
- Compression breathing

---

### 3.3 GIF Artifacts

**Characteristics:**
- Limited color palette (256 colors)
- Dithering patterns
- No partial transparency
- Frame-based animation

**Visual Markers:**
- Color banding
- Dither dots
- Sharp color transitions
- Retro web aesthetic

---

### 3.4 Screenshot Degradation

**Characteristics:**
- Multiple compression passes
- Color profile shifts
- Resolution reduction
- Platform-specific artifacts

**Visual Markers:**
- "Reposted too many times" look
- Color drift
- Progressive quality loss
- Social media compression

---

## 4. Compression + Other Drivers

### 4.1 Compression + Bloom

**Effect:**
Compression damage glows and softens, creating "beautiful damage."

**Use For:**
- Glamorous compression
- Soft internet heartbreak
- Beautiful malfunction

---

### 4.2 Compression + Channel Split

**Effect:**
Compressed colors separate, creating chromatic chaos.

**Use For:**
- Maximum color damage
- RGB phantom + compression
- Chromatic explosion

---

### 4.3 Compression + Text

**Effect:**
Text degrades along with image, creating mediated damage.

**Use For:**
- Text screen heartbreak
- Message corruption
- Digital confession damage

---

### 4.4 Compression + Temporal Echo

**Effect:**
Compression errors echo through time, creating persistent damage trails.

**Use For:**
- Ghost frame + compression
- Persistent damage
- Memory corruption

---

## 5. Compression Parameters by Subtype

| Subtype | Primary Compression | Secondary | Intensity |
|---------|---------------------|-----------|-----------|
| Candy Crash | Macroblock | Chroma Smear | High |
| Screenshot Damage | Multi-pass | Color Drift | Medium-High |
| Internet-Broken | Packet Loss | Edge Buzz | Medium |
| Codec Aesthetic | DCT Artifacts | Quantization | Medium |
| Bratty Quality | All Types | Mixed | High |

---

## 6. Compression Drift Detection

### 6.1 Generic Low Quality

**Symptoms:**
- Just looks blurry
- No specific artifact type
- No beauty preservation
- Boring degradation

**Fix:**
- Add specific artifact types
- Preserve one beauty zone
- Add color to damage
- Create tension

---

### 6.2 Too Much Damage

**Symptoms:**
- Image is unrecognizable
- No anchor preserved
- Just looks broken
- No aesthetic value

**Fix:**
- Reduce overall intensity
- Add beauty zone preservation
- Create damage hierarchy
- Let something survive

---

### 6.3 Uniform Degradation

**Symptoms:**
- Same damage everywhere
- No variation
- No interest
- Flat quality loss

**Fix:**
- Add edge preference
- Create damage zones
- Vary intensity across image
- Add preservation areas

---

## 7. Short Anchor Rule

**Make the damage beautiful, not just bad.**
