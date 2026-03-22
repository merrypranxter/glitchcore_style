# Preset Library

Ready-to-use glitchcore configurations for common use cases.

## Purpose

This file provides a library of pre-configured glitchcore presets that users can select and apply immediately.

Each preset includes:
- Subtype configuration
- Driver settings
- Palette specification
- Density level
- Emotional tags
- Best use cases
- Anti-drift notes

---

## 1. Quick Preset Index

| Preset | Subtype | Mood | Best For |
|--------|---------|------|----------|
| Candy Angel | Candy Broadcast | Seductive, loud | Beauty portraits |
| Soft Dream | Pastel Smear | Dreamy, romantic | Soft portraits |
| Electric Ghost | RGB Phantom | Electric, unstable | Profile shots |
| Motion Memory | Ghost-Frame | Kinetic, haunted | Dance/movement |
| Terminal Confession | Text-Screen | Lonely, confessional | Emotional text |
| Signal Saint | CRT Contour | Iconic, ceremonial | Strong silhouettes |
| Internet Broken | Candy-Crash | Bratty, broken | Screenshot aesthetic |
| Diva Glitter | Glitter-Signal | Glamorous, radiant | Glam shots |
| Fever Dream | Composite | Decadent, overloaded | Maximal art |
| Watched | Surveillance | Cold, institutional | Monitored figures |

---

## 2. Full Preset Configurations

### 2.1 Candy Angel

**Preset ID:** `preset_candy_angel`

**Configuration:**
```json
{
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
  "preserved_anchors": [
    "eyes",
    "lips",
    "face_center"
  ],
  "drift_blockers": [
    "not_clean_editorial",
    "not_simple_rgb_filter",
    "corruption_must_alter_face_planes"
  ],
  "best_subjects": [
    "beauty_closeup",
    "glam_portrait",
    "diva_icon_face"
  ],
  "intensity": "high",
  "color_temperature": "hot",
  "surface_feel": "glossy_digital"
}
```

**Prompt Template:**
```
A beauty close-up treated as a candy broadcast hallucination, with channel split as the main transformation logic, supported by bloom contamination, overprint stacking, and sparkle static, using a hyperpop rupture palette with dominant magenta and hot pink, cyan as collision hue, and sharp white flare accents, at dense signal density, creating a mood of seductive emotional loudness and synthetic euphoria, with glossy digital surface feel, while preserving the eyes, lips, and face center, not a clean fashion editorial or simple RGB filter effect.
```

---

### 2.2 Soft Dream

**Preset ID:** `preset_soft_dream`

**Configuration:**
```json
{
  "subtype": "pastel_identity_smear",
  "primary_driver": "overprint_stacking",
  "secondary_drivers": [
    "soft_channel_split",
    "bloom_contamination",
    "gentle_temporal_echo"
  ],
  "palette_family": "pastel_signal_melt",
  "palette_structure": {
    "dominant_hue_family": "cotton_candy_pink",
    "collision_hue_family": "lavender_baby_blue",
    "accent_puncture": "pearl_white"
  },
  "density_level": "moderate_signal",
  "emotion_tags": [
    "dreamy",
    "romantic",
    "fragile",
    "dissociative",
    "chemically_tender"
  ],
  "preserved_anchors": [
    "eyes",
    "lips",
    "nose_bridge"
  ],
  "drift_blockers": [
    "not_generic_dream_filter",
    "must_repeat_or_destabilize_features",
    "not_beauty_ad_polish"
  ],
  "best_subjects": [
    "soft_portrait",
    "romantic_closeup",
    "dreamy_self_image"
  ],
  "intensity": "medium",
  "color_temperature": "soft",
  "surface_feel": "velvety_cosmetic"
}
```

**Prompt Template:**
```
A frontal face portrait rendered as a pastel identity smear, with overprint stacking as the main transformation logic, supported by soft channel split, creamy bloom contamination, and gentle temporal echo, using a pastel signal melt palette with dominant cotton-candy pink, lavender as collision hue, and pearl-white accent punctures, at moderate signal density, creating a dreamy, romantic, fragile mood, with velvety cosmetic surface feel, while preserving the eyes, lips, and nose bridge, not a generic dreamy filter or polished beauty ad.
```

---

### 2.3 Electric Ghost

**Preset ID:** `preset_electric_ghost`

**Configuration:**
```json
{
  "subtype": "rgb_phantom",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "phase_lag_duplication",
    "edge_emphasis",
    "soft_bloom"
  ],
  "palette_family": "rainbow_channel_hallucination",
  "palette_structure": {
    "dominant_hue_family": "cyan_magenta",
    "collision_hue_family": "green_spectral_intrusion",
    "accent_puncture": "white_edge_flare"
  },
  "density_level": "moderate_signal",
  "emotion_tags": [
    "electric",
    "unstable",
    "spectral",
    "synthetic_intimate"
  ],
  "preserved_anchors": [
    "profile_line",
    "eye_socket_shape",
    "mouth_line"
  ],
  "drift_blockers": [
    "not_basic_chromatic_aberration",
    "must_affect_body_perception",
    "not_all_hues_equal_strength"
  ],
  "best_subjects": [
    "profile_portrait",
    "confrontational_face",
    "chromatic_ghost_figure"
  ],
  "intensity": "medium_high",
  "color_temperature": "electric",
  "surface_feel": "prismatic_glow"
}
```

**Prompt Template:**
```
A profile portrait built as an RGB phantom, with channel split as the lead driver and phase-lag duplication as support, using a rainbow channel hallucination palette with cyan-magenta dominance and green spectral intrusion, white edge flare accents, at moderate signal density, creating an electric, unstable, spectral mood, with prismatic glow surface feel, while preserving the profile line and eye socket shape, not simple chromatic aberration pasted over a normal image.
```

---

### 2.4 Motion Memory

**Preset ID:** `preset_motion_memory`

**Configuration:**
```json
{
  "subtype": "ghost_frame_body",
  "primary_driver": "temporal_echo",
  "secondary_drivers": [
    "multi_exposure_stack",
    "soft_channel_split",
    "bloom_trail_haze"
  ],
  "palette_family": "gloss_electric_glam",
  "palette_structure": {
    "dominant_hue_family": "glossy_pink",
    "collision_hue_family": "electric_blue_violet",
    "accent_puncture": "white_halo"
  },
  "density_level": "dense_signal",
  "emotion_tags": [
    "ecstatic",
    "kinetic",
    "sensual",
    "haunted",
    "ritualistic"
  ],
  "preserved_anchors": [
    "dominant_body_pose",
    "face_angle",
    "gesture_arc"
  ],
  "drift_blockers": [
    "not_generic_motion_blur",
    "not_equal_opacity_trail_stack",
    "preserve_one_present_body"
  ],
  "best_subjects": [
    "dancer",
    "moving_body",
    "gesture_study"
  ],
  "intensity": "high",
  "color_temperature": "warm",
  "surface_feel": "glossy_trail_residue"
}
```

**Prompt Template:**
```
A moving glam figure treated as a ghost-frame body image, driven by temporal echo and multi-exposure stacking, supported by soft RGB lag and bloom-heavy trail haze, using a gloss-electric glam palette with glossy pink dominance, electric blue-violet collision, and white halo accents, at dense signal density, creating an ecstatic, kinetic, haunted mood, with glossy trail residue surface feel, while preserving the dominant body pose and gesture arc, not ordinary motion blur.
```

---

### 2.5 Terminal Confession

**Preset ID:** `preset_terminal_confession`

**Configuration:**
```json
{
  "subtype": "text_screen_heartbreak",
  "primary_driver": "text_interface_debris",
  "secondary_drivers": [
    "subtitle_ghosting",
    "overprint_stacking",
    "compression_haze"
  ],
  "palette_family": "gloss_electric_glam",
  "palette_structure": {
    "dominant_hue_family": "magenta_pearl_white",
    "collision_hue_family": "cyan",
    "accent_puncture": "white_terminal_glow"
  },
  "density_level": "dense_signal",
  "emotion_tags": [
    "confessional",
    "lonely",
    "obsessive",
    "internet_broken",
    "mediated_tenderness"
  ],
  "preserved_anchors": [
    "eyes",
    "one_readable_phrase",
    "face_center"
  ],
  "drift_blockers": [
    "not_poster_design",
    "not_polished_ui_mockup",
    "text_must_behave_like_debris"
  ],
  "best_subjects": [
    "lonely_portrait",
    "confessional_moment",
    "digital_romance"
  ],
  "intensity": "high",
  "color_temperature": "cool_warm",
  "surface_feel": "glowing_chat_window"
}
```

**Prompt Template:**
```
A lonely bust portrait approached as text-screen heartbreak, with text interface debris as the primary driver, supported by subtitle ghosting, compression haze, and low-opacity overprint copies, using gloss-electric glam color with magenta, pearl white, and cyan contamination, at dense signal density, creating a confessional, obsessive, internet-broken mood, rendered like a glowing chat window with lipstick-soft bloom and dead notification residue, while preserving the face and one readable repeated phrase, not poster design or polished UI mockup.
```

---

### 2.6 Signal Saint

**Preset ID:** `preset_signal_saint`

**Configuration:**
```json
{
  "subtype": "crt_contour",
  "primary_driver": "scanline_contour_banding",
  "secondary_drivers": [
    "phosphor_bloom",
    "faint_static_veil",
    "subtle_capture_degradation"
  ],
  "palette_family": "phosphor_noir",
  "palette_structure": {
    "dominant_hue_family": "cyan_teal",
    "collision_hue_family": "ice_blue",
    "accent_puncture": "warning_red_small"
  },
  "density_level": "sparse_signal",
  "emotion_tags": [
    "remote",
    "iconic",
    "ceremonial",
    "eerie",
    "sacred_machine"
  ],
  "preserved_anchors": [
    "profile_line",
    "head_shape",
    "shoulder_contour"
  ],
  "drift_blockers": [
    "not_op_art_poster",
    "not_generic_scanline_overlay",
    "black_cannot_replace_visual_interest"
  ],
  "best_subjects": [
    "bust_portrait",
    "strong_silhouette",
    "signal_statue"
  ],
  "intensity": "low_medium",
  "color_temperature": "cold",
  "surface_feel": "crt_phosphor"
}
```

**Prompt Template:**
```
A bust portrait treated as CRT contour, with scanline contour banding as the main driver, supported by phosphor bloom, faint static veil, and subtle capture degradation, using a phosphor noir palette with cyan-teal dominance, ice blue collision, and small warning red accent punctures, at sparse signal density, creating a remote, iconic, ceremonial mood, with CRT phosphor surface feel, while preserving the profile line and head shape, not op art poster or generic scanline overlay.
```

---

### 2.7 Internet Broken

**Preset ID:** `preset_internet_broken`

**Configuration:**
```json
{
  "subtype": "candy_crash_compression",
  "primary_driver": "compression_chew",
  "secondary_drivers": [
    "macroblock_breakup",
    "chroma_smear",
    "quantization_banding",
    "light_text_residue"
  ],
  "palette_family": "codec_candy_crash",
  "palette_structure": {
    "dominant_hue_family": "magenta",
    "collision_hue_family": "flat_cyan_violet",
    "accent_puncture": "harsh_white"
  },
  "density_level": "overloaded_signal",
  "emotion_tags": [
    "bratty",
    "internet_broken",
    "cheap_beautiful",
    "synthetic",
    "overprocessed"
  ],
  "preserved_anchors": [
    "mouth",
    "lashes",
    "head_silhouette"
  ],
  "drift_blockers": [
    "not_generic_low_quality",
    "preserve_one_hot_beauty_zone",
    "colors_must_break_clearly_not_die_muddy"
  ],
  "best_subjects": [
    "pop_portrait",
    "screenshot_aesthetic",
    "upload_damaged_identity"
  ],
  "intensity": "very_high",
  "color_temperature": "hot_broken",
  "surface_feel": "recompression_mush"
}
```

**Prompt Template:**
```
A glossy pop portrait treated as candy-crash compression, driven by compression chew with visible macroblock breakup, chroma smear, and quantization banding, supported by light text residue, using a codec candy crash palette with dominant magenta, flat cyan-violet collision, and harsh white punctures, at overloaded signal density, creating a bratty, internet-bruised, cheap-beautiful emotional tone, with dead-soft recompression mush and buzzing artifact halos, while preserving the mouth, lashes, and face silhouette, not merely a low-quality image or retro export effect.
```

---

### 2.8 Diva Glitter

**Preset ID:** `preset_diva_glitter`

**Configuration:**
```json
{
  "subtype": "glitter_signal_overprint",
  "primary_driver": "overprint_stacking",
  "secondary_drivers": [
    "bloom_contamination",
    "soft_channel_split",
    "sparkle_static"
  ],
  "palette_family": "gloss_electric_glam",
  "palette_structure": {
    "dominant_hue_family": "glossy_pink_pearl",
    "collision_hue_family": "cool_violet_cyan",
    "accent_puncture": "white_silver_glint"
  },
  "density_level": "dense_signal",
  "emotion_tags": [
    "glamorous",
    "coquettish",
    "radiant",
    "unstable",
    "emotionally_overdressed"
  ],
  "preserved_anchors": [
    "eyes",
    "cheekbones",
    "lips"
  ],
  "drift_blockers": [
    "not_clean_beauty_ad",
    "not_glitter_overlay_only",
    "one_rude_corruption_zone_required"
  ],
  "best_subjects": [
    "glam_portrait",
    "diva_coded_image",
    "icon_like_face"
  ],
  "intensity": "high",
  "color_temperature": "warm_glossy",
  "surface_feel": "sparkly_overlit_digital"
}
```

**Prompt Template:**
```
A glossy diva portrait treated as glitter-signal overprint, with overprint stacking as the primary driver, supported by bloom contamination, soft channel split, and sparkle static, using a gloss-electric glam palette with glossy pink-pearl dominance, cool violet-cyan collision, and white-silver glint accents, at dense signal density, creating a glamorous, coquettish, radiant mood, with sparkly overlit digital surface feel, while preserving the eyes, cheekbones, and lips, not a clean beauty ad or glitter overlay only.
```

---

### 2.9 Fever Dream

**Preset ID:** `preset_fever_dream`

**Configuration:**
```json
{
  "subtype": "composite_fever_dream",
  "primary_driver": "overprint_stacking",
  "secondary_drivers": [
    "channel_split",
    "bloom_contamination",
    "compression_trace",
    "text_interface_debris",
    "temporal_haze"
  ],
  "palette_family": "rainbow_channel_hallucination",
  "palette_structure": {
    "dominant_hue_family": "magenta_cyan",
    "collision_hue_family": "green_violet",
    "accent_puncture": "white_and_yellow"
  },
  "density_level": "pile_up_delirium",
  "emotion_tags": [
    "decadent",
    "feverish",
    "beautiful_malfunction",
    "overloaded",
    "glamorous_instability"
  ],
  "preserved_anchors": [
    "one_eye_region",
    "mouth",
    "one_readable_phrase"
  ],
  "drift_blockers": [
    "not_random_effect_soup",
    "one_anchor_must_survive",
    "one_driver_must_still_read_as_primary"
  ],
  "best_subjects": [
    "maximal_portrait",
    "cover_art_type",
    "emotional_pile_up"
  ],
  "intensity": "maximum",
  "color_temperature": "full_spectrum",
  "surface_feel": "multi_pass_live_post_process"
}
```

**Prompt Template:**
```
A maximal portrait treated as composite fever dream, with overprint stacking as the primary driver, supported by channel split, bloom contamination, compression trace, text interface debris, and temporal haze, using a rainbow channel hallucination palette with magenta-cyan dominance, green-violet collision, and white-yellow accents, at pile-up delirium density, creating a decadent, feverish, beautiful malfunction mood, with multi-pass live post-process surface feel, while preserving one eye region, mouth, and one readable phrase, not random effect soup.
```

---

### 2.10 Watched

**Preset ID:** `preset_watched`

**Configuration:**
```json
{
  "subtype": "surveillance_apparition",
  "primary_driver": "capture_degradation",
  "secondary_drivers": [
    "noise_veil",
    "pixel_matrix_visibility",
    "weak_interface_trace"
  ],
  "palette_family": "phosphor_noir",
  "palette_structure": {
    "dominant_hue_family": "cold_cyan_green",
    "collision_hue_family": "minimal_gray_blue",
    "accent_puncture": "dim_white"
  },
  "density_level": "moderate_signal",
  "emotion_tags": [
    "watched",
    "depersonalized",
    "eerie",
    "institutional",
    "detached"
  ],
  "preserved_anchors": [
    "silhouette",
    "figure_position",
    "coarse_head_shape"
  ],
  "drift_blockers": [
    "not_generic_analog_horror",
    "not_cinematic_movie_still",
    "not_too_polished"
  ],
  "best_subjects": [
    "standing_figure",
    "hallway_scene",
    "depersonalized_portrait"
  ],
  "intensity": "medium",
  "color_temperature": "cold",
  "surface_feel": "weak_cctv_feed"
}
```

**Prompt Template:**
```
A solitary standing figure treated as surveillance apparition, with capture degradation as the primary driver, supported by noise veil, pixel matrix visibility, and weak interface trace, using a phosphor noir palette with cold cyan-green dominance, minimal gray-blue collision, and dim white accent punctures, at moderate signal density, creating a watched, depersonalized, institutional mood, with weak CCTV feed surface feel, while preserving the silhouette and figure position, not generic analog horror or cinematic movie still.
```

---

## 3. Preset Usage Guide

### 3.1 Selecting a Preset

1. **Identify your subject:** Portrait, landscape, movement, text-heavy?
2. **Identify your mood:** Seductive, dreamy, lonely, electric, cold?
3. **Match to preset:** Use the Quick Index table
4. **Apply and adjust:** Use as-is or modify intensity

### 3.2 Customizing a Preset

All presets can be modified:
- **Intensity slider:** Adjust density level
- **Color picker:** Modify palette hues
- **Driver toggles:** Add/remove secondary drivers
- **Anchor map:** Change protected zones

### 3.3 Creating New Presets

1. Start with closest existing preset
2. Modify parameters
3. Save with new name
4. Add tags for discovery

---

## 4. Summary

The preset library provides:
- 10 ready-to-use configurations
- Full JSON specifications
- Prompt templates
- Usage guidance
- Customization paths

Start with a preset, then make it yours.

---

## 5. Short Anchor Rule

Presets are starting points, not prisons.
