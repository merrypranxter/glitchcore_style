# Artifact Driver Taxonomy

A complete catalog of glitch corruption mechanisms and how they work.

## Purpose

This file catalogs every artifact driver in the glitchcore system — what it is, how it works, what it looks like, and when to use it.

This is the part that helps the app stop going:
"apply some glitch effects"
and start going:
"channel_split with edge_bias for this, temporal_echo for that."

The taxonomy here is designed to make corruption choices precise, intentional, and stylistically appropriate.

---

## 1. Primary Artifact Drivers

### 1.1 Channel Split (RGB Displacement)

**Also Known As:**
- Chromatic aberration
- Color separation
- RGB offset
- Prism displacement

**What It Does:**
Separates the red, green, and blue color channels and offsets them from each other, creating a prismatic, 3D-without-glasses effect.

**Visual Character:**
- Colors appear to separate at edges
- Like looking through a broken prism
- High-energy, electric feeling
- Most noticeable on high-contrast edges

**Parameters:**
```
red_offset: [x, y]      # Red channel displacement vector
green_offset: [x, y]    # Green channel displacement vector
blue_offset: [x, y]     # Blue channel displacement vector
edge_bias: 0.0-1.0      # Wider offset at edges vs center
strength: 0.0-1.0       # Overall intensity
```

**Best For:**
- RGB phantom
- Candy broadcast hallucination
- Electric, unstable energy
- Creating 3D-like depth without glasses

**Drift Risks:**
- Basic chromatic aberration (too simple)
- Equal offset everywhere (no edge bias)
- Too strong (destroys image)

**Anchor Behavior:**
- Can be tight at anchors (low edge_bias near eyes)
- Wide at edges (high edge_bias at periphery)

---

### 1.2 Overprint Stacking

**Also Known As:**
- Duplicate layers
- Ghost copies
- Multi-exposure
- Print registration error

**What It Does:**
Creates multiple semi-transparent copies of the image, offset from each other, like a printing press that didn't align properly.

**Visual Character:**
- Multiple ghost images layered
- Each copy slightly offset
- Creates depth through repetition
- Like seeing double or triple

**Parameters:**
```
layer_count: 2-10           # Number of duplicate layers
offset_pattern: string      # "radial", "directional", "random"
offset_distance: float      # How far layers are offset
opacity_falloff: 0.0-1.0    # How fast layers fade
blend_mode: string          # "screen", "add", "multiply", "normal"
center_bias: 0.0-1.0        # Stack outward from center
```

**Best For:**
- Glitter signal overprint
- Pastel identity smear
- Creating ghostly, dreamy effects
- Emphasizing movement or instability

**Drift Risks:**
- Equal opacity (no hierarchy)
- Too many layers (visual chaos)
- Random offsets (no intention)

**Anchor Behavior:**
- Stack outward from face center
- Preserve center layer most
- Let outer layers take damage

---

### 1.3 Bloom Contamination

**Also Known As:**
- Glow
- Halation
- Light bleed
- Luminous overflow

**What It Does:**
Bright areas of the image glow and bleed into darker areas, like light overwhelming the sensor or film.

**Visual Character:**
- Bright spots glow outward
- Soft, luminous edges
- Dreamy, ethereal quality
- Like looking through haze

**Parameters:**
```
threshold: 0.0-1.0      # Brightness threshold for bloom
radius: float           # How far bloom spreads
intensity: 0.0-1.0      # Bloom brightness multiplier
color_bias: string      # "warm", "cool", "neutral"
edge_preference: 0.0-1.0 # Bloom stronger at edges
```

**Best For:**
- Candy broadcast hallucination
- Glitter signal overprint
- Soft, glamorous effects
- Creating luminous, radiant subjects

**Drift Risks:**
- Too much bloom (loses detail)
- Generic glow filter look
- No color bias (boring)

**Anchor Behavior:**
- Glow around but not obscuring eyes
- Stronger at cheeks/jaw
- Softer at face center

---

### 1.4 Temporal Echo

**Also Known As:**
- Motion trails
- Frame stacking
- Time ghosts
- History persistence

**What It Does:**
Previous frames linger as fading ghosts, creating trails that follow movement through time.

**Visual Character:**
- Fading copies of previous moments
- Trails follow motion
- Sense of time visible
- Kinetic, dynamic feeling

**Parameters:**
```
echo_count: 2-10           # Number of historical frames
fade_curve: string         # "linear", "exponential", "ease_out"
direction_bias: string     # "motion", "radial", "random"
persistence: 0.0-1.0       # How long echoes last
brightness_falloff: 0.0-1.0 # Echo brightness decay
```

**Best For:**
- Ghost frame body
- Dance and movement
- Creating time-visible effects
- Kinetic, energetic subjects

**Drift Risks:**
- Equal opacity (no present moment)
- Too many echoes (chaos)
- Not following motion direction

**Anchor Behavior:**
- Present frame brightest
- Echoes follow motion
- Preserve gesture arcs

---

## 2. Secondary Artifact Drivers

### 2.1 Compression Chew

**Also Known As:**
- Block damage
- Macroblock artifacts
- Codec corruption
- JPEG damage

**What It Does:**
Simulates digital compression artifacts — blocky corruption, color smearing, and quality degradation.

**Visual Character:**
- Visible compression blocks
- Color bleeding between blocks
- Edge buzz and corruption
- "Internet-broken" look

**Parameters:**
```
block_size: 4-32          # Size of compression blocks
quality: 0.0-1.0          # Compression quality (lower = worse)
chroma_bleed: 0.0-1.0     # Color bleeding amount
edge_buzz: 0.0-1.0        # Edge corruption intensity
random_seed: int          # For consistent patterns
```

**Best For:**
- Candy crash compression
- Screenshot damage
- Internet-broken aesthetic
- Bratty, cheap-beautiful energy

**Drift Risks:**
- Generic low quality
- No beauty preservation
- Too uniform (not broken enough)

---

### 2.2 Text Interface Debris

**Also Known As:**
- Terminal residue
- UI fragments
- Text ghosts
- Interface corruption

**What It Does:**
Adds fragments of text, UI elements, and interface debris as visual corruption.

**Visual Character:**
- Floating text fragments
- UI elements mixed with image
- Like a broken terminal or crashed app
- Confessional, lonely feeling

**Parameters:**
```
text_source: string       # "generated", "input", "random"
density: 0.0-1.0          # Amount of text
legibility: 0.0-1.0       # How readable
overlap_bias: 0.0-1.0     # Text over face/body
font_style: string        # "terminal", "subtitle", "ui"
repetition: 0.0-1.0       # Phrase repetition
```

**Best For:**
- Text screen heartbreak
- Terminal confession
- Soft internet heartbreak
- Confessional, mediated emotions

**Drift Risks:**
- Poster design (too composed)
- Too legible (graphic design)
- No body overlap (decorative)

---

### 2.3 Scanline Contour

**Also Known As:**
- CRT lines
- Phosphor banding
- Monitor lines
- Raster scan

**What It Does:**
Creates horizontal lines that follow the contours of the subject, like a CRT monitor displaying the image.

**Visual Character:**
- Horizontal lines following shapes
- Phosphor glow effect
- Retro-futuristic feeling
- Iconic, graphic quality

**Parameters:**
```
line_spacing: 1-10        # Pixels between lines
line_thickness: 0.0-1.0   # Thickness of each line
phosphor_color: string    # "cyan", "green", "white", "amber"
glow_amount: 0.0-1.0      # Phosphor bloom
curvature: 0.0-1.0        # Screen curvature
static_amount: 0.0-1.0    # Faint noise overlay
```

**Best For:**
- CRT contour
- Signal saint aesthetic
- Retro-futuristic subjects
- Iconic, ceremonial feeling

**Drift Risks:**
- Op art wallpaper (too uniform)
- Generic scanline overlay
- No contour following

---

### 2.4 Capture Degradation

**Also Known As:**
- Surveillance noise
- Feed damage
- Signal loss
- CCTV corruption

**What It Does:**
Simulates weak surveillance feed — noise, degradation, occasional glitches, and institutional coldness.

**Visual Character:**
- Static and noise
- Occasional glitch flashes
- Weak signal quality
- Institutional, watched feeling

**Parameters:**
```
noise_type: string        # "static", "banding", "pixelation"
noise_intensity: 0.0-1.0  # Amount of noise
feed_weakness: 0.0-1.0    # Overall signal quality
roll_speed: float         # Vertical roll speed
glitch_frequency: 0.0-1.0 # How often glitches occur
interface_traces: 0.0-1.0 # UI elements visible
```

**Best For:**
- Surveillance apparatus
- Institutional coldness
- Watched, depersonalized feeling
- Eerie, remote atmosphere

**Drift Risks:**
- Generic analog horror
- Cinematic movie still
- Too polished

---

### 2.5 Sparkle Static

**Also Known As:**
- Glitter particles
- Specular highlights
- Star bursts
- Shine dots

**What It Does:**
Adds small, bright sparkle particles across the image, like glitter or specular highlights.

**Visual Character:**
- Tiny bright dots
- Glitter-like effect
- Glamorous, radiant feeling
- Adds texture and life

**Parameters:**
```
density: 0.0-1.0          # Amount of sparkles
size_range: [min, max]    # Size variation
brightness: 0.0-1.0       # Sparkle intensity
color: string             # "white", "gold", "rainbow"
movement: 0.0-1.0         # Sparkle movement/flicker
```

**Best For:**
- Glitter signal overprint
- Glamorous subjects
- Adding radiance and life
- Diva, expensive energy

---

### 2.6 Color Field Collision

**Also Known As:**
- Color clash
- Hue interference
- Palette rupture
- Chromatic tension

**What It Does:**
Creates areas where different color fields meet and clash, generating visual tension and energy.

**Visual Character:**
- Distinct color zones
- Tension at boundaries
- Vibrating edges where colors meet
- High energy, unstable feeling

**Parameters:**
```
zone_count: 2-5           # Number of color zones
boundary_sharpness: 0.0-1.0 # How sharp the edges
tension_intensity: 0.0-1.0 # How much colors fight
blend_mode: string        # How zones interact
```

**Best For:**
- Hyperpop rupture
- Color-heavy subtypes
- Creating visual tension
- Maximum energy moments

---

## 3. Driver Combination Rules

### 3.1 Primary + Secondary Pairings

| Primary | Best Secondary | Why |
|---------|----------------|-----|
| Channel Split | Bloom, Sparkle | Color + glow = electric |
| Overprint | Bloom, Soft Split | Layers + softness = dreamy |
| Bloom | Sparkle, Overprint | Glow + glitter = glamorous |
| Temporal Echo | Channel Split, Bloom | Motion + color = kinetic |

### 3.2 Avoid These Combinations

| Combination | Problem |
|-------------|---------|
| Compression + Scanline | Both reduce quality, too much |
| Text + Heavy Overprint | Both compete for attention |
| Capture Deg + Compression | Both noisy, muddy result |
| Maximum everything | No hierarchy, chaos soup |

---

## 4. Driver Selection by Subtype

| Subtype | Primary | Secondary |
|---------|---------|-----------|
| Candy Broadcast | Channel Split | Bloom, Overprint |
| RGB Phantom | Channel Split | Phase Lag, Edge |
| Ghost Frame | Temporal Echo | Multi-Exposure |
| Candy Crash | Compression | Macroblock, Chroma |
| Text Screen | Text Debris | Subtitle Ghost |
| CRT Contour | Scanline | Phosphor Bloom |
| Surveillance | Capture Deg | Noise Veil |
| Glitter Signal | Overprint | Bloom, Sparkle |
| Pastel Smear | Overprint | Soft Bloom |

---

## 5. Driver Intensity Guide

### 5.1 By Density Level

| Density | Driver Strength |
|---------|-----------------|
| Sparse | 0.2-0.3 |
| Moderate | 0.4-0.5 |
| Dense | 0.6-0.7 |
| Overloaded | 0.8-0.9 |
| Pile-Up | 0.9-1.0 |

### 5.2 By Zone

| Zone | Driver Strength |
|------|-----------------|
| Preserve High | 0.1-0.3 |
| Preserve Medium | 0.4-0.6 |
| Distort First | 0.7-1.0 |

---

## 6. Short Anchor Rule

**Every driver should know its job and do it well.**
