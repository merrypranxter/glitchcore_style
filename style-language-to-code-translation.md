# Style Language to Code Translation

How to turn glitchcore descriptive language into actual implementation logic.

## Purpose

This file bridges the gap between the poetic, descriptive language of glitchcore aesthetics and the concrete code that makes it work.

This is the part that helps the app stop going:
"what does 'seductive signal damage' even mean?"
and start going:
"seductive = preserve eyes/lips, signal damage = channel_split at 0.7 strength."

The translations here are designed to make the style system implementable without losing its emotional and aesthetic intent.

---

## 1. Emotion Tag Translation

### 1.1 Seductive

**Descriptive Meaning:** Attractive, alluring, draws the viewer in

**Code Translation:**
```
preserve_zones: [eyes, lips, face_center]
corruption_flow: inward_from_edges
palette_bias: warm_pinks_magentas
bloom_strength: 0.6 (glow on skin)
edge_softness: 0.4 (inviting, not harsh)
```

**Visual Result:** Face remains attractive while edges corrupt

---

### 1.2 Bratty

**Descriptive Meaning:** Defiant, playful, cheap-beautiful, internet-broken

**Code Translation:**
```
primary_driver: compression_chew
secondary_drivers: [macroblock_breakup, chroma_smear]
palette_bias: saturated_magenta_cyan
quality_degradation: 0.7
block_size_variance: high
emotion: defiant_playful
```

**Visual Result:** Looks like a screenshot that's been reposted too many times

---

### 1.3 Dreamy

**Descriptive Meaning:** Soft, dissociative, romantic, fragile

**Code Translation:**
```
primary_driver: soft_overprint
secondary_drivers: [gentle_bloom, pastel_palette]
blur_amount: 0.3
duplicate_opacity: 0.4 (ghostly)
color_saturation: 0.6 (muted)
temporal_echo: light
```

**Visual Result:** Soft, floating, memory-like corruption

---

### 1.4 Electric

**Descriptive Meaning:** Energetic, unstable, high-frequency, alive

**Code Translation:**
```
primary_driver: channel_split
secondary_drivers: [edge_emphasis, sparkle_static]
rgb_offset: 0.5 (strong separation)
edge_chatter: 0.7
sparkle_density: high
flicker_rate: medium_fast
```

**Visual Result:** Vibrating, high-energy color separation

---

### 1.5 Lonely

**Descriptive Meaning:** Isolated, confessional, mediated tenderness

**Code Translation:**
```
primary_driver: text_interface_debris
secondary_drivers: [subtitle_ghosting, compression_haze]
text_behavior: fragmented_confessional
palette_bias: cool_blues_grays
brightness: 0.7 (dimmed)
isolation_emphasis: high
```

**Visual Result:** Text fragments floating in dim, degraded space

---

### 1.6 Glamorous

**Descriptive Meaning:** Glossy, radiant, overlit, diva-energy

**Code Translation:**
```
primary_driver: overprint_stacking
secondary_drivers: [bloom_contamination, sparkle_static]
gloss_emphasis: 0.8
overprint_layers: 3-5
sparkle_density: high
lighting: overlit_beauty
```

**Visual Result:** Glossy, radiant corruption that feels expensive

---

### 1.7 Haunted

**Descriptive Meaning:** Ghostly, ceremonial, ritualistic, eerie

**Code Translation:**
```
primary_driver: temporal_echo
secondary_drivers: [ghost_frame_stack, phosphor_bloom]
echo_count: 5-8
echo_fade: gradual
palette_bias: cool_teals_cyans
ritual_emphasis: high
```

**Visual Result:** Multiple time layers visible, ghostly presence

---

### 1.8 Decadent

**Descriptive Meaning:** Overloaded, excessive, beautiful malfunction, feverish

**Code Translation:**
```
primary_driver: composite_pile_up
secondary_drivers: [all_available]
density: maximum
layer_count: 5+
palette: rainbow_channel_hallucination
controlled_chaos: true
```

**Visual Result:** Maximum corruption that still holds together

---

## 2. Driver Name Translation

### 2.1 Channel Split

**Also Called:** RGB Displacement, Chromatic Aberration, Color Separation

**Code Parameters:**
```
channel_split:
  red_offset: [x, y]    # Red channel displacement
  green_offset: [x, y]  # Green channel displacement
  blue_offset: [x, y]   # Blue channel displacement
  edge_bias: float      # Wider at edges (0-1)
  strength: float       # Overall intensity (0-1)
```

**Visual Description:** Colors separate like a prism, edges most affected

---

### 2.2 Overprint Stacking

**Also Called:** Duplicate Layers, Ghost Copies, Multi-Exposure

**Code Parameters:**
```
overprint_stacking:
  layer_count: int           # Number of duplicates
  offset_pattern: string     # "radial", "directional", "random"
  opacity_falloff: float     # How fast layers fade (0-1)
  blend_mode: string         # "screen", "add", "multiply"
  center_bias: float         # Stack outward from center (0-1)
```

**Visual Description:** Multiple semi-transparent copies layered over each other

---

### 2.3 Bloom Contamination

**Also Called:** Glow, Halation, Light Bleed

**Code Parameters:**
```
bloom_contamination:
  threshold: float      # Brightness threshold for bloom
  radius: float         # Bloom spread distance
  intensity: float      # Bloom brightness
  color_bias: string    # "warm", "cool", "neutral"
  edge_preference: float # Bloom stronger at edges (0-1)
```

**Visual Description:** Bright areas glow and bleed into darker areas

---

### 2.4 Temporal Echo

**Also Called:** Motion Trails, Frame Stacking, Time Ghosts

**Code Parameters:**
```
temporal_echo:
  echo_count: int       # Number of historical frames
  fade_curve: string    # "linear", "exponential", "ease_out"
  direction_bias: string # "motion", "radial", "random"
  persistence: float    # How long echoes last (0-1)
  brightness_falloff: float # Echo brightness decay
```

**Visual Description:** Previous moments linger as fading ghosts

---

### 2.5 Compression Chew

**Also Called:** Block Damage, Macroblock Artifacts, Codec Corruption

**Code Parameters:**
```
compression_chew:
  block_size: int       # Size of compression blocks
  quality: float        # Compression quality (0-1, lower = worse)
  chroma_bleed: float   # Color bleeding amount
  edge_buzz: float      # Edge corruption intensity
  random_seed: int      # For consistent patterns
```

**Visual Description:** Digital artifacts, blocky corruption, color smearing

---

### 2.6 Text Interface Debris

**Also Called:** Terminal Residue, UI Fragments, Text Ghosts

**Code Parameters:**
```
text_interface_debris:
  text_source: string       # "generated", "input", "random"
  density: float           # Amount of text (0-1)
  legibility: float        # How readable (0-1)
  overlap_bias: float      # Text over face/body (0-1)
  font_style: string       # "terminal", "subtitle", "ui"
  repetition: float        # How often phrases repeat
```

**Visual Description:** Fragments of text floating like digital debris

---

### 2.7 Scanline Contour

**Also Called:** CRT Lines, Phosphor Banding, Monitor Glow

**Code Parameters:**
```
scanline_contour:
  line_spacing: int     # Pixels between scanlines
  line_thickness: float # Thickness of each line
  phosphor_color: string # "cyan", "green", "white", "amber"
  glow_amount: float    # Phosphor bloom
  curvature: float      # Screen curvature (0 = flat)
  static_amount: float  # Faint noise overlay
```

**Visual Description:** CRT monitor lines following contours, phosphor glow

---

### 2.8 Capture Degradation

**Also Called:** Surveillance Noise, Feed Damage, Signal Loss

**Code Parameters:**
```
capture_degradation:
  noise_type: string    # "static", "banding", "pixelation"
  noise_intensity: float # Amount of noise (0-1)
  feed_weakness: float  # Overall signal quality (0-1)
  roll_speed: float     # Vertical roll speed
  glitch_frequency: float # How often glitches occur
  interface_traces: float # UI elements visible (0-1)
```

**Visual Description:** Weak surveillance feed, noise, occasional glitches

---

## 3. Palette Family Translation

### 3.1 Hyperpop Rupture

**Code Translation:**
```
dominant: [255, 0, 128]      # Hot magenta
collision: [0, 255, 255]      # Electric cyan
accent: [255, 255, 255]       # Sharp white
saturation: 0.9
contrast: 0.8
```

---

### 3.2 Pastel Signal Melt

**Code Translation:**
```
dominant: [255, 182, 193]    # Cotton candy pink
collision: [173, 216, 230]    # Baby blue
accent: [255, 250, 250]       # Pearl white
saturation: 0.5
contrast: 0.5
```

---

### 3.3 Gloss Electric Glam

**Code Translation:**
```
dominant: [255, 105, 180]    # Glossy hot pink
collision: [138, 43, 226]     # Cool violet
accent: [192, 192, 192]       # Silver/white
saturation: 0.8
contrast: 0.7
```

---

### 3.4 Phosphor Noir

**Code Translation:**
```
dominant: [0, 206, 209]      # Teal cyan
collision: [176, 224, 230]    # Ice blue
accent: [220, 20, 60]         # Warning red (small)
saturation: 0.6
contrast: 0.9
```

---

### 3.5 Codec Candy Crash

**Code Translation:**
```
dominant: [255, 0, 255]      # Magenta
collision: [0, 255, 255]      # Flat cyan
accent: [255, 255, 0]         # Lime highlight
saturation: 0.85
contrast: 0.75
```

---

## 4. Density Level Translation

### 4.1 Sparse Signal

**Code Translation:**
```
primary_driver_strength: 0.3
secondary_driver_count: 1
layer_complexity: low
visual_rest: 70%
```

---

### 4.2 Moderate Signal

**Code Translation:**
```
primary_driver_strength: 0.5
secondary_driver_count: 2
layer_complexity: medium
visual_rest: 50%
```

---

### 4.3 Dense Signal

**Code Translation:**
```
primary_driver_strength: 0.7
secondary_driver_count: 3-4
layer_complexity: high
visual_rest: 30%
```

---

### 4.4 Overloaded Signal

**Code Translation:**
```
primary_driver_strength: 0.9
secondary_driver_count: 4+
layer_complexity: maximum
visual_rest: 10%
```

---

### 4.5 Pile-Up Delirium

**Code Translation:**
```
all_drivers_active: true
layer_count: 5+
controlled_chaos: true
visual_rest: minimal
anchor_preservation: critical
```

---

## 5. Media Source Translation

### 5.1 Glossy Digital

**Code Translation:**
```
source_quality: high
lighting: overlit_beauty
surface: smooth_glossy
color_depth: 24bit
```

---

### 5.2 Screenshot Repost

**Code Translation:**
```
source_quality: degraded
compression_layers: 3+
color_banding: present
edge_artifacts: visible
```

---

### 5.3 CRT Monitor

**Code Translation:**
```
source_quality: analog
scanlines: visible
phosphor_glow: present
screen_curvature: slight
refresh_flicker: subtle
```

---

### 5.4 CCTV Feed

**Code Translation:**
```
source_quality: low
noise_level: high
frame_rate: low
compression: heavy
color: desaturated
```

---

## 6. Complete Example Translation

**Input:**
```
"seductive candy broadcast hallucination with bratty undertones"
```

**Translation Process:**
```
"seductive" → preserve eyes/lips, inward corruption flow
"candy broadcast" → subtype = candy_broadcast_hallucination
"hallucination" → density = dense_signal, drivers = channel_split + bloom
"bratty undertones" → add compression_chew at 0.3 strength
```

**Output Code:**
```json
{
  "subtype": "candy_broadcast_hallucination",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "bloom_contamination",
    "compression_chew"
  ],
  "driver_strengths": {
    "channel_split": 0.7,
    "bloom_contamination": 0.6,
    "compression_chew": 0.3
  },
  "palette_family": "hyperpop_rupture",
  "density_level": "dense_signal",
  "preserved_zones": ["eyes", "lips"],
  "corruption_flow": "inward_from_edges"
}
```

---

## 7. Short Anchor Rule

**Turn poetry into parameters without killing the poetry.**
