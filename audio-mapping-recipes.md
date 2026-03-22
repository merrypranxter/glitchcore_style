# Audio Mapping Recipes

Specific frequency-to-visual mappings for each glitchcore subtype.

## Purpose

This file provides concrete audio-to-visual mapping recipes for each glitchcore subtype.

Each recipe includes:
- Frequency band assignments
- Visual parameter mappings
- State switch rules
- Example configurations

---

## 1. Recipe Structure

### 1.1 Standard Format

```json
{
  "recipe_id": "string",
  "name": "string",
  "subtype": "string",
  "audio_mode": "string",
  "frequency_bands": {
    "bass": { "range": "20-250Hz", "mapping": "string" },
    "low_mids": { "range": "250-500Hz", "mapping": "string" },
    "high_mids": { "range": "500-2000Hz", "mapping": "string" },
    "highs": { "range": "2000-8000Hz", "mapping": "string" }
  },
  "transient_response": "string",
  "amplitude_response": "string",
  "state_switches": {},
  "example_values": {}
}
```

---

## 2. Subtype Audio Recipes

### 2.1 Candy Broadcast Hallucination — Hyperpop Rupture Mode

**Recipe ID:** `audio_recipe_candy_broadcast`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_candy_broadcast",
  "name": "Hyperpop Rupture Mode",
  "subtype": "candy_broadcast_hallucination",
  "audio_mode": "spectrum_reactive",
  "frequency_bands": {
    "bass": {
      "range": "20-250Hz",
      "mapping": "widen_rgb_offset",
      "description": "Bass widens the RGB channel separation",
      "parameter": "rgb_offset_amount",
      "min_value": 0.2,
      "max_value": 1.0
    },
    "low_mids": {
      "range": "250-500Hz",
      "mapping": "increase_duplicate_spacing",
      "description": "Low mids increase space between overprint copies",
      "parameter": "overprint_offset",
      "min_value": 0.1,
      "max_value": 0.8
    },
    "high_mids": {
      "range": "500-2000Hz",
      "mapping": "enhance_edge_chatter",
      "description": "High mids activate edge glow and face emphasis",
      "parameter": "edge_emphasis",
      "min_value": 0.3,
      "max_value": 0.9
    },
    "highs": {
      "range": "2000-8000Hz",
      "mapping": "increase_sparkle_density",
      "description": "Highs add sparkle particles and fringe flicker",
      "parameter": "sparkle_density",
      "min_value": 0.0,
      "max_value": 1.0
    }
  },
  "transient_response": {
    "mapping": "channel_snap_jump",
    "description": "Sharp transients cause sudden RGB channel jumps",
    "parameter": "transient_snap",
    "duration_ms": 100,
    "recovery_ms": 300
  },
  "amplitude_response": {
    "mapping": "global_intensity",
    "description": "Overall loudness drives base corruption level",
    "parameter": "global_strength",
    "curve": "exponential"
  },
  "state_switches": {
    "chorus": {
      "action": "increase_density",
      "target_density": "overloaded",
      "transition_beats": 2
    },
    "drop": {
      "action": "brief_overdrive_then_recover",
      "overdrive_duration_ms": 500,
      "recovery_beats": 2
    },
    "verse": {
      "action": "preserve_anchor_clarity",
      "target_density": "moderate"
    }
  },
  "example_values": {
    "quiet_section": {
      "rgb_offset": 0.3,
      "overprint_spacing": 0.2,
      "edge_emphasis": 0.4,
      "sparkle": 0.1
    },
    "loud_chorus": {
      "rgb_offset": 0.9,
      "overprint_spacing": 0.7,
      "edge_emphasis": 0.85,
      "sparkle": 0.8
    }
  }
}
```

---

### 2.2 Ghost-Frame Body — Kinetic Echo Mode

**Recipe ID:** `audio_recipe_ghost_frame`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_ghost_frame",
  "name": "Kinetic Echo Mode",
  "subtype": "ghost_frame_body",
  "audio_mode": "trail_reactive",
  "frequency_bands": {
    "beat": {
      "detection": "onset",
      "mapping": "reinforce_present_frame",
      "description": "Each beat makes the present frame brighter",
      "parameter": "present_frame_boost",
      "boost_amount": 0.3,
      "decay_ms": 200
    },
    "low_mids": {
      "range": "250-500Hz",
      "mapping": "increase_echo_count",
      "description": "Low mids add more historical frames to the stack",
      "parameter": "echo_count",
      "min_value": 2,
      "max_value": 8
    },
    "pads": {
      "detection": "sustained",
      "mapping": "increase_trail_persistence",
      "description": "Sustained pads make echoes linger longer",
      "parameter": "echo_persistence",
      "min_value": 0.3,
      "max_value": 0.9
    },
    "highs": {
      "range": "2000-8000Hz",
      "mapping": "trail_shimmer",
      "description": "Highs add shimmer to echo trails",
      "parameter": "trail_shimmer",
      "min_value": 0.0,
      "max_value": 0.6
    }
  },
  "transient_response": {
    "mapping": "add_stutter_copy",
    "description": "Sharp transients add brief duplicate frames",
    "parameter": "stutter_frames",
    "frame_count": 2,
    "duration_ms": 80
  },
  "amplitude_response": {
    "mapping": "trail_brightness",
    "description": "Louder sounds make trails brighter",
    "parameter": "trail_intensity",
    "curve": "linear"
  },
  "state_switches": {
    "breakdown": {
      "action": "maximum_echo_density",
      "target_echo_count": 8,
      "fade_curve": "exponential_slow"
    },
    "build": {
      "action": "compress_echoes_toward_present",
      "transition_beats": 4
    },
    "drop": {
      "action": "present_frame_dominates",
      "target_echo_count": 2,
      "present_boost": 1.5
    }
  },
  "example_values": {
    "quiet_section": {
      "echo_count": 3,
      "persistence": 0.4,
      "trail_brightness": 0.3
    },
    "intense_breakdown": {
      "echo_count": 7,
      "persistence": 0.85,
      "trail_brightness": 0.9
    }
  }
}
```

---

### 2.3 Text-Screen Heartbreak — Spoken Confession Mode

**Recipe ID:** `audio_recipe_text_screen`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_text_screen",
  "name": "Spoken Confession Mode",
  "subtype": "text_screen_heartbreak",
  "audio_mode": "semantic_reactive",
  "frequency_bands": {
    "speech_presence": {
      "detection": "vocals_isolated",
      "mapping": "emit_phrase_fragments",
      "description": "Speech triggers text fragment emission",
      "parameter": "text_emission_rate",
      "threshold": 0.3,
      "max_rate": 0.8
    },
    "emotional_peaks": {
      "detection": "spectral_flux_in_vocals",
      "mapping": "increase_face_text_overlap",
      "description": "Emotional vocal moments push text onto face",
      "parameter": "overlap_bias",
      "min_value": 0.3,
      "max_value": 0.9
    },
    "high_mids": {
      "range": "500-2000Hz",
      "mapping": "increase_text_clarity",
      "description": "Speech frequencies improve text legibility",
      "parameter": "text_legibility",
      "min_value": 0.2,
      "max_value": 0.7
    },
    "silence": {
      "detection": "amplitude_below_threshold",
      "threshold": 0.1,
      "mapping": "linger_ghost_text",
      "description": "Silence makes previous text fade slowly",
      "parameter": "ghost_linger",
      "linger_duration_ms": 2000
    }
  },
  "transient_response": {
    "mapping": "text_flicker_stutter",
    "description": "Sharp sounds cause text to flicker",
    "parameter": "flicker_intensity",
    "duration_ms": 150
  },
  "amplitude_response": {
    "mapping": "phrase_density",
    "description": "Louder speech = more text fragments",
    "parameter": "fragment_density",
    "curve": "logarithmic"
  },
  "state_switches": {
    "whispery_sections": {
      "action": "lower_density_raise_intimacy",
      "target_density": "sparse",
      "legibility_boost": 0.2
    },
    "louder_sections": {
      "action": "increase_text_pressure",
      "target_density": "dense",
      "overlap_increase": 0.3
    },
    "pause": {
      "action": "linger_phrase_residue",
      "linger_duration_ms": 3000
    }
  },
  "example_values": {
    "whisper": {
      "text_density": 0.2,
      "legibility": 0.6,
      "overlap": 0.3
    },
    "emotional_peak": {
      "text_density": 0.8,
      "legibility": 0.4,
      "overlap": 0.85
    }
  }
}
```

---

### 2.4 Candy-Crash Compression — Bratty File Damage Mode

**Recipe ID:** `audio_recipe_candy_crash`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_candy_crash",
  "name": "Bratty File Damage Mode",
  "subtype": "candy_crash_compression",
  "audio_mode": "compression_reactive",
  "frequency_bands": {
    "bass": {
      "range": "20-250Hz",
      "mapping": "increase_block_size",
      "description": "Bass increases compression block size",
      "parameter": "block_size_multiplier",
      "min_value": 1.0,
      "max_value": 3.0
    },
    "transients": {
      "detection": "sharp_attack",
      "mapping": "packet_loss_puncture",
      "description": "Sharp transients cause packet-loss glitches",
      "parameter": "packet_loss_probability",
      "min_value": 0.0,
      "max_value": 0.8
    },
    "high_mids": {
      "range": "500-2000Hz",
      "mapping": "edge_buzz_and_chroma_damage",
      "description": "High mids activate edge buzz and color bleeding",
      "parameter": "edge_chroma_damage",
      "min_value": 0.2,
      "max_value": 0.9
    },
    "vocals": {
      "detection": "vocal_range_isolated",
      "mapping": "face_zone_smear",
      "description": "Vocals concentrate corruption on face",
      "parameter": "face_smear_amount",
      "min_value": 0.1,
      "max_value": 0.7
    }
  },
  "transient_response": {
    "mapping": "compression_spike",
    "description": "Transients cause brief quality drops",
    "parameter": "quality_dip",
    "dip_amount": 0.4,
    "recovery_ms": 400
  },
  "amplitude_response": {
    "mapping": "global_compression_pressure",
    "description": "Overall loudness drives compression intensity",
    "parameter": "compression_pressure",
    "curve": "exponential"
  },
  "state_switches": {
    "loud_sections": {
      "action": "maximum_compression_damage",
      "target_quality": 0.2,
      "block_size": 32
    },
    "quiet_sections": {
      "action": "partial_recovery",
      "target_quality": 0.6,
      "block_size": 8
    },
    "transitions": {
      "action": "packet_loss_spikes",
      "spike_probability": 0.5
    }
  },
  "example_values": {
    "quiet": {
      "quality": 0.6,
      "block_size": 8,
      "chroma_bleed": 0.3
    },
    "loud": {
      "quality": 0.2,
      "block_size": 24,
      "chroma_bleed": 0.8
    }
  }
}
```

---

### 2.5 CRT Contour — Signal Saint Mode

**Recipe ID:** `audio_recipe_crt_contour`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_crt_contour",
  "name": "Signal Saint Mode",
  "subtype": "crt_contour",
  "audio_mode": "pulse_reactive",
  "frequency_bands": {
    "bass": {
      "range": "20-250Hz",
      "mapping": "contour_thickness",
      "description": "Bass thickens the scanline contour bands",
      "parameter": "line_thickness",
      "min_value": 1.0,
      "max_value": 4.0
    },
    "highs": {
      "range": "2000-8000Hz",
      "mapping": "scanline_shimmer",
      "description": "Highs make scanlines sparkle and shift",
      "parameter": "shimmer_intensity",
      "min_value": 0.0,
      "max_value": 0.7
    },
    "sustained_tones": {
      "detection": "sustained_notes",
      "mapping": "halo_build",
      "description": "Long tones build phosphor halo",
      "parameter": "halo_growth",
      "growth_rate": 0.1,
      "max_halo": 0.8
    },
    "vocals": {
      "detection": "vocal_presence",
      "mapping": "face_contour_emphasis",
      "description": "Vocals make face scanlines more prominent",
      "parameter": "face_emphasis",
      "min_value": 0.3,
      "max_value": 0.9
    }
  },
  "transient_response": {
    "mapping": "row_jitter",
    "description": "Sharp sounds cause brief line displacement",
    "parameter": "jitter_amount",
    "duration_ms": 80
  },
  "amplitude_response": {
    "mapping": "phosphor_glow_intensity",
    "description": "Overall level drives phosphor brightness",
    "parameter": "phosphor_intensity",
    "curve": "linear"
  },
  "state_switches": {
    "sustained_notes": {
      "action": "halo_grows",
      "growth_rate": 0.05
    },
    "percussion": {
      "action": "row_jitter_spikes",
      "jitter_probability": 0.6
    },
    "silence": {
      "action": "static_veil_thickens",
      "static_increase": 0.2
    }
  },
  "example_values": {
    "quiet": {
      "line_thickness": 1.5,
      "shimmer": 0.1,
      "halo": 0.3,
      "static": 0.1
    },
    "sustained": {
      "line_thickness": 2.5,
      "shimmer": 0.3,
      "halo": 0.7,
      "static": 0.15
    }
  }
}
```

---

### 2.6 Glitter-Signal Overprint — Gloss Disaster Mode

**Recipe ID:** `audio_recipe_glitter_signal`

**Configuration:**
```json
{
  "recipe_id": "audio_recipe_glitter_signal",
  "name": "Gloss Disaster Mode",
  "subtype": "glitter_signal_overprint",
  "audio_mode": "pulse_reactive",
  "frequency_bands": {
    "highs": {
      "range": "2000-8000Hz",
      "mapping": "sparkle_density",
      "description": "Highs add glitter particles",
      "parameter": "sparkle_amount",
      "min_value": 0.2,
      "max_value": 1.0
    },
    "vocals": {
      "detection": "vocal_presence",
      "mapping": "gloss_bloom",
      "description": "Vocals make face more luminous",
      "parameter": "bloom_intensity",
      "min_value": 0.4,
      "max_value": 0.9
    },
    "bass": {
      "range": "20-250Hz",
      "mapping": "duplicate_drift",
      "description": "Bass makes overprint copies separate wider",
      "parameter": "duplicate_spacing",
      "min_value": 0.2,
      "max_value": 0.8
    },
    "chorus": {
      "detection": "harmonic_richness",
      "mapping": "overprint_expansion",
      "description": "Chorus sections show more layers",
      "parameter": "layer_visibility",
      "min_value": 0.5,
      "max_value": 1.0
    }
  },
  "transient_response": {
    "mapping": "sparkle_burst",
    "description": "Sharp sounds cause sparkle explosions",
    "parameter": "burst_intensity",
    "duration_ms": 150
  },
  "amplitude_response": {
    "mapping": "halo_growth",
    "description": "Louder sounds grow the glow halo",
    "parameter": "halo_size",
    "curve": "ease_out"
  },
  "state_switches": {
    "chorus": {
      "action": "maximum_overprint",
      "target_layers": 5,
      "sparkle_boost": 0.3
    },
    "verse": {
      "action": "reduced_layers",
      "target_layers": 2,
      "face_clarity": 0.8
    },
    "bridge": {
      "action": "sparkle_density_peaks",
      "sparkle_max": 1.0
    }
  },
  "example_values": {
    "verse": {
      "layers": 2,
      "sparkle": 0.4,
      "bloom": 0.5
    },
    "chorus": {
      "layers": 4,
      "sparkle": 0.9,
      "bloom": 0.85
    }
  }
}
```

---

## 3. Universal Audio Behaviors

### 3.1 Amplitude Response Curve

```
Amplitude 0.0 → Visual 0.0
Amplitude 0.25 → Visual 0.15
Amplitude 0.5 → Visual 0.4
Amplitude 0.75 → Visual 0.7
Amplitude 1.0 → Visual 1.0
```

Use exponential or ease-out curves for natural feel.

### 3.2 Transient Response

| Transient Type | Response |
|----------------|----------|
| Sharp Attack | Quick spike, fast recovery |
| Soft Attack | Gradual increase |
| Sharp Decay | Quick release |
| Soft Decay | Slow fade |

### 3.3 Sustained Sound Response

| Sound Type | Response |
|------------|----------|
| Drone/Pad | Accumulating effect |
| Sustained Note | Gradual build |
| Long Tone | Slow intensity increase |
| Ambient Texture | Thickening |

---

## 4. Summary

Audio mapping recipes provide:
- Frequency-to-visual mappings
- Transient responses
- Amplitude curves
- State switch rules
- Example values

Use these to make glitchcore respond musically and intelligently.

---

## 5. Short Anchor Rule

The music should conduct the corruption, not just trigger it.
