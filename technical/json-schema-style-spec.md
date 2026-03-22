# JSON Schema — Style Spec

Formal schema definition for glitchcore style configurations.

## Purpose

This file defines the formal JSON schema for glitchcore style specifications.

Its job is to provide:
- A machine-readable structure for style configs
- Validation rules for config files
- Type definitions for all parameters
- Reference for implementation

---

## 1. Schema Overview

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "$id": "glitchcore-style-spec",
  "title": "Glitchcore Style Configuration",
  "description": "Configuration for glitchcore image generation",
  "type": "object",
  "required": ["config_id", "subtype", "primary_driver"],
  "properties": {
    "config_id": { "type": "string" },
    "subtype": { "type": "string" },
    "primary_driver": { "type": "string" },
    "secondary_drivers": { "type": "array", "items": { "type": "string" } },
    "palette_family": { "type": "string" },
    "palette_structure": { "type": "object" },
    "density_level": { "type": "string" },
    "emotion_tags": { "type": "array", "items": { "type": "string" } },
    "preserved_anchors": { "type": "array", "items": { "type": "string" } },
    "drift_blockers": { "type": "array", "items": { "type": "string" } },
    "media_source": { "type": "string" },
    "audio_mode": { "type": "string" },
    "audio_mapping": { "type": "object" },
    "text_behavior": { "type": "object" },
    "hybrid_type": { "type": "string" },
    "notes": { "type": "string" }
  }
}
```

---

## 2. Field Definitions

### 2.1 config_id

**Type:** string
**Required:** yes
**Description:** Unique identifier for this configuration

**Examples:**
```json
"config_id": "cfg_001_candy_broadcast_portrait"
"config_id": "preset_candy_angel"
"config_id": "hybrid_011_dream_diary_face"
```

---

### 2.2 subtype

**Type:** string
**Required:** yes
**Description:** The glitchcore subtype/branch

**Enum:**
- candy_broadcast_hallucination
- pastel_identity_smear
- rgb_phantom
- composite_fever_dream
- crt_contour
- ghost_frame_body
- raster_meltdown
- pixel_ghost
- text_screen_heartbreak
- surveillance_apparition
- candy_crash_compression
- glitter_signal_overprint

**Example:**
```json
"subtype": "candy_broadcast_hallucination"
```

---

### 2.3 primary_driver

**Type:** string
**Required:** yes
**Description:** The main artifact driver

**Enum:**
- channel_split
- temporal_echo
- scanline_contour_banding
- raster_tear
- compression_chew
- pixel_matrix_visibility
- overprint_stacking
- bloom_contamination
- noise_veil
- text_interface_debris
- capture_degradation
- color_field_collision

**Example:**
```json
"primary_driver": "channel_split"
```

---

### 2.4 secondary_drivers

**Type:** array of strings
**Required:** no
**Description:** Supporting artifact drivers

**Max Items:** 4

**Example:**
```json
"secondary_drivers": [
  "bloom_contamination",
  "overprint_stacking",
  "sparkle_static"
]
```

---

### 2.5 palette_family

**Type:** string
**Required:** no
**Description:** The color palette family

**Enum:**
- phosphor_noir
- hyperpop_rupture
- pastel_signal_melt
- rainbow_channel_hallucination
- toxic_cathode_candy
- gloss_electric_glam
- codec_candy_crash

**Example:**
```json
"palette_family": "hyperpop_rupture"
```

---

### 2.6 palette_structure

**Type:** object
**Required:** no
**Description:** Detailed palette specification

**Properties:**
```json
{
  "dominant_hue_family": "string",
  "collision_hue_family": "string",
  "accent_puncture": "string"
}
```

**Example:**
```json
"palette_structure": {
  "dominant_hue_family": "magenta_hot_pink",
  "collision_hue_family": "cyan_electric_blue",
  "accent_puncture": "sharp_white"
}
```

---

### 2.7 density_level

**Type:** string
**Required:** no
**Description:** Signal density level

**Enum:**
- sparse_signal
- moderate_signal
- dense_signal
- overloaded_signal
- pile_up_delirium

**Example:**
```json
"density_level": "dense_signal"
```

---

### 2.8 emotion_tags

**Type:** array of strings
**Required:** no
**Description:** Emotional descriptors

**Example:**
```json
"emotion_tags": [
  "seductive",
  "emotionally_loud",
  "synthetic_euphoria"
]
```

---

### 2.9 preserved_anchors

**Type:** array of strings
**Required:** no
**Description:** Zones to preserve from corruption

**Example:**
```json
"preserved_anchors": [
  "eyes",
  "lips",
  "face_center"
]
```

---

### 2.10 drift_blockers

**Type:** array of strings
**Required:** no
**Description:** Anti-drift rules to apply

**Example:**
```json
"drift_blockers": [
  "not_clean_editorial",
  "not_simple_rgb_filter",
  "corruption_must_alter_face_planes"
]
```

---

### 2.11 media_source

**Type:** string
**Required:** no
**Description:** Implied media/display source

**Enum:**
- glossy_digital
- screenshot_repost_export_damage
- crt_monitor
- cctv_weak_feed
- terminal_screen
- live_post_process
- multi_pass_live_post_process

**Example:**
```json
"media_source": "glossy_digital"
```

---

### 2.12 audio_mode

**Type:** string
**Required:** no
**Description:** Audio-reactive behavior type

**Enum:**
- spectrum_reactive
- semantic_reactive
- trail_reactive
- compression_reactive
- pulse_reactive
- tear_reactive_subtle

**Example:**
```json
"audio_mode": "spectrum_reactive"
```

---

### 2.13 audio_mapping

**Type:** object
**Required:** no
**Description:** Frequency-to-visual mapping

**Properties:**
```json
{
  "bass": "string",
  "low_mids": "string",
  "high_mids": "string",
  "highs": "string",
  "transients": "string",
  "vocals": "string",
  "amplitude": "string"
}
```

**Example:**
```json
"audio_mapping": {
  "bass": "widen_rgb_offset",
  "low_mids": "increase_duplicate_spacing",
  "high_mids": "enhance_edge_chatter",
  "highs": "fringe_flicker",
  "transients": "channel_snap_jump"
}
```

---

### 2.14 text_behavior

**Type:** object
**Required:** no
**Description:** Text debris configuration

**Properties:**
```json
{
  "text_mode": "string",
  "phrase_density": "string",
  "legibility_level": "string",
  "repetition_intensity": "string",
  "body_text_overlap_bias": "string"
}
```

**Example:**
```json
"text_behavior": {
  "text_mode": "terminal_residue_and_subtitle_ghosting",
  "phrase_density": "moderate",
  "legibility_level": "partial",
  "repetition_intensity": "medium_high",
  "body_text_overlap_bias": "high"
}
```

---

### 2.15 hybrid_type

**Type:** string
**Required:** no (only for hybrids)
**Description:** Type of hybrid combination

**Enum:**
- body_plus_contamination
- palette_plus_failure
- structure_plus_motion
- atmosphere_plus_text

**Example:**
```json
"hybrid_type": "body_plus_contamination"
```

---

### 2.16 notes

**Type:** string
**Required:** no
**Description:** Additional notes for AI interpretation

**Example:**
```json
"notes": "For stage performance, emphasize motion and glamour"
```

---

## 3. Complete Example

```json
{
  "config_id": "cfg_001_candy_broadcast_portrait",
  "subtype": "candy_broadcast_hallucination",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "bloom_contamination",
    "overprint_stacking",
    "sparkle_static"
  ],
  "palette_family": "hyperpop_rupture",
  "palette_structure": {
    "dominant_hue_family": "magenta_hot_pink",
    "collision_hue_family": "cyan_electric_blue",
    "accent_puncture": "sharp_white"
  },
  "density_level": "dense_signal",
  "emotion_tags": [
    "seductive",
    "emotionally_loud",
    "synthetic_euphoria",
    "glamorous_instability"
  ],
  "media_source": "glossy_digital",
  "preserved_anchors": [
    "eyes",
    "lips",
    "central_face_shape"
  ],
  "drift_blockers": [
    "not_clean_editorial",
    "not_simple_rgb_filter",
    "corruption_must_alter_face_planes"
  ],
  "audio_mode": "spectrum_reactive",
  "audio_mapping": {
    "bass": "widen_rgb_offset",
    "low_mids": "increase_duplicate_spacing",
    "high_mids": "enhance_edge_chatter",
    "highs": "fringe_flicker",
    "transients": "channel_snap_jump",
    "vocals": "mouth_and_face_emphasis"
  },
  "notes": "Maintain one pleasure zone and one injury zone"
}
```

---

## 4. Validation Rules

### 4.1 Required Fields

Every config MUST have:
- config_id
- subtype
- primary_driver

### 4.2 Subtype-Driver Compatibility

| Subtype | Valid Primary Drivers |
|---------|----------------------|
| candy_broadcast_hallucination | channel_split, overprint_stacking |
| pastel_identity_smear | overprint_stacking, soft_channel_split |
| rgb_phantom | channel_split |
| ghost_frame_body | temporal_echo |
| text_screen_heartbreak | text_interface_debris |
| crt_contour | scanline_contour_banding |
| candy_crash_compression | compression_chew |
| surveillance_apparition | capture_degradation |
| glitter_signal_overprint | overprint_stacking |
| composite_fever_dream | any |

### 4.3 Palette-Subtype Compatibility

| Subtype | Recommended Palettes |
|---------|---------------------|
| candy_broadcast_hallucination | hyperpop_rupture, gloss_electric_glam |
| pastel_identity_smear | pastel_signal_melt, gloss_electric_glam |
| rgb_phantom | rainbow_channel_hallucination, hyperpop_rupture |
| ghost_frame_body | gloss_electric_glam, rainbow_channel_hallucination |
| text_screen_heartbreak | gloss_electric_glam, codec_candy_crash |
| crt_contour | phosphor_noir, toxic_cathode_candy |
| candy_crash_compression | codec_candy_crash, hyperpop_rupture |
| surveillance_apparition | phosphor_noir |
| glitter_signal_overprint | gloss_electric_glam, hyperpop_rupture |
| composite_fever_dream | any |

---

## 5. Type Definitions

### 5.1 Subtype Enum

```json
{
  "subtype": {
    "type": "string",
    "enum": [
      "candy_broadcast_hallucination",
      "pastel_identity_smear",
      "rgb_phantom",
      "composite_fever_dream",
      "crt_contour",
      "ghost_frame_body",
      "raster_meltdown",
      "pixel_ghost",
      "text_screen_heartbreak",
      "surveillance_apparition",
      "candy_crash_compression",
      "glitter_signal_overprint"
    ]
  }
}
```

### 5.2 Driver Enum

```json
{
  "driver": {
    "type": "string",
    "enum": [
      "channel_split",
      "temporal_echo",
      "scanline_contour_banding",
      "raster_tear",
      "compression_chew",
      "pixel_matrix_visibility",
      "overprint_stacking",
      "bloom_contamination",
      "noise_veil",
      "text_interface_debris",
      "capture_degradation",
      "color_field_collision",
      "sparkle_static",
      "phase_lag_duplication",
      "edge_emphasis",
      "macroblock_breakup",
      "chroma_smear",
      "quantization_banding",
      "subtitle_ghosting"
    ]
  }
}
```

### 5.3 Palette Enum

```json
{
  "palette": {
    "type": "string",
    "enum": [
      "phosphor_noir",
      "hyperpop_rupture",
      "pastel_signal_melt",
      "rainbow_channel_hallucination",
      "toxic_cathode_candy",
      "gloss_electric_glam",
      "codec_candy_crash"
    ]
  }
}
```

### 5.4 Density Enum

```json
{
  "density": {
    "type": "string",
    "enum": [
      "sparse_signal",
      "moderate_signal",
      "dense_signal",
      "overloaded_signal",
      "pile_up_delirium"
    ]
  }
}
```

---

## 6. Implementation Notes

### 6.1 For JSON Validators

Use this schema to validate config files before processing.

### 6.2 For App Developers

- Use enum values for dropdown menus
- Validate configs on import
- Provide helpful error messages
- Suggest fixes for invalid configs

### 6.3 For AI Systems

- Parse config_id for categorization
- Use subtype to determine base behavior
- Apply primary_driver at specified strength
- Add secondary_drivers at reduced strength
- Follow palette_structure for color logic
- Respect density_level for corruption amount
- Preserve preserved_anchors
- Apply drift_blockers as constraints

---

## 7. Summary

The JSON schema provides:
- Formal structure for configs
- Validation rules
- Type definitions
- Implementation guidance

Use this schema to ensure all glitchcore configs are valid and interoperable.

---

## 8. Short Anchor Rule

Structure enables creativity without chaos.
