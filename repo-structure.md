# Glitchcore Style Repo — Structure Guide

## Overview

This repository contains a comprehensive style system for glitchcore aesthetics — a bright, seductive, hyperpop-influenced approach to digital corruption and visual glitch art.

**Purpose:** Help AI systems generate glitchcore outputs that are emotionally specific, stylistically coherent, and technically implementable.

---

## Directory Structure

```
glitchcore_style/
│
├── README.md                              ← Start here — full system overview
├── repo-structure.md                      ← YOU ARE HERE
│
├── core/                                  ← Core style system
│   ├── subcategories-reference-index.md   ← Master subtype map (start here)
│   ├── subcategory-system-glitchcore.md   ← Full subtype catalog
│   ├── palette-energy-system.md           ← Color logic and emotional temperature
│   ├── signal-density-system.md           ← Corruption vs preservation levels
│   ├── artifact-driver-taxonomy.md        ← All corruption mechanisms cataloged
│   └── hybridization-rules.md             ← Rules for combining subtypes
│
├── subject/                               ← Subject & composition
│   ├── subject-treatment-rules.md         ← How to treat faces, bodies, objects
│   ├── face-and-body-anchor-profiles.md   ← Pre-configured anchor settings
│   └── region-priority-map.md             ← Zone-by-zone preservation rules
│
├── effects/                               ← Specialized effect systems
│   ├── text-screen-and-interface-debris.md    ← Text as visual corruption
│   ├── compression-and-codec-corruption.md    ← Digital damage aesthetics
│   └── temporal-echo-and-motion-stacks.md     ← Time-based glitch
│
├── audio/                                 ← Audio & interactivity
│   ├── music-mode-profiles.md             ← Audio-reactive behavior maps
│   ├── audio-mapping-recipes.md           ← Frequency-to-visual mappings
│   └── shader-and-audio-reactive-system.md    ← Shader/audio integration
│
├── language/                              ← Style vocabulary & prompt construction
│   ├── glam-pop-glitch-vocabulary.md      ← Emotional language for bright glitch
│   ├── style-language-to-code-translation.md  ← Turn descriptions into code
│   └── prompt-construction-system.md      ← How to build effective prompts
│
├── technical/                             ← Technical implementation
│   ├── json-schema-style-spec.md          ← Formal JSON schema & validation
│   ├── glsl-behavior-snippets.md          ← Ready-to-use shader code
│   ├── shader-preset-bundles.md           ← Shader configuration bundles
│   └── sample-json-bundles.md             ← Example configs for implementation
│
├── presets/                               ← Ready-to-use presets
│   └── preset-library.md                  ← 10 pre-configured style presets
│
├── ai/                                    ← AI control & interface
│   ├── ai-control-logic-map.md            ← Input parsing & decision trees
│   └── user-facing-control-model.md       ← UI/UX control design
│
└── quality/                               ← Quality control & troubleshooting
    ├── drift-rescue-recipes.md            ← Fixes for when outputs go wrong
    ├── anti-drift-rules.md                ← How to prevent common drift types
    └── image-evaluation-rubric.md         ← Scoring rubric for output quality
```

---

## Quick Start Paths

### "I need to pick a glitch style"
→ `core/subcategories-reference-index.md`

### "I need to understand color choices"
→ `core/palette-energy-system.md`

### "I need to know what corruption effects to use"
→ `core/artifact-driver-taxonomy.md`

### "I need to preserve a face properly"
→ `subject/face-and-body-anchor-profiles.md` + `subject/region-priority-map.md`

### "I need to make it react to music"
→ `audio/music-mode-profiles.md`

### "I need to add text debris"
→ `effects/text-screen-and-interface-debris.md`

### "I need compression damage"
→ `effects/compression-and-codec-corruption.md`

### "I need motion trails"
→ `effects/temporal-echo-and-motion-stacks.md`

### "The output looks wrong"
→ `quality/drift-rescue-recipes.md`

### "I need example code/configs"
→ `technical/sample-json-bundles.md`

---

## Core Concepts (Read These First)

### 1. Subtypes (The "What")

Glitchcore has distinct subtypes, each with its own personality:

| Subtype | Vibe | Key Driver |
|---------|------|------------|
| Candy Broadcast | Hyperpop, seductive | Channel Split |
| RGB Phantom | Electric, spectral | Channel Split (wide) |
| Ghost Frame | Kinetic, haunted | Temporal Echo |
| Pastel Smear | Dreamy, fragile | Overprint Stacking |
| Candy Crash | Bratty, internet-broken | Compression Chew |
| Text Screen | Confessional, lonely | Text Interface Debris |
| CRT Contour | Iconic, ceremonial | Scanline Contour |
| Surveillance | Watched, cold | Capture Degradation |
| Glitter Signal | Glamorous, radiant | Overprint + Bloom |

**Full details:** `core/subcategories-reference-index.md`

---

### 2. Palette Families (The "Color")

Every palette has 3 roles:

```
DOMINANT (60-70%) → Sets emotional temperature
COLLISION (20-30%) → Creates tension
ACCENT (5-10%) → Provides focal points
```

| Family | Colors | Emotion |
|--------|--------|---------|
| Hyperpop Rupture | Magenta + Cyan | Seductive, loud |
| Pastel Signal Melt | Pink + Lavender | Dreamy, fragile |
| Gloss Electric Glam | Hot Pink + Violet | Glamorous, expensive |
| Phosphor Noir | Teal + Ice Blue | Remote, eerie |
| Codec Candy Crash | Magenta + Flat Cyan | Bratty, broken |

**Full details:** `core/palette-energy-system.md`

---

### 3. Artifact Drivers (The "How")

The corruption mechanisms:

| Driver | What It Does |
|--------|--------------|
| Channel Split | RGB color separation |
| Overprint Stacking | Ghost copies layered |
| Bloom Contamination | Glow and light bleed |
| Temporal Echo | Motion trails through time |
| Compression Chew | Digital file damage |
| Text Interface Debris | Fragmented text as corruption |
| Scanline Contour | CRT lines following shapes |
| Capture Degradation | Surveillance feed noise |
| Sparkle Static | Glitter particles |
| Color Field Collision | Clashing color zones |

**Full details:** `core/artifact-driver-taxonomy.md`

---

### 4. Density Levels (The "How Much")

| Level | Corruption | Rest | Use Case |
|-------|------------|------|----------|
| Sparse | 20-30% | 70-80% | Subtle, elegant |
| Moderate | 40-50% | 50-60% | Balanced |
| Dense | 65-75% | 25-35% | Intense |
| Overloaded | 80-90% | 10-20% | Extreme |
| Pile-Up | 90-100% | 0-10% | Maximum chaos |

**Full details:** `core/signal-density-system.md`

---

### 5. Anchor Preservation (The "What Survives")

The rule: **Preserve one hot anchor, injure everything else.**

**Face Priority:**
1. Eyes (most critical)
2. Mouth/lips
3. Nose bridge
4. Face center
5. Jawline

**Body Priority:**
1. Torso center
2. Gesture arcs
3. Shoulder line
4. Head position

**Full details:** `subject/face-and-body-anchor-profiles.md` + `subject/region-priority-map.md`

---

## Common Workflows

### Workflow 1: Create a New Glitchcore Config

1. **Pick subtype** → `core/subcategories-reference-index.md`
2. **Choose palette** → `core/palette-energy-system.md`
3. **Select drivers** → `core/artifact-driver-taxonomy.md`
4. **Set density** → `core/signal-density-system.md`
5. **Define anchors** → `subject/face-and-body-anchor-profiles.md`
6. **Write JSON** → `technical/sample-json-bundles.md` for examples

---

### Workflow 2: Fix a Drifted Output

1. **Identify drift type** → `quality/drift-rescue-recipes.md` (Section 11)
2. **Apply rescue recipe** → Specific fix in that file
3. **Adjust parameters** → `language/style-language-to-code-translation.md`
4. **Verify anchors** → `subject/region-priority-map.md`

---

### Workflow 3: Add Audio Reactivity

1. **Pick audio mode** → `audio/music-mode-profiles.md` (Section 1)
2. **Map frequencies** → Frequency-to-visual mapping in that file
3. **Set state switches** → Chorus/verse/drop behavior
4. **Test with music** → Adjust thresholds

---

### Workflow 4: Translate Description to Code

1. **Parse emotion tags** → `language/glam-pop-glitch-vocabulary.md`
2. **Map to drivers** → `language/style-language-to-code-translation.md`
3. **Set parameters** → Parameter tables in that file
4. **Generate config** → JSON structure from `technical/sample-json-bundles.md`

---

## Key Principles (The "Rules")

### 1. The Anchor Rule
> **Preserve one hot anchor, injure everything else first.**

Corruption should feel like it's attacking the periphery while the center holds.

---

### 2. The Palette Hierarchy Rule
> **One dominant, one collision, one accent. No rainbow soup.**

Every palette needs clear color roles. Equal-strength colors create chaos, not intention.

---

### 3. The Driver Hierarchy Rule
> **One primary driver leads, 2-3 secondary drivers support.**

Don't pile up effects equally. Let one driver define the look, others complement.

---

### 4. The Beauty vs Damage Rule
> **The tension between beauty and damage creates the aesthetic.**

Pure beauty is boring. Pure damage is ugly. The friction between them is glitchcore.

---

### 5. The Temporal Hierarchy Rule
> **Present frame brightest, past fades exponentially.**

Time-based effects need clear hierarchy. Equal opacity = no present moment.

---

## Drift Types (What Can Go Wrong)

| Drift | Symptom | Fix |
|-------|---------|-----|
| Face Destruction | Face unrecognizable | `quality/drift-rescue-recipes.md` Section 1 |
| Beauty Ad | Too polished, filter-like | `quality/drift-rescue-recipes.md` Section 2 |
| Rainbow Soup | All colors equal | `quality/drift-rescue-recipes.md` Section 3 |
| Generic Filter | Could be any glitch app | `quality/drift-rescue-recipes.md` Section 4 |
| Motion Blur | Generic blur, no frames | `quality/drift-rescue-recipes.md` Section 5 |
| Poster Design | Text too designed | `quality/drift-rescue-recipes.md` Section 6 |
| Cinematic CCTV | Too movie-like | `quality/drift-rescue-recipes.md` Section 7 |
| Op Art | Pattern too uniform | `quality/drift-rescue-recipes.md` Section 8 |
| Bad Quality | Just ugly, not aesthetic | `quality/drift-rescue-recipes.md` Section 9 |
| Effect Soup | No driver hierarchy | `quality/drift-rescue-recipes.md` Section 10 |

---

## Emotion → Subtype Quick Map

| Emotion | Subtype | Palette |
|---------|---------|---------|
| Seductive | Candy Broadcast | Hyperpop Rupture |
| Bratty | Candy Crash | Codec Candy Crash |
| Dreamy | Pastel Smear | Pastel Signal Melt |
| Electric | RGB Phantom | Rainbow Channel |
| Lonely | Text Screen | Gloss Electric Glam |
| Glamorous | Glitter Signal | Gloss Electric Glam |
| Haunted | Ghost Frame | Gloss Electric Glam |
| Eerie | Surveillance | Phosphor Noir |
| Iconic | CRT Contour | Phosphor Noir |
| Decadent | Composite | Rainbow Channel |

---

## File Relationships

```
core/subcategories-reference-index.md
    ├── core/palette-energy-system.md
    ├── core/artifact-driver-taxonomy.md
    ├── core/signal-density-system.md
    └── subject/face-and-body-anchor-profiles.md

technical/sample-json-bundles.md
    ├── All core files (examples reference everything)

language/style-language-to-code-translation.md
    ├── language/glam-pop-glitch-vocabulary.md (emotion terms)
    ├── core/palette-energy-system.md (color codes)
    ├── core/artifact-driver-taxonomy.md (driver codes)
    └── core/signal-density-system.md (density codes)

quality/drift-rescue-recipes.md
    ├── References all files for fixes
    └── Cross-references specific sections
```

---

## For AI Implementation

When generating glitchcore outputs:

1. **Always start with subtype** — Don't apply generic "glitch"
2. **Always define palette hierarchy** — Dominant, collision, accent
3. **Always preserve one hot anchor** — Usually eyes for faces
4. **Always have driver hierarchy** — One primary, 2-3 secondary
5. **Always check for drift** — Compare output to drift types

**Example prompt structure:**
```
"[subtype] with [primary_driver] and [secondary_drivers], 
[palette_family] palette, [density_level] density, 
preserve [anchors], [emotion_tags] mood"
```

---

## Version & Credits

**System Version:** 1.0

**Core Principles:**
- Seductive signal damage
- Beauty vs corruption tension
- One hot anchor preservation
- Palette hierarchy
- Driver hierarchy

**Philosophy:**
> Make the theory executable. Turn poetry into parameters without killing the poetry.

---

## Short Anchor Rule

**Start with the index. Follow the system. Trust the tension.**
