# Glitchcore Style Repo — Structure Guide for Copilot

## Overview

This repository contains a comprehensive style system for glitchcore aesthetics — a bright, seductive, hyperpop-influenced approach to digital corruption and visual glitch art.

**Purpose:** Help AI systems generate glitchcore outputs that are emotionally specific, stylistically coherent, and technically implementable.

---

## File Organization

```
glitchcore-style-repo/
├── repo-structure.md              ← YOU ARE HERE
├── subcategories-reference-index.md   ← START HERE for subtype lookup
├── sample-json-bundles.md         ← Example configs for implementation
├──
├── CORE SYSTEM FILES
├── palette-energy-system.md       ← Color logic and emotional temperature
├── signal-density-system.md       ← How much corruption vs preservation
├── artifact-driver-taxonomy.md    ← All corruption mechanisms cataloged
├──
├── SUBJECT & COMPOSITION
├── subject-treatment-rules.md     ← How to treat faces, bodies, objects
├── face-and-body-anchor-profiles.md   ← Pre-configured anchor settings
├── region-priority-map.md         ← Zone-by-zone preservation rules
├──
├── STYLE TRANSLATION
├── style-language-to-code-translation.md  ← Turn descriptions into code
├── glam-pop-glitch-vocabulary.md  ← Emotional language for bright glitch
├──
├── SPECIALIZED SYSTEMS
├── text-screen-and-interface-debris.md    ← Text as visual corruption
├── compression-and-codec-corruption.md    ← Digital damage aesthetics
├── temporal-echo-and-motion-stacks.md     ← Time-based glitch
├──
├── AUDIO & INTERACTIVITY
├── music-mode-profiles.md         ← Audio-reactive behavior maps
├──
└── TROUBLESHOOTING
    └── drift-rescue-recipes.md    ← Fixes for when outputs go wrong
```

---

## Quick Start Paths

### "I need to pick a glitch style"
→ `subcategories-reference-index.md`

### "I need to understand color choices"
→ `palette-energy-system.md`

### "I need to know what corruption effects to use"
→ `artifact-driver-taxonomy.md`

### "I need to preserve a face properly"
→ `face-and-body-anchor-profiles.md` + `region-priority-map.md`

### "I need to make it react to music"
→ `music-mode-profiles.md`

### "I need to add text debris"
→ `text-screen-and-interface-debris.md`

### "I need compression damage"
→ `compression-and-codec-corruption.md`

### "I need motion trails"
→ `temporal-echo-and-motion-stacks.md`

### "The output looks wrong"
→ `drift-rescue-recipes.md`

### "I need example code/configs"
→ `sample-json-bundles.md`

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

**Full details:** `subcategories-reference-index.md`

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

**Full details:** `palette-energy-system.md`

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

**Full details:** `artifact-driver-taxonomy.md`

---

### 4. Density Levels (The "How Much")

| Level | Corruption | Rest | Use Case |
|-------|------------|------|----------|
| Sparse | 20-30% | 70-80% | Subtle, elegant |
| Moderate | 40-50% | 50-60% | Balanced |
| Dense | 65-75% | 25-35% | Intense |
| Overloaded | 80-90% | 10-20% | Extreme |
| Pile-Up | 90-100% | 0-10% | Maximum chaos |

**Full details:** `signal-density-system.md`

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

**Full details:** `face-and-body-anchor-profiles.md` + `region-priority-map.md`

---

## Common Workflows

### Workflow 1: Create a New Glitchcore Config

1. **Pick subtype** → `subcategories-reference-index.md`
2. **Choose palette** → `palette-energy-system.md`
3. **Select drivers** → `artifact-driver-taxonomy.md`
4. **Set density** → `signal-density-system.md`
5. **Define anchors** → `face-and-body-anchor-profiles.md`
6. **Write JSON** → `sample-json-bundles.md` for examples

---

### Workflow 2: Fix a Drifted Output

1. **Identify drift type** → `drift-rescue-recipes.md` (Section 11)
2. **Apply rescue recipe** → Specific fix in that file
3. **Adjust parameters** → `style-language-to-code-translation.md`
4. **Verify anchors** → `region-priority-map.md`

---

### Workflow 3: Add Audio Reactivity

1. **Pick audio mode** → `music-mode-profiles.md` (Section 1)
2. **Map frequencies** → Frequency-to-visual mapping in that file
3. **Set state switches** → Chorus/verse/drop behavior
4. **Test with music** → Adjust thresholds

---

### Workflow 4: Translate Description to Code

1. **Parse emotion tags** → `glam-pop-glitch-vocabulary.md`
2. **Map to drivers** → `style-language-to-code-translation.md`
3. **Set parameters** → Parameter tables in that file
4. **Generate config** → JSON structure from `sample-json-bundles.md`

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
| Face Destruction | Face unrecognizable | `drift-rescue-recipes.md` Section 1 |
| Beauty Ad | Too polished, filter-like | `drift-rescue-recipes.md` Section 2 |
| Rainbow Soup | All colors equal | `drift-rescue-recipes.md` Section 3 |
| Generic Filter | Could be any glitch app | `drift-rescue-recipes.md` Section 4 |
| Motion Blur | Generic blur, no frames | `drift-rescue-recipes.md` Section 5 |
| Poster Design | Text too designed | `drift-rescue-recipes.md` Section 6 |
| Cinematic CCTV | Too movie-like | `drift-rescue-recipes.md` Section 7 |
| Op Art | Pattern too uniform | `drift-rescue-recipes.md` Section 8 |
| Bad Quality | Just ugly, not aesthetic | `drift-rescue-recipes.md` Section 9 |
| Effect Soup | No driver hierarchy | `drift-rescue-recipes.md` Section 10 |

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
subcategories-reference-index.md
    ├── palette-energy-system.md
    ├── artifact-driver-taxonomy.md
    ├── signal-density-system.md
    └── face-and-body-anchor-profiles.md

sample-json-bundles.md
    ├── All core files (examples reference everything)

style-language-to-code-translation.md
    ├── glam-pop-glitch-vocabulary.md (emotion terms)
    ├── palette-energy-system.md (color codes)
    ├── artifact-driver-taxonomy.md (driver codes)
    └── signal-density-system.md (density codes)

drift-rescue-recipes.md
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
