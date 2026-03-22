# AI Control Logic Map

How the AI should interpret glitchcore style inputs and generate outputs that match the system.

## Purpose

This file defines the control logic for AI systems generating glitchcore images.

Its job is to bridge:
- User input (natural language, controls, selections)
- The glitchcore style system (subtypes, drivers, palettes, density)
- The actual image generation process (prompts, parameters, refinement)

This is the brain that turns "make it glitchy" into actual structured corruption.

---

## 1. Input Interpretation Layer

### 1.1 User Input Types

The AI should handle these input types:

**Natural Language:**
- "Make it dreamy and broken"
- "Candy broadcast diva energy"
- "Sad terminal confession vibe"
- "Bright hyperpop glitch portrait"

**Structured Selections:**
- Subtype: [dropdown selection]
- Intensity: [slider 1-5]
- Color mood: [palette family selection]
- Motion: [static / echo / trail]
- Text amount: [none / sparse / moderate / dense]

**Reference Images:**
- "Like this but more bratty"
- "Similar to reference but with more compression"

**Hybrid Requests:**
- "Candy broadcast + text screen heartbreak"
- "Pastel smear with surveillance coldness"

---

### 1.2 Input Parsing Logic

**Step 1: Identify Core Intent**

Parse user input for:
- Emotional keywords (dreamy, bratty, lonely, seductive, etc.)
- Subtype hints (candy, pastel, RGB, ghost, text, etc.)
- Visual descriptors (bright, dark, glossy, soft, etc.)
- Technical cues (glitch, VHS, digital, screen, etc.)

**Step 2: Map to Subtype**

| Input Cue | Likely Subtype |
|-----------|----------------|
| candy, bright, pop, hyperpop | Candy Broadcast Hallucination |
| pastel, soft, dreamy, romantic | Pastel Identity Smear |
| RGB, chromatic, spectral, electric | RGB Phantom |
| ghost, motion, trail, echo | Ghost-Frame Body |
| text, chat, terminal, confession | Text-Screen Heartbreak |
| CRT, scanline, phosphor, retro | CRT Contour |
| compression, codec, broken, internet | Candy-Crash Compression |
| surveillance, CCTV, watched, cold | Surveillance Apparition |
| glitter, glossy, diva, glam | Glitter-Signal Overprint |
| all, everything, maximal, fever | Composite Fever Dream |

**Step 3: Map to Palette**

| Input Cue | Likely Palette |
|-----------|----------------|
| bright, hyperpop, magenta, cyan | Hyperpop Rupture |
| pastel, soft, pink, lavender | Pastel Signal Melt |
| glossy, expensive, diva | Gloss-Electric Glam |
| dark, cold, teal, noir | Phosphor Noir |
| broken, codec, internet | Codec Candy Crash |
| rainbow, all colors | Rainbow Channel Hallucination |

**Step 4: Map to Density**

| Input Cue | Likely Density |
|-----------|----------------|
| subtle, gentle, soft | Sparse |
| balanced, moderate | Moderate |
| intense, heavy, dense | Dense |
| extreme, maximum, overloaded | Overloaded |
| everything, chaos, pile-up | Pile-Up Delirium |

---

## 2. Decision Tree Logic

### 2.1 Primary Decision: Subtype Selection

```
IF user mentions "candy" OR "bright" OR "hyperpop" OR "pop"
  → Candy Broadcast Hallucination

ELSE IF user mentions "pastel" OR "dreamy" OR "soft" OR "romantic"
  → Pastel Identity Smear

ELSE IF user mentions "RGB" OR "chromatic" OR "spectral" OR "electric"
  → RGB Phantom

ELSE IF user mentions "ghost" OR "motion" OR "trail" OR "echo" OR "time"
  → Ghost-Frame Body

ELSE IF user mentions "text" OR "chat" OR "terminal" OR "confession" OR "message"
  → Text-Screen Heartbreak

ELSE IF user mentions "CRT" OR "scanline" OR "phosphor" OR "monitor"
  → CRT Contour

ELSE IF user mentions "compression" OR "codec" OR "broken" OR "internet" OR "file"
  → Candy-Crash Compression

ELSE IF user mentions "surveillance" OR "CCTV" OR "watched" OR "cold" OR "monitor"
  → Surveillance Apparition

ELSE IF user mentions "glitter" OR "glossy" OR "diva" OR "glam"
  → Glitter-Signal Overprint

ELSE IF user mentions "everything" OR "all" OR "maximal" OR "fever"
  → Composite Fever Dream

ELSE
  → Ask for clarification OR default to Candy Broadcast Hallucination
```

---

### 2.2 Secondary Decision: Driver Selection

```
IF subtype = Candy Broadcast
  primary_driver = channel_split
  secondary_drivers = [bloom_contamination, overprint_stacking]

ELSE IF subtype = Pastel Smear
  primary_driver = overprint_stacking
  secondary_drivers = [soft_channel_split, bloom_contamination]

ELSE IF subtype = RGB Phantom
  primary_driver = channel_split
  secondary_drivers = [phase_lag_duplication, edge_emphasis]

ELSE IF subtype = Ghost-Frame Body
  primary_driver = temporal_echo
  secondary_drivers = [multi_exposure_stack, bloom_trail_haze]

ELSE IF subtype = Text-Screen Heartbreak
  primary_driver = text_interface_debris
  secondary_drivers = [subtitle_ghosting, compression_haze]

ELSE IF subtype = CRT Contour
  primary_driver = scanline_contour_banding
  secondary_drivers = [phosphor_bloom, static_veil]

ELSE IF subtype = Candy-Crash Compression
  primary_driver = compression_chew
  secondary_drivers = [macroblock_breakup, chroma_smear]

ELSE IF subtype = Surveillance Apparition
  primary_driver = capture_degradation
  secondary_drivers = [noise_veil, pixel_matrix]

ELSE IF subtype = Glitter-Signal Overprint
  primary_driver = overprint_stacking
  secondary_drivers = [bloom_contamination, sparkle_static]

ELSE IF subtype = Composite Fever Dream
  primary_driver = overprint_stacking
  secondary_drivers = [channel_split, bloom, compression, text, temporal]
```

---

### 2.3 Tertiary Decision: Palette Selection

```
IF emotional_tone = "seductive" OR "bratty" OR "loud"
  palette = hyperpop_rupture
  dominant = magenta_hot_pink
  collision = cyan_electric_blue
  accent = white_flare

ELSE IF emotional_tone = "dreamy" OR "soft" OR "romantic"
  palette = pastel_signal_melt
  dominant = cotton_candy_pink
  collision = lavender_baby_blue
  accent = pearl_white

ELSE IF emotional_tone = "glamorous" OR "expensive" OR "diva"
  palette = gloss_electric_glam
  dominant = glossy_hot_pink
  collision = cool_violet_cyan
  accent = white_silver

ELSE IF emotional_tone = "cold" OR "eerie" OR "remote"
  palette = phosphor_noir
  dominant = teal_cyan
  collision = ice_blue
  accent = warning_red_small

ELSE IF emotional_tone = "broken" OR "internet" OR "cheap"
  palette = codec_candy_crash
  dominant = magenta
  collision = flat_cyan_violet
  accent = white_lime

ELSE IF emotional_tone = "electric" OR "unstable" OR "spectral"
  palette = rainbow_channel_hallucination
  dominant = cyan_magenta
  collision = green_spectral_intrusion
  accent = white_yellow
```

---

## 3. Prompt Assembly Logic

### 3.1 Prompt Construction Order

```
1. SUBJECT DESCRIPTION
   → "close-up beauty portrait"
   → "profile glam figure"
   → "dancer mid-movement"

2. SUBTYPE DECLARATION
   → "treated as [subtype]"

3. PRIMARY DRIVER
   → "with [driver] as main transformation"

4. SECONDARY DRIVERS
   → "supported by [driver1], [driver2]"

5. PALETTE SPECIFICATION
   → "using [palette] with [dominant], [collision], [accent]"

6. DENSITY LEVEL
   → "at [density] signal load"

7. EMOTIONAL FLAVOR
   → "creating mood of [emotion1], [emotion2]"

8. MATERIAL FEEL
   → "with [material] surface"

9. PRESERVED ANCHOR
   → "while preserving [anchor]"

10. ANTI-DRIFT CLAUSE
    → "not [drift_type]"
```

---

### 3.2 Example Assembly

**Input:** "Make a dreamy pastel glitch portrait with soft colors"

**Parsed:**
- Subtype: Pastel Identity Smear
- Palette: Pastel Signal Melt
- Density: Moderate
- Emotion: Dreamy, romantic

**Assembled Prompt:**
```
A frontal beauty portrait treated as a pastel identity smear, with overprint stacking as the main transformation logic, supported by soft channel split and creamy bloom haze, using a pastel signal melt palette with dominant cotton-candy pink, lavender collision, and pearl-white accent punctures, at moderate signal density, creating a dreamy, romantic, dissociative mood, with velvety cosmetic surface feel, while preserving the eyes and lips, not a generic dreamy filter or beauty ad.
```

---

## 4. Refinement Loop Logic

### 4.1 Evaluation Check

After generating an image, evaluate:

```
IF figure_anchor_score < 3
  → Add stronger retrieval path
  → Preserve eyes/mouth/silhouette more explicitly

IF artifact_specificity_score < 3
  → Strengthen primary driver
  → Make artifact behavior more visible

IF palette_architecture_score < 3
  → Clarify palette hierarchy
  → Reduce color chaos

IF emotional_consequence_score < 3
  → Add explicit emotional tags
  → Make corruption affect beauty/identity

IF anti_drift_score < 3
  → Add anti-drift clause
  → Remove generic trend cues
```

---

### 4.2 Iterative Refinement

```
GENERATION 1: Initial output based on parsed input

EVALUATION: Score across rubric categories

IF total_score < 30
  → Major revision needed
  → Re-examine subtype/driver/palette choices

ELSE IF total_score < 38
  → Minor refinement needed
  → Adjust specific parameters

ELSE IF total_score >= 38
  → Success
  → Optional fine-tuning

GENERATION 2+: Refined based on evaluation

REPEAT until satisfactory or max_iterations reached
```

---

## 5. Hybrid Logic

### 5.1 Hybrid Detection

```
IF user mentions "+" OR "and" OR "with" OR "mixed with"
  → Parse for hybrid intent

IF two subtypes detected
  → Create hybrid configuration

IF more than two subtypes
  → Warn about soup risk
  → Suggest primary + secondary only
```

---

### 5.2 Hybrid Assembly

```
hybrid_type = detect_hybrid_type(subtype_a, subtype_b)

IF hybrid_type = "body_plus_contamination"
  → Body subtype leads
  → Contamination subtype secondary

ELSE IF hybrid_type = "palette_plus_failure"
  → Palette from one
  → Failure mode from other

ELSE IF hybrid_type = "structure_plus_motion"
  → Structural driver leads
  → Motion driver secondary

ELSE IF hybrid_type = "atmosphere_plus_text"
  → Atmosphere subtype leads
  → Text subtype secondary

primary_driver = subtype_a.primary_driver
secondary_drivers = [subtype_a.secondary_drivers + subtype_b.drivers]
palette = choose_dominant_palette(subtype_a, subtype_b)
```

---

## 6. Error Handling

### 6.1 Ambiguous Input

```
IF input is too vague
  → Ask clarifying questions:
    - "Do you want bright and loud or soft and dreamy?"
    - "Should the corruption be subtle or intense?"
    - "Is this more about beauty or about damage?"
```

---

### 6.2 Conflicting Input

```
IF conflicting cues detected
  → Prioritize:
    1. Explicit subtype mention
    2. Emotional keywords
    3. Technical descriptors
    4. Visual adjectives

  → Warn user:
    - "I detected conflicting cues. Prioritizing [choice]."
```

---

### 6.3 Drift Detection

```
IF output shows drift signs
  → Identify drift type
  → Apply rescue recipe
  → Regenerate with fixes
```

---

## 7. Control Interface Mapping

### 7.1 Slider Mappings

| Slider | Parameter | Range |
|--------|-----------|-------|
| Intensity | primary_driver_strength | 0.0 - 1.0 |
| Color Saturation | palette_saturation | 0.0 - 1.0 |
| Motion/Time | temporal_echo_amount | 0.0 - 1.0 |
| Text Amount | text_density | 0.0 - 1.0 |
| Compression | compression_strength | 0.0 - 1.0 |
| Glow/Bloom | bloom_intensity | 0.0 - 1.0 |

---

### 7.2 Dropdown Mappings

| Dropdown | Maps To |
|----------|---------|
| Style Branch | subtype |
| Color Mood | palette_family |
| Density | density_level |
| Face Preservation | anchor_protection_level |
| Motion Type | temporal_behavior |

---

## 8. Summary

The AI control logic map provides:
- Input parsing rules
- Decision trees for subtype/driver/palette selection
- Prompt assembly order
- Refinement loop logic
- Hybrid handling
- Error handling
- Control interface mappings

This system ensures that user inputs are consistently translated into structured glitchcore outputs that match the style system's principles.

---

## 9. Short Anchor Rule

Parse the feeling first, then build the corruption around it.
