# glitchcore_style

> **A structured style system for glitchcore art generation.** Covers visual subtypes, palette logic, artifact drivers, density control, subject preservation, audio reactivity, GLSL shaders, JSON schemas, and prompt construction — everything needed to turn "make it glitchy" into precise, emotionally alive output.

---

## What Is This Repo?

This is a **complete reference system** for generating glitchcore-aesthetic art with AI, shader pipelines, or any tool that accepts structured style parameters. It's designed to be consumed directly by sonar apps, vibe-coded tools, AI art generators, and LLM-powered creative pipelines.

Glitchcore, as defined here, is **not** generic RGB splits or stock glitch filters. It's a precise aesthetic language: artifact-driven identity distortion, beauty under signal damage, hyperpop-saturated palette pressure, and specific media-failure logic acting on the body.

---

## Quick Navigation

| If you need... | Start here |
|----------------|-----------|
| Pick a style | [`core/subcategories-reference-index.md`](core/subcategories-reference-index.md) |
| Use a ready preset | [`presets/preset-library.md`](presets/preset-library.md) |
| Understand color | [`core/palette-energy-system.md`](core/palette-energy-system.md) |
| Choose corruption type | [`core/artifact-driver-taxonomy.md`](core/artifact-driver-taxonomy.md) |
| Set how much corruption | [`core/signal-density-system.md`](core/signal-density-system.md) |
| Preserve a face | [`subject/face-and-body-anchor-profiles.md`](subject/face-and-body-anchor-profiles.md) |
| Add text debris | [`effects/text-screen-and-interface-debris.md`](effects/text-screen-and-interface-debris.md) |
| Add compression damage | [`effects/compression-and-codec-corruption.md`](effects/compression-and-codec-corruption.md) |
| Add motion trails | [`effects/temporal-echo-and-motion-stacks.md`](effects/temporal-echo-and-motion-stacks.md) |
| Make it audio-reactive | [`audio/music-mode-profiles.md`](audio/music-mode-profiles.md) |
| Build prompts | [`language/prompt-construction-system.md`](language/prompt-construction-system.md) |
| Use shader code | [`technical/glsl-behavior-snippets.md`](technical/glsl-behavior-snippets.md) |
| Validate a config | [`technical/json-schema-style-spec.md`](technical/json-schema-style-spec.md) |
| Fix bad output | [`quality/drift-rescue-recipes.md`](quality/drift-rescue-recipes.md) |
| Score an output | [`quality/image-evaluation-rubric.md`](quality/image-evaluation-rubric.md) |
| Understand AI input parsing | [`ai/ai-control-logic-map.md`](ai/ai-control-logic-map.md) |

---

## Repository Structure

```
glitchcore_style/
│
├── README.md                              ← You are here
├── repo-structure.md                      ← Detailed navigation guide
│
├── core/                                  ← Core style system
│   ├── subcategories-reference-index.md   ← Master subtype map
│   ├── subcategory-system-glitchcore.md   ← Full subtype catalog
│   ├── palette-energy-system.md           ← Color logic & emotional temperature
│   ├── signal-density-system.md           ← Corruption density levels
│   ├── artifact-driver-taxonomy.md        ← All corruption mechanisms
│   └── hybridization-rules.md             ← Subtype combination rules
│
├── subject/                               ← Subject & composition
│   ├── subject-treatment-rules.md         ← Face, body, object handling
│   ├── face-and-body-anchor-profiles.md   ← Anchor zone presets
│   └── region-priority-map.md             ← Zone-by-zone preservation
│
├── effects/                               ← Specialized effect systems
│   ├── text-screen-and-interface-debris.md
│   ├── compression-and-codec-corruption.md
│   └── temporal-echo-and-motion-stacks.md
│
├── audio/                                 ← Audio & interactivity
│   ├── music-mode-profiles.md
│   ├── audio-mapping-recipes.md
│   └── shader-and-audio-reactive-system.md
│
├── language/                              ← Vocabulary & prompt construction
│   ├── glam-pop-glitch-vocabulary.md
│   ├── style-language-to-code-translation.md
│   └── prompt-construction-system.md
│
├── technical/                             ← Implementation
│   ├── json-schema-style-spec.md
│   ├── glsl-behavior-snippets.md
│   ├── shader-preset-bundles.md
│   └── sample-json-bundles.md
│
├── presets/
│   └── preset-library.md                  ← 10 ready-to-use style configs
│
├── ai/                                    ← AI control & interface
│   ├── ai-control-logic-map.md
│   └── user-facing-control-model.md
│
└── quality/                               ← Quality control
    ├── drift-rescue-recipes.md
    ├── anti-drift-rules.md
    └── image-evaluation-rubric.md
```

---

## The Five Core Concepts

Understanding these five concepts unlocks the entire system.

### 1. Subtypes — The "What"

Every glitchcore image belongs to a subtype. Each subtype has its own artifact logic, palette family, emotional tone, and preservation rules. There are 9 primary subtypes and an infinite hybrid space:

| Subtype | Mood | Primary Driver | Best For |
|---------|------|----------------|----------|
| **Candy Broadcast Hallucination** | Seductive, hyperpop | Channel Split | Glam portraits, beauty closeups |
| **RGB Phantom** | Electric, spectral | Channel Split (wide) | Profile shots, chromatic effects |
| **Ghost Frame Body** | Kinetic, haunted | Temporal Echo | Dance, movement, action |
| **Pastel Identity Smear** | Dreamy, fragile | Overprint Stacking | Soft portraits, romantic moments |
| **Candy Crash Compression** | Bratty, internet-broken | Compression Chew | Screenshot aesthetic, broken beauty |
| **Text Screen Heartbreak** | Lonely, confessional | Text Interface Debris | Digital romance, mediated intimacy |
| **CRT Contour** | Iconic, ceremonial | Scanline Contour Banding | Strong silhouettes, iconic portraits |
| **Surveillance Apparition** | Cold, watched | Capture Degradation | Institutional scenes, cold distance |
| **Glitter Signal Overprint** | Glamorous, radiant | Overprint + Bloom | Diva energy, expensive beauty |
| **Composite Fever Dream** | Decadent, overloaded | Multiple | Maximal art, cover-art energy |

→ Full details: [`core/subcategories-reference-index.md`](core/subcategories-reference-index.md)

---

### 2. Palette Families — The "Color"

Every palette has three defined roles. No rainbow soup.

```
DOMINANT  (60–70%) → Sets emotional temperature
COLLISION (20–30%) → Creates tension
ACCENT    (5–10%)  → Provides focal puncture
```

| Family | Dominant | Collision | Emotion |
|--------|----------|-----------|---------|
| **Hyperpop Rupture** | Magenta / Hot Pink | Cyan / Electric Blue | Seductive, loud |
| **Pastel Signal Melt** | Cotton Candy Pink | Lavender / Baby Blue | Dreamy, fragile |
| **Gloss Electric Glam** | Glossy Hot Pink | Violet / Cool Cyan | Glamorous, expensive |
| **Phosphor Noir** | Teal / Cold Cyan | Ice Blue | Remote, eerie |
| **Codec Candy Crash** | Flat Magenta | Flat Cyan / Violet | Bratty, broken |
| **Rainbow Channel Hallucination** | Cyan / Magenta | Green Spectral | Electric, unstable |
| **Toxic Cathode Candy** | Acid Green / Yellow | Hot Magenta | Toxic, industrial-glamour |

→ Full details: [`core/palette-energy-system.md`](core/palette-energy-system.md)

---

### 3. Artifact Drivers — The "How"

Corruption mechanisms that transform the image. One leads; 2–3 support.

| Driver | Effect | Key Subtypes |
|--------|--------|--------------|
| **Channel Split** | RGB color separation / misregistration | Candy Broadcast, RGB Phantom |
| **Overprint Stacking** | Multiple semi-transparent copies | Glitter Signal, Pastel Smear |
| **Bloom Contamination** | Glow and light bleed | Candy Broadcast, Glitter Signal |
| **Temporal Echo** | Motion trails through time | Ghost Frame |
| **Compression Chew** | Digital codec damage, macroblocks | Candy Crash |
| **Text Interface Debris** | Fragmented text as visual corruption | Text Screen |
| **Scanline Contour Banding** | CRT lines following body contours | CRT Contour |
| **Capture Degradation** | CCTV/surveillance feed noise | Surveillance |
| **Sparkle Static** | Glitter particle noise | Glitter Signal |
| **Color Field Collision** | Clashing color zones | Multiple |
| **Raster Tear** | Horizontal image tearing | Multiple |
| **Noise Veil** | Film/TV static texture | Surveillance |

→ Full details: [`core/artifact-driver-taxonomy.md`](core/artifact-driver-taxonomy.md)

---

### 4. Signal Density — The "How Much"

Five levels from subtle to chaos:

| Level | Code | Corruption | Rest | Description |
|-------|------|------------|------|-------------|
| 1 | `sparse_signal` | 20–30% | 70–80% | Elegant, barely-there damage |
| 2 | `moderate_signal` | 40–50% | 50–60% | Balanced — beauty and damage share space |
| 3 | `dense_signal` | 65–75% | 25–35% | Intense — corruption dominates |
| 4 | `overloaded_signal` | 80–90% | 10–20% | Desperate — one anchor barely holds |
| 5 | `pile_up_delirium` | 90–100% | 0–10% | Maximum chaos with structured hierarchy |

→ Full details: [`core/signal-density-system.md`](core/signal-density-system.md)

---

### 5. Anchor Preservation — The "What Survives"

**The anchor rule: Preserve one hot anchor. Injure everything else.**

The system protects key zones from corruption so the image remains emotionally readable. For faces:

```
Priority order (most protected → least):
Eyes → Lips → Nose Bridge → Face Center → Jawline
```

For bodies:
```
Torso Center → Gesture Arc → Shoulder Line → Head Position
```

→ Full details: [`subject/face-and-body-anchor-profiles.md`](subject/face-and-body-anchor-profiles.md) + [`subject/region-priority-map.md`](subject/region-priority-map.md)

---

## The 10 Presets — Ready to Use

Ten fully specified configurations with JSON configs and prompt templates:

| Preset | File Key | Mood | Intensity |
|--------|----------|------|-----------|
| **Candy Angel** | `preset_candy_angel` | Seductive, hyperpop loud | High |
| **Soft Dream** | `preset_soft_dream` | Dreamy, romantic, fragile | Medium |
| **Electric Ghost** | `preset_electric_ghost` | Electric, unstable, spectral | Medium-High |
| **Motion Memory** | `preset_motion_memory` | Ecstatic, kinetic, haunted | High |
| **Terminal Confession** | `preset_terminal_confession` | Confessional, lonely, obsessive | High |
| **Signal Saint** | `preset_signal_saint` | Iconic, ceremonial, remote | Low-Medium |
| **Internet Broken** | `preset_internet_broken` | Bratty, internet-damaged | Very High |
| **Diva Glitter** | `preset_diva_glitter` | Glamorous, coquettish, radiant | High |
| **Fever Dream** | `preset_fever_dream` | Decadent, feverish, overloaded | Maximum |
| **Watched** | `preset_watched` | Cold, depersonalized, watched | Medium |

→ Full configs + prompt templates: [`presets/preset-library.md`](presets/preset-library.md)

---

## Config Format (JSON Schema)

Every glitchcore configuration uses this structure:

```json
{
  "config_id": "cfg_001_candy_broadcast_portrait",
  "subtype": "candy_broadcast_hallucination",
  "primary_driver": "channel_split",
  "secondary_drivers": ["bloom_contamination", "overprint_stacking", "sparkle_static"],
  "palette_family": "hyperpop_rupture",
  "palette_structure": {
    "dominant_hue_family": "magenta_hot_pink",
    "collision_hue_family": "cyan_electric_blue",
    "accent_puncture": "sharp_white"
  },
  "density_level": "dense_signal",
  "emotion_tags": ["seductive", "emotionally_loud", "synthetic_euphoria"],
  "preserved_anchors": ["eyes", "lips", "face_center"],
  "drift_blockers": ["not_clean_editorial", "not_simple_rgb_filter"],
  "audio_mode": "spectrum_reactive",
  "audio_mapping": {
    "bass": "widen_rgb_offset",
    "highs": "fringe_flicker",
    "transients": "channel_snap_jump"
  }
}
```

**Required fields:** `config_id`, `subtype`, `primary_driver`

→ Full schema + validation rules: [`technical/json-schema-style-spec.md`](technical/json-schema-style-spec.md)  
→ 20+ example configs: [`technical/sample-json-bundles.md`](technical/sample-json-bundles.md)

---

## Prompt Construction

To translate a glitchcore config into an image prompt, use this order:

```
1. Subject description         → "close-up beauty portrait"
2. Subtype declaration         → "treated as [subtype]"
3. Primary driver              → "with [driver] as main transformation"
4. Secondary drivers           → "supported by [driver1], [driver2]"
5. Palette specification       → "using [palette] with [dominant], [collision], [accent]"
6. Density level               → "at [density] signal load"
7. Emotional flavor            → "creating mood of [emotion1], [emotion2]"
8. Material feel               → "with [material] surface"
9. Preserved anchor            → "while preserving [anchor]"
10. Anti-drift clause          → "not [drift_type]"
```

**Example (Candy Angel preset):**
```
A beauty close-up treated as a candy broadcast hallucination, with channel split 
as the main transformation logic, supported by bloom contamination, overprint 
stacking, and sparkle static, using a hyperpop rupture palette with dominant 
magenta and hot pink, cyan as collision hue, and sharp white flare accents, at 
dense signal density, creating a mood of seductive emotional loudness and 
synthetic euphoria, with glossy digital surface feel, while preserving the eyes, 
lips, and face center, not a clean fashion editorial or simple RGB filter effect.
```

→ Full system: [`language/prompt-construction-system.md`](language/prompt-construction-system.md)  
→ Emotion vocabulary: [`language/glam-pop-glitch-vocabulary.md`](language/glam-pop-glitch-vocabulary.md)  
→ Language-to-code translation: [`language/style-language-to-code-translation.md`](language/style-language-to-code-translation.md)

---

## Audio Reactivity

The system supports six audio-reactive modes:

| Mode | Description | Best For |
|------|-------------|----------|
| `spectrum_reactive` | Real-time frequency → visual parameters | Live performance |
| `semantic_reactive` | Music meaning/mood drives style | Art generation |
| `trail_reactive` | Beat/amplitude → trail length | Dance/movement |
| `compression_reactive` | Drops → compression artifacts | Club visuals |
| `pulse_reactive` | Beat → intensity pulses | High-energy tracks |
| `tear_reactive_subtle` | Subtle frequency → raster tears | Ambient/chill |

**Frequency mapping:**
```
Bass      → Widen channel split / RGB offset
Low Mids  → Increase duplicate spacing / overprint offset
High Mids → Edge chatter / bloom intensity
Highs     → Fringe flicker / sparkle density
Transients → Snap jumps / sudden artifact spikes
Vocals    → Face-zone emphasis
Amplitude → Overall density
```

→ Full audio system: [`audio/music-mode-profiles.md`](audio/music-mode-profiles.md)  
→ Mapping recipes: [`audio/audio-mapping-recipes.md`](audio/audio-mapping-recipes.md)  
→ Shader integration: [`audio/shader-and-audio-reactive-system.md`](audio/shader-and-audio-reactive-system.md)

---

## GLSL Shader Code

Ready-to-use fragment shaders for each artifact driver:

| Shader | File | Description |
|--------|------|-------------|
| Channel Split | [`technical/glsl-behavior-snippets.md`](technical/glsl-behavior-snippets.md) §1 | RGB displacement with edge bias |
| Bloom / Glow | §2 | Luminance-based light bleed |
| Overprint Stacking | §3 | Multi-layer screen blend |
| Temporal Echo | §4 | History buffer trail system |
| Scanline Contour | §5 | CRT banding with contour following |
| Compression Artifacts | §6 | Macroblock quantization |
| Noise / Static | §7 | Film grain and TV static |
| Sparkle / Glitter | §8 | Specular particle system |
| Text Debris | §9 | Text atlas overlay |
| Full Pass Combiner | §10 | Anchor-mask composite |
| Utility Functions | §11 | Random, noise, luminance, screen, overlay |

→ Shader presets: [`technical/shader-preset-bundles.md`](technical/shader-preset-bundles.md)

---

## Quality Control

### Evaluation Rubric

Score images across 10 categories (max 50 points):

| Category | What It Measures |
|----------|-----------------|
| 1. Figure / Identity Anchor | Is there a readable human subject? |
| 2. Artifact Specificity | Is there a real, identifiable failure mode? |
| 3. Artifact Hierarchy | Is there a clear lead driver? |
| 4. Palette Architecture | Does the color have structure and hierarchy? |
| 5. Signal Density Control | Is the density level intentional? |
| 6. Emotional Consequence | Does the corruption create a feeling? |
| 7. Media / Material Specificity | Does it feel like a specific screen/file type? |
| 8. Retrieval Path Clarity | Can the eye recover something human? |
| 9. Anti-Drift Integrity | Does it resist generic cyberpunk/filter drift? |
| 10. Overall Subtype Coherence | Does it clearly belong to a subtype? |

**Score guide:** 45–50 = excellent · 38–44 = strong · 30–37 = promising · 20–29 = weak · 0–19 = failed

→ Full rubric: [`quality/image-evaluation-rubric.md`](quality/image-evaluation-rubric.md)

---

### Drift Types to Avoid

| Drift Type | Symptoms | Fix |
|------------|----------|-----|
| Generic Cyberpunk | Too polished, too cinematic, no artifact logic | Add real corruption: channel mis-reg, compression chew |
| Fake Glitch Filter | Glitch sits on top, face untouched | Make corruption structural — split eyes, let text hit face |
| Beauty Ad | Corruption is timid, decorative only | Ruin something valuable — let damage reach the glamour |
| Dead Black Monitor | All black/cyan, no tension, same mood always | Add accent collisions, density shifts, pop palette branches |
| Rainbow Clown Soup | All colors equal, no hierarchy | Apply palette architecture: dominant/collision/accent |
| Random Effect Soup | Everything screaming equally | Choose one lead driver, demote everything else |
| Generic Retro/VHS | "Vintage" texture with no body fracture | Push the body/screen relationship |
| Analog Horror Cliché | Too horror-coded, too monochrome | Add palette energy, body glamour, emotional ambiguity |

→ Full anti-drift rules: [`quality/anti-drift-rules.md`](quality/anti-drift-rules.md)  
→ Rescue recipes: [`quality/drift-rescue-recipes.md`](quality/drift-rescue-recipes.md)

---

## For AI Systems (Implementation Guide)

### Input Parsing Logic

When receiving user input, parse for:

1. **Emotional keywords** → map to subtype + palette  
   `"dreamy"` → Pastel Identity Smear + Pastel Signal Melt  
   `"bratty"` → Candy Crash + Codec Candy Crash  
   `"seductive"` → Candy Broadcast + Hyperpop Rupture  

2. **Subtype hints** → direct subtype selection  
   `"candy"`, `"hyperpop"` → Candy Broadcast  
   `"ghost"`, `"trail"`, `"echo"` → Ghost Frame Body  
   `"text"`, `"chat"`, `"confession"` → Text Screen  

3. **Intensity cues** → density level  
   `"subtle"`, `"gentle"` → Sparse (1)  
   `"intense"`, `"extreme"` → Overloaded (4)  
   `"chaos"`, `"pile-up"` → Pile-Up Delirium (5)  

→ Full decision tree logic: [`ai/ai-control-logic-map.md`](ai/ai-control-logic-map.md)

### Always Apply These Rules

```
1. Start with a specific subtype — never apply generic "glitch"
2. Define palette hierarchy — dominant → collision → accent
3. Preserve one hot anchor — usually eyes for face images
4. Establish driver hierarchy — one primary, 2–3 secondary
5. Check output for drift — compare against drift types
6. Validate config against JSON schema before processing
```

### Config Validation

Every config must have:
- `config_id` (string, unique)
- `subtype` (from valid enum in [`technical/json-schema-style-spec.md`](technical/json-schema-style-spec.md))
- `primary_driver` (from valid enum)

→ Schema file: [`technical/json-schema-style-spec.md`](technical/json-schema-style-spec.md)  
→ UI control model: [`ai/user-facing-control-model.md`](ai/user-facing-control-model.md)

---

## Common Workflows

### Workflow 1: Generate a New Glitchcore Config

```
1. Pick subtype     → core/subcategories-reference-index.md
2. Choose palette   → core/palette-energy-system.md
3. Select drivers   → core/artifact-driver-taxonomy.md
4. Set density      → core/signal-density-system.md
5. Define anchors   → subject/face-and-body-anchor-profiles.md
6. Build prompt     → language/prompt-construction-system.md
7. Validate JSON    → technical/json-schema-style-spec.md
```

### Workflow 2: Use a Preset (Fastest Path)

```
1. Browse presets   → presets/preset-library.md
2. Select closest   → copy JSON config or prompt template
3. Customize        → adjust density, palette, anchors
4. Apply            → use prompt template directly
```

### Workflow 3: Fix a Drifted Output

```
1. Score the image  → quality/image-evaluation-rubric.md
2. Identify drift   → quality/anti-drift-rules.md
3. Apply rescue     → quality/drift-rescue-recipes.md
4. Adjust params    → language/style-language-to-code-translation.md
5. Re-verify        → quality/image-evaluation-rubric.md
```

### Workflow 4: Add Audio Reactivity

```
1. Pick audio mode  → audio/music-mode-profiles.md
2. Map frequencies  → audio/audio-mapping-recipes.md
3. Hook to shaders  → audio/shader-and-audio-reactive-system.md
4. Test + tune      → adjust thresholds
```

### Workflow 5: Implement Shader Pipeline

```
1. Get GLSL code    → technical/glsl-behavior-snippets.md
2. Pick shader pack → technical/shader-preset-bundles.md
3. Configure params → technical/json-schema-style-spec.md
4. Hook audio       → audio/shader-and-audio-reactive-system.md
```

---

## Key Principles

> **Preserve one hot anchor. Injure everything else.**

> **One dominant, one collision, one accent. No rainbow soup.**

> **One primary driver leads. 2–3 secondary drivers support.**

> **The tension between beauty and damage creates the aesthetic.**

> **Glitch should not sit on the body. It should get into the body.**

> **Make the theory executable. Turn poetry into parameters without killing the poetry.**

---

## File Index

| File | Category | Description |
|------|----------|-------------|
| [`core/subcategories-reference-index.md`](core/subcategories-reference-index.md) | Core | Master subtype map — start here |
| [`core/subcategory-system-glitchcore.md`](core/subcategory-system-glitchcore.md) | Core | Full 12-subtype catalog |
| [`core/palette-energy-system.md`](core/palette-energy-system.md) | Core | Color families, palette logic |
| [`core/signal-density-system.md`](core/signal-density-system.md) | Core | Density levels 1–5 |
| [`core/artifact-driver-taxonomy.md`](core/artifact-driver-taxonomy.md) | Core | All artifact drivers cataloged |
| [`core/hybridization-rules.md`](core/hybridization-rules.md) | Core | Subtype combination rules |
| [`subject/subject-treatment-rules.md`](subject/subject-treatment-rules.md) | Subject | Faces, bodies, objects |
| [`subject/face-and-body-anchor-profiles.md`](subject/face-and-body-anchor-profiles.md) | Subject | Anchor presets |
| [`subject/region-priority-map.md`](subject/region-priority-map.md) | Subject | Zone-by-zone preservation |
| [`effects/text-screen-and-interface-debris.md`](effects/text-screen-and-interface-debris.md) | Effects | Text as corruption |
| [`effects/compression-and-codec-corruption.md`](effects/compression-and-codec-corruption.md) | Effects | Compression damage |
| [`effects/temporal-echo-and-motion-stacks.md`](effects/temporal-echo-and-motion-stacks.md) | Effects | Motion trails, time-stacking |
| [`audio/music-mode-profiles.md`](audio/music-mode-profiles.md) | Audio | Audio-reactive modes |
| [`audio/audio-mapping-recipes.md`](audio/audio-mapping-recipes.md) | Audio | Frequency-to-visual mapping |
| [`audio/shader-and-audio-reactive-system.md`](audio/shader-and-audio-reactive-system.md) | Audio | Shader/audio integration |
| [`language/glam-pop-glitch-vocabulary.md`](language/glam-pop-glitch-vocabulary.md) | Language | Emotion vocabulary |
| [`language/style-language-to-code-translation.md`](language/style-language-to-code-translation.md) | Language | Language → parameters |
| [`language/prompt-construction-system.md`](language/prompt-construction-system.md) | Language | Prompt building system |
| [`technical/json-schema-style-spec.md`](technical/json-schema-style-spec.md) | Technical | Formal JSON schema |
| [`technical/glsl-behavior-snippets.md`](technical/glsl-behavior-snippets.md) | Technical | GLSL shader code |
| [`technical/shader-preset-bundles.md`](technical/shader-preset-bundles.md) | Technical | Shader configurations |
| [`technical/sample-json-bundles.md`](technical/sample-json-bundles.md) | Technical | 20+ example configs |
| [`presets/preset-library.md`](presets/preset-library.md) | Presets | 10 ready-to-use presets |
| [`ai/ai-control-logic-map.md`](ai/ai-control-logic-map.md) | AI | Input parsing + decision trees |
| [`ai/user-facing-control-model.md`](ai/user-facing-control-model.md) | AI | UI/UX control design |
| [`quality/drift-rescue-recipes.md`](quality/drift-rescue-recipes.md) | Quality | Output fix recipes |
| [`quality/anti-drift-rules.md`](quality/anti-drift-rules.md) | Quality | Drift prevention rules |
| [`quality/image-evaluation-rubric.md`](quality/image-evaluation-rubric.md) | Quality | Scoring rubric (50-point) |

---

## System Version

**v1.0** — Core system: 9 subtypes, 12 artifact drivers, 7 palette families, 5 density levels, 10 presets, 6 audio modes, 11 GLSL shaders, formal JSON schema.

**Philosophy:**
> Make the theory executable. Turn poetry into parameters without killing the poetry.
