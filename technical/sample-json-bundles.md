# Sample JSON Bundles

Filled-out example records for glitchcore branches, hybrids, presets, audio-reactive behavior, anchor protection, and app-ready style configs.

## Purpose

This file provides concrete example JSON objects based on the schema and logic system already defined in the repo.

This is the part that helps the app stop going:
"cool theory bro"
and start going:
"ah, I can actually use this."

These records are meant to show how the system can represent:
- subtype configs
- preset configs
- hybrid configs
- audio-reactive configs
- text-heavy configs
- compression-heavy configs
- shader behavior packs
- drift blockers
- preserved anchors

These are example structures, not the only valid format.
They're here to make implementation easier, clearer, and less cursed.

---

## 1. Minimal Single-Image Config Example

```json
{
  "config_id": "cfg_001_candy_broadcast_portrait",
  "subtype": "candy_broadcast_hallucination",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "bloom_contamination",
    "overprint_stacking",
    "color_field_collision"
  ],
  "palette_family": "hyperpop_rupture",
  "palette_structure": {
    "dominant_hue_family": "hot_pink_magenta",
    "collision_hue_family": "cyan_electric_blue",
    "accent_puncture": "white_flare"
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
  ]
}
```

---

## 2. Candy Broadcast Preset Bundle

```json
{
  "config_id": "preset_candy_angel_breakdown",
  "preset_name": "Candy Angel Breakdown",
  "primary_branch": "candy_broadcast_hallucination",
  "secondary_branch": "glitter_signal_overprint",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "bloom_contamination",
    "overprint_stacking",
    "sparkle_static"
  ],
  "palette_family": "hyperpop_rupture",
  "palette_structure": {
    "dominant_hue_family": "magenta_hot_pink",
    "collision_hue_family": "cyan_violet",
    "accent_puncture": "sharp_white"
  },
  "density_default": "dense_signal",
  "emotion_tags": [
    "seductive",
    "synthetic",
    "sugary_heartbreak",
    "coquettish",
    "overstimulating"
  ],
  "best_subjects": [
    "beauty_closeup",
    "glam_portrait",
    "diva_icon_face"
  ],
  "preserved_anchor_bias": [
    "eyes",
    "lips",
    "face_center"
  ],
  "drift_risks": [
    "beauty_ad_drift",
    "empty_hyperpop_editorial",
    "rainbow_clown_soup"
  ],
  "hidden_ai_notes": [
    "maintain one pleasure zone and one injury zone",
    "protect face center slightly more than outer planes",
    "let bloom feel cosmetic not generic"
  ]
}
```

---

## 3. Pastel Identity Smear Config

```json
{
  "config_id": "cfg_003_pastel_identity_smear",
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
    "fragile",
    "dissociative",
    "romantic",
    "chemically_tender"
  ],
  "media_source": "glossy_cosmetic_digital",
  "preserved_anchors": [
    "both_eyes",
    "lips",
    "nose_bridge"
  ],
  "drift_blockers": [
    "not_generic_dream_filter",
    "must_repeat_or_destabilize_features",
    "not_beauty_ad_polish"
  ]
}
```

---

## 4. RGB Phantom Audio-Reactive Config

```json
{
  "config_id": "cfg_004_rgb_phantom_audio",
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
  "media_source": "live_post_process",
  "preserved_anchors": [
    "profile_line",
    "eye_socket_shape",
    "mouth_line"
  ],
  "audio_mode": "spectrum_reactive",
  "audio_mapping": {
    "bass": "widen_rgb_offset",
    "low_mids": "increase_phase_lag",
    "high_mids": "enhance_edge_chatter",
    "highs": "fringe_flicker",
    "transients": "channel_snap_jump"
  },
  "drift_blockers": [
    "not_basic_chromatic_aberration",
    "must_affect_body_perception",
    "not_all_hues_equal_strength"
  ]
}
```

---

## 5. Ghost-Frame Dance Config

```json
{
  "config_id": "cfg_005_ghost_frame_dancer",
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
  "media_source": "live_video_feedback",
  "preserved_anchors": [
    "dominant_body_pose",
    "face_angle",
    "gesture_arc"
  ],
  "audio_mode": "trail_reactive",
  "audio_mapping": {
    "beat": "reinforce_current_frame",
    "low_mids": "increase_echo_count",
    "pads": "increase_trail_persistence",
    "transients": "add_stutter_copy",
    "amplitude": "increase_trail_brightness"
  },
  "drift_blockers": [
    "not_generic_motion_blur",
    "not_equal_opacity_trail_stack",
    "preserve_one_present_body"
  ]
}
```

---

## 6. Candy-Crash Compression Config

```json
{
  "config_id": "cfg_006_bratty_file_damage",
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
  "media_source": "screenshot_repost_export_damage",
  "preserved_anchors": [
    "mouth",
    "lashes",
    "head_silhouette"
  ],
  "audio_mode": "compression_reactive",
  "audio_mapping": {
    "bass": "increase_block_size",
    "transients": "packet_loss_puncture",
    "high_mids": "edge_buzz_and_chroma_damage",
    "vocals": "face_zone_smear",
    "amplitude": "global_compression_pressure"
  },
  "drift_blockers": [
    "not_generic_low_quality",
    "preserve_one_hot_beauty_zone",
    "colors_must_break_clearly_not_die_muddy"
  ]
}
```

---

## 7. Text-Screen Heartbreak Config

```json
{
  "config_id": "cfg_007_terminal_confession",
  "subtype": "text_screen_heartbreak",
  "primary_driver": "text_interface_debris",
  "secondary_drivers": [
    "subtitle_ghosting",
    "overprint_stacking",
    "compression_haze",
    "soft_bloom"
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
  "media_source": "terminal_plus_screenshot_hybrid",
  "text_behavior": {
    "text_mode": "terminal_residue_and_subtitle_ghosting",
    "phrase_density": "moderate",
    "legibility_level": "partial",
    "repetition_intensity": "medium_high",
    "body_text_overlap_bias": "high"
  },
  "preserved_anchors": [
    "eyes",
    "one_readable_phrase",
    "face_center"
  ],
  "audio_mode": "semantic_reactive",
  "audio_mapping": {
    "vocals": "emit_phrase_fragments",
    "high_mids": "increase_text_clarity",
    "beat": "text_flicker_stutter",
    "silence": "linger_ghost_text",
    "amplitude": "phrase_density"
  },
  "drift_blockers": [
    "not_poster_design",
    "not_polished_ui_mockup",
    "text_must_behave_like_debris"
  ]
}
```

---

## 8. CRT Contour Config

```json
{
  "config_id": "cfg_008_signal_saint",
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
  "media_source": "crt_monitor",
  "preserved_anchors": [
    "profile_line",
    "head_shape",
    "shoulder_contour"
  ],
  "audio_mode": "pulse_reactive",
  "audio_mapping": {
    "bass": "contour_thickness",
    "highs": "scanline_shimmer",
    "sustained_tones": "halo_build",
    "transients": "row_jitter",
    "vocals": "face_contour_emphasis"
  },
  "drift_blockers": [
    "not_op_art_poster",
    "not_generic_scanline_overlay",
    "black_cannot_replace_visual_interest"
  ]
}
```

---

## 9. Surveillance Apparition Config

```json
{
  "config_id": "cfg_009_monitored_ghost",
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
  "media_source": "cctv_weak_feed",
  "preserved_anchors": [
    "silhouette",
    "figure_position",
    "coarse_head_shape"
  ],
  "audio_mode": "tear_reactive_subtle",
  "audio_mapping": {
    "low_bass": "feed_roll",
    "highs": "hiss_static",
    "transients": "glitch_flash",
    "speech": "monitor_focus_shift",
    "silence": "weak_feed_stillness"
  },
  "drift_blockers": [
    "not_generic_analog_horror",
    "not_cinematic_movie_still",
    "not_too_polished"
  ]
}
```

---

## 10. Glitter-Signal Overprint Config

```json
{
  "config_id": "cfg_010_gloss_disaster_icon",
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
  "media_source": "glossy_overlit_digital",
  "preserved_anchors": [
    "eyes",
    "cheekbones",
    "lips"
  ],
  "audio_mode": "pulse_reactive",
  "audio_mapping": {
    "highs": "sparkle_density",
    "vocals": "gloss_bloom",
    "bass": "duplicate_drift",
    "chorus": "overprint_expansion",
    "sustained_harmonics": "halo_growth"
  },
  "drift_blockers": [
    "not_clean_beauty_ad",
    "not_glitter_overlay_only",
    "one_rude_corruption_zone_required"
  ]
}
```

---

## 11. Hybrid Example — Dream Diary Face

```json
{
  "config_id": "hybrid_011_dream_diary_face",
  "primary_branch": "pastel_identity_smear",
  "secondary_branch": "text_screen_heartbreak",
  "hybrid_type": "body_plus_contamination",
  "primary_driver": "overprint_stacking",
  "secondary_drivers": [
    "subtitle_ghosting",
    "soft_bloom",
    "interface_debris"
  ],
  "palette_family": "pastel_signal_melt",
  "palette_structure": {
    "dominant_hue_family": "pastel_pink",
    "collision_hue_family": "lavender_baby_blue",
    "accent_puncture": "pearl_white"
  },
  "density_level": "moderate_signal",
  "emotion_tags": [
    "dreamy",
    "lonely",
    "confessional",
    "romantic",
    "fragile"
  ],
  "media_source": "soft_chat_window_digital",
  "preserved_anchors": [
    "eyes",
    "lips",
    "one_readable_phrase"
  ],
  "drift_blockers": [
    "not_beauty_ad_polish",
    "not_poster_layout",
    "text_must_feel_like_leakage"
  ],
  "ai_notes": [
    "body logic leads",
    "text remains secondary but emotionally important",
    "preserve repeated feature instability"
  ]
}
```

---

## 12. Hybrid Example — Internet Pop Disaster Angel

```json
{
  "config_id": "hybrid_012_internet_pop_disaster_angel",
  "primary_branch": "candy_broadcast_hallucination",
  "secondary_branch": "candy_crash_compression",
  "hybrid_type": "palette_plus_failure",
  "primary_driver": "channel_split",
  "secondary_drivers": [
    "compression_chew",
    "bloom_contamination",
    "chroma_smear",
    "macroblock_breakup"
  ],
  "palette_family": "codec_candy_crash",
  "palette_structure": {
    "dominant_hue_family": "magenta_hot_pink",
    "collision_hue_family": "cyan_electric_blue",
    "accent_puncture": "white_and_lime"
  },
  "density_level": "overloaded_signal",
  "emotion_tags": [
    "bratty",
    "glamorous",
    "overprocessed",
    "emotionally_loud",
    "internet_broken"
  ],
  "media_source": "reposted_screenshot_damage",
  "preserved_anchors": [
    "mouth",
    "one_eye",
    "face_silhouette"
  ],
  "drift_blockers": [
    "not_generic_hyperpop_editorial",
    "not_bad_quality_for_its_own_sake",
    "beauty_vs_damage_tension_required"
  ]
}
```

---

## 13. Hybrid Example — Ritual Signal Saint

```json
{
  "config_id": "hybrid_013_ritual_signal_saint",
  "primary_branch": "crt_contour",
  "secondary_branch": "ghost_frame_body",
  "hybrid_type": "structure_plus_motion",
  "primary_driver": "scanline_contour_banding",
  "secondary_drivers": [
    "temporal_echo",
    "phosphor_bloom",
    "faint_static_veil"
  ],
  "palette_family": "phosphor_noir",
  "palette_structure": {
    "dominant_hue_family": "teal_cyan",
    "collision_hue_family": "ice_blue",
    "accent_puncture": "small_red_warning"
  },
  "density_level": "moderate_signal",
  "emotion_tags": [
    "ceremonial",
    "haunted",
    "remote",
    "ritualistic",
    "iconic"
  ],
  "media_source": "crt_feedback_halo",
  "preserved_anchors": [
    "silhouette",
    "profile_line",
    "dominant_current_pose"
  ],
  "drift_blockers": [
    "not_op_art_wallpaper",
    "not_generic_motion_blur",
    "not_dead_monitor_jail"
  ]
}
```

---

## 14. Hybrid Example — Diva Signal Relic

```json
{
  "config_id": "hybrid_014_diva_signal_relic",
  "primary_branch": "glitter_signal_overprint",
  "secondary_branch": "rgb_phantom",
  "hybrid_type": "structure_plus_atmosphere",
  "primary_driver": "overprint_stacking",
  "secondary_drivers": [
    "soft_channel_split",
    "bloom_contamination",
    "sparkle_static"
  ],
  "palette_family": "gloss_electric_glam",
  "palette_structure": {
    "dominant_hue_family": "glossy_hot_pink",
    "collision_hue_family": "cool_violet_cyan",
    "accent_puncture": "white_silver"
  },
  "density_level": "dense_signal",
  "emotion_tags": [
    "glamorous",
    "radiant",
    "unstable",
    "iconic",
    "coquettish"
  ],
  "media_source": "overlit_signal_icon",
  "preserved_anchors": [
    "eyes",
    "cheekbones",
    "mouth"
  ],
  "drift_blockers": [
    "not_clean_beauty_editorial",
    "not_decorative_glitter_only",
    "must_preserve_real_instability"
  ]
}
```

---

## 15. Audio-Mode Profile Example — Hyperpop Rupture Mode

```json
{
  "audio_profile_id": "music_mode_hyperpop_rupture",
  "name": "Hyperpop Rupture Mode",
  "best_for": [
    "candy_broadcast_hallucination",
    "rgb_phantom",
    "glitter_signal_overprint",
    "candy_crash_compression"
  ],
  "audio_mode": "spectrum_reactive",
  "behavior_bias": {
    "channel_split": "high",
    "bloom_contamination": "high",
    "color_field_collision": "medium_high",
    "compression_chew": "medium",
    "text_interface_debris": "low_to_medium"
  },
  "audio_mapping": {
    "bass": "widen_structural_distortion",
    "low_mids": "increase_duplicate_spacing",
    "high_mids": "edge_activity_and_face_glow",
    "highs": "sparkle_static_and_fringe_chatter",
    "transients": "rupture_pops",
    "vocals": "mouth_and_face_emphasis"
  },
  "state_switch_rules": {
    "chorus": "increase_density",
    "drop": "brief_overdrive_then_recover",
    "verse": "preserve_anchor_clarity"
  },
  "drift_blockers": [
    "not_rainbow_clown_soup",
    "not_generic_music_visualizer",
    "maintain_palette_hierarchy"
  ]
}
```

---

## 16. Audio-Mode Profile Example — Spoken Confession Mode

```json
{
  "audio_profile_id": "music_mode_spoken_confession",
  "name": "Spoken Confession Mode",
  "best_for": [
    "text_screen_heartbreak",
    "soft_internet_heartbreak",
    "terminal_confession"
  ],
  "audio_mode": "semantic_reactive",
  "behavior_bias": {
    "text_interface_debris": "high",
    "subtitle_ghosting": "high",
    "overprint_stacking": "medium",
    "compression_haze": "medium_low",
    "bloom_contamination": "medium"
  },
  "audio_mapping": {
    "speech_presence": "emit_phrase_fragments",
    "high_mids": "increase_legibility",
    "silence": "leave_text_ghosts",
    "amplitude": "adjust_phrase_density",
    "emotional_peaks": "increase_face_text_overlap"
  },
  "state_switch_rules": {
    "whispery_sections": "lower_density_raise_intimacy",
    "louder_sections": "increase_text_pressure",
    "pause": "linger_phrase_residue"
  },
  "drift_blockers": [
    "not_quote_poster",
    "not_ui_mockup",
    "text_must_feel_found_or_leaked"
  ]
}
```

---

## 17. Shader Bundle Example — Candy Broadcast Core

```json
{
  "shader_bundle_id": "shader_preset_candy_broadcast_core",
  "subtype_alignment": "candy_broadcast_hallucination",
  "lead_shader_family": "channel_displacement",
  "support_shader_families": [
    "bloom_halation",
    "overprint_layers",
    "color_collision"
  ],
  "optional_trace_families": [
    "temporal_feedback_light",
    "sparkle_static"
  ],
  "default_pass_order": [
    "source_input",
    "rgb_displacement",
    "overprint_duplicate_pass",
    "bloom_pass",
    "palette_collision_pass",
    "sparkle_trace_pass",
    "anchor_restore_composite"
  ],
  "anchor_rules": {
    "preserve": [
      "eyes",
      "lips",
      "face_silhouette"
    ],
    "injure_first": [
      "outer_face_planes",
      "hair_edges",
      "duplicate_layers"
    ]
  },
  "density_default": "dense_signal",
  "audio_mode_default": "spectrum_reactive",
  "drift_blockers": [
    "not_clean_editorial",
    "not_simple_rgb_outline_effect"
  ]
}
```

---

## 18. Region Priority Example

```json
{
  "region_profile_id": "region_priority_candy_broadcast_face",
  "subtype": "candy_broadcast_hallucination",
  "priority_zones": {
    "preserve_high": [
      "eyes",
      "mouth",
      "nose_bridge"
    ],
    "preserve_medium": [
      "jawline",
      "face_center"
    ],
    "distort_first": [
      "hair_edges",
      "cheeks",
      "outer_silhouette",
      "duplicate_planes"
    ]
  },
  "notes": [
    "maintain hot face anchor",
    "injury should feel like color and signal attacking the periphery first"
  ]
}
```

---

## 19. Minimal UI-to-AI Mapping Example

```json
{
  "user_input": {
    "style_branch": "Candy Broadcast",
    "intensity": "Strong",
    "color_mood": "Hyperpop Bright",
    "human_vs_corrupted": "Split",
    "dreamy_vs_aggressive": "Balanced",
    "text_amount": "A Little",
    "motion_amount": "Slight Echo",
    "clean_vs_messy": "Balanced"
  },
  "ai_interpretation": {
    "subtype": "candy_broadcast_hallucination",
    "primary_driver": "channel_split",
    "secondary_drivers": [
      "bloom_contamination",
      "overprint_stacking"
    ],
    "palette_family": "hyperpop_rupture",
    "density_level": "dense_signal",
    "emotion_tags": [
      "seductive",
      "emotionally_loud",
      "glamorous_instability"
    ],
    "preserved_anchors": [
      "eyes",
      "lips"
    ],
    "text_behavior": "low_subtitle_trace",
    "temporal_behavior": "low_echo"
  }
}
```

---

## 20. Composite Fever Dream Example

```json
{
  "config_id": "cfg_020_composite_fever_cover_art",
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
  "media_source": "multi_pass_live_post_process",
  "preserved_anchors": [
    "one_eye_region",
    "mouth",
    "one_readable_phrase"
  ],
  "drift_blockers": [
    "not_random_effect_soup",
    "one_anchor_must_survive",
    "one_driver_must_still_read_as_primary"
  ]
}
```

---

## 21. Suggested Real App Categories for These Examples

You could file these into groups like:
- `examples/subtype_configs`
- `examples/hybrid_configs`
- `examples/audio_profiles`
- `examples/shader_bundles`
- `examples/region_profiles`
- `examples/ui_to_ai_mappings`
- `examples/maximal_composites`

That would keep the repo from turning into a junk drawer.

---

## 22. Summary Sentence

The sample JSON bundles make the glitchcore system concrete by showing how subtype logic, artifact drivers, palette architecture, density, emotional flavor, media source, preserved anchors, audio mapping, shader bundles, hybrids, and drift blockers can all be represented as app-ready structured records.

---

## 23. Short Anchor Rule

**Make the theory executable.**
