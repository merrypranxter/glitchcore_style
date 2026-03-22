# Drift Rescue Recipes

Specific fixes for when glitchcore outputs drift into unwanted territory.

## Purpose

This file provides concrete, actionable fixes for when glitchcore outputs drift away from the intended aesthetic — when the corruption becomes too much, too little, or just wrong.

This is the part that helps the app stop going:
"this doesn't look right but I don't know why"
and start going:
"the face is getting destroyed → apply face_anchor_restore recipe."

The recipes here are designed to be diagnostic and prescriptive — identify the problem, apply the fix.

---

## 1. Face Destruction Drift

### 1.1 Problem

The face is being destroyed by corruption. Eyes, mouth, or facial structure is unrecognizable.

### 1.2 Diagnosis

- Eyes are obscured or distorted
- Mouth is unrecognizable
- Face structure is collapsed
- Subject looks like a different person or no person

### 1.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Reduce primary_driver strength by 30%
2. Add face_anchor_restore pass
3. Increase preserve_high zone protection
4. Reduce edge_bias on channel_split

PARAMETER CHANGES:
- primary_driver_strength: current * 0.7
- face_protection: 0.8 (was 0.5)
- edge_bias: 0.3 (was 0.7)
- add_pass: face_anchor_restore

ZONE ADJUSTMENTS:
- eyes: protection +0.3
- mouth: protection +0.3
- face_center: protection +0.2
```

### 1.4 Prevention

- Always set face protection before applying drivers
- Use face_anchor_profiles for guidance
- Test on face-heavy images first

---

## 2. Beauty Ad Drift

### 2.1 Problem

The output looks like a beauty advertisement with a glitch filter applied — too polished, too clean, corruption feels cosmetic.

### 2.2 Diagnosis

- Face is perfectly preserved
- Corruption looks like an Instagram filter
- Colors are harmonious in a boring way
- No tension between beauty and damage
- Looks like it could be in a magazine

### 2.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Add one "rude" corruption zone
2. Increase primary_driver strength by 20%
3. Reduce face_protection slightly
4. Add compression_chew or text_interface_debris

PARAMETER CHANGES:
- primary_driver_strength: current * 1.2
- face_protection: 0.6 (was 0.8)
- add_driver: compression_chew at 0.4
- add_zone: one_injury_zone_on_face

AESTHETIC ADJUSTMENTS:
- palette: increase collision contrast
- emotion_tags: add "unstable" or "broken"
- media_source: change to "screenshot_repost"
```

### 2.4 Prevention

- Always include at least one injury zone
- Don't over-preserve the face
- Use bratty or broken emotion tags

---

## 3. Rainbow Clown Soup Drift

### 3.1 Problem

Too many colors of equal strength — looks like a rainbow exploded, no palette hierarchy.

### 3.2 Diagnosis

- All colors equally bright
- No dominant hue family
- No clear collision hue
- Looks like a children's toy or circus
- No emotional direction from color

### 3.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Establish palette hierarchy
2. Reduce color count
3. Pick one dominant, one collision, one accent
4. Reduce saturation on non-dominant colors

PARAMETER CHANGES:
- dominant_hue_saturation: 0.9
- collision_hue_saturation: 0.6
- accent_saturation: 1.0
- other_colors: reduce to 0.3 or remove

PALETTE RESTRUCTURE:
- dominant: [choose one]
- collision: [choose one, complementary]
- accent: [white or single highlight]
- eliminate: all other strong colors
```

### 3.4 Prevention

- Always define palette structure before applying
- Use palette_family presets
- Limit to 3 main colors maximum

---

## 4. Generic Filter Drift

### 4.1 Problem

The corruption looks like a generic filter — chromatic aberration overlay, scanline texture, etc. No unique identity.

### 4.2 Diagnosis

- Could be any "glitch" app
- No subtype personality
- Effect feels like a sticker
- No relationship between corruption and subject
- Looks like a tutorial example

### 4.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Add subtype-specific drivers
2. Change emotion_tags to be specific
3. Add media_source context
4. Combine multiple drivers uniquely

PARAMETER CHANGES:
- add_driver: subtype_secondary_driver
- emotion_tags: [specific, not generic]
- media_source: [specific context]
- driver_combination: unique_mix

IDENTITY ADJUSTMENTS:
- reference: specific_subtype_definition
- add: signature_behavior
- remove: generic_overlay_effects
```

### 4.4 Prevention

- Always start with subtype selection
- Use specific emotion tags
- Combine drivers in unique ways

---

## 5. Motion Blur Drift (Ghost Frame)

### 5.1 Problem

Ghost frame or temporal echo looks like generic motion blur — all frames equal opacity, no present moment.

### 5.2 Diagnosis

- All echo frames same brightness
- No clear "current" frame
- Looks like camera motion blur
- No temporal hierarchy
- Subject looks frozen in blur

### 5.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Establish present frame dominance
2. Create opacity falloff curve
3. Add temporal hierarchy
4. Reduce echo count if needed

PARAMETER CHANGES:
- present_frame_brightness: 1.0
- echo_1_opacity: 0.5
- echo_2_opacity: 0.3
- echo_3_opacity: 0.15
- fade_curve: exponential

TEMPORAL ADJUSTMENTS:
- echo_count: reduce to 3-5
- direction_bias: motion_following
- persistence: reduce for clarity
```

### 5.4 Prevention

- Always make present frame brightest
- Use exponential fade curves
- Limit echo count

---

## 6. Poster Design Drift (Text)

### 6.1 Problem

Text feels like a poster design — too legible, too composed, too intentional.

### 6.2 Diagnosis

- Text is perfectly readable
- Text placement feels designed
- Font is too nice
- Text doesn't overlap body
- Looks like graphic design, not debris

### 6.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Reduce text legibility
2. Add text-body overlap
3. Use worse fonts
4. Add repetition and fragmentation

PARAMETER CHANGES:
- legibility: 0.4 (was 0.8)
- overlap_bias: 0.7 (was 0.2)
- font_style: terminal_or_degraded
- repetition: 0.6 (was 0.2)

TEXT ADJUSTMENTS:
- add: phrase_fragments
- add: subtitle_ghosting
- remove: clean_typography
- add: compression_damage_to_text
```

### 6.4 Prevention

- Text should feel found, not designed
- Always include body overlap
- Use degraded/terminal fonts

---

## 7. Cinematic Movie Still Drift (Surveillance)

### 7.1 Problem

Surveillance footage looks like a cinematic movie still — too composed, too high quality, too intentional.

### 7.2 Diagnosis

- Image is too clear
- Lighting is too good
- Composition is too perfect
- No sense of being watched
- Looks like a film production

### 7.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Reduce overall quality
2. Add noise and degradation
3. Flatten lighting
4. Add institutional framing

PARAMETER CHANGES:
- quality: 0.4 (was 0.8)
- noise_level: 0.6
- lighting: flat_institutional
- composition: awkward_cctv_angle

DEGRADATION ADJUSTMENTS:
- add: capture_degradation
- add: compression_artifacts
- add: weak_feed_character
- remove: cinematic_lighting
```

### 7.4 Prevention

- Use low-quality source aesthetic
- Flat, institutional lighting
- Awkward angles

---

## 8. Op Art Wallpaper Drift (CRT)

### 8.1 Problem

CRT contour looks like op art or wallpaper — pattern is too perfect, too decorative, no subject relationship.

### 8.2 Diagnosis

- Scanlines are uniform
- Pattern dominates subject
- No contour following
- Looks like a filter overlay
- No phosphor or CRT character

### 8.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Make scanlines follow contours
2. Add phosphor bloom
3. Reduce pattern uniformity
4. Add CRT-specific artifacts

PARAMETER CHANGES:
- contour_following: 0.8 (was 0.2)
- phosphor_glow: 0.6
- pattern_variance: 0.5
- add: screen_curvature

CRT ADJUSTMENTS:
- add: phosphor_bloom
- add: faint_static_veil
- add: subtle_flicker
- remove: uniform_pattern
```

### 8.4 Prevention

- Scanlines must follow subject contours
- Add phosphor glow
- Include CRT-specific artifacts

---

## 9. Bad Quality for Its Own Sake Drift

### 9.1 Problem

Compression damage looks like bad quality for its own sake — no beauty, no tension, just ugly.

### 9.2 Diagnosis

- Image is just low quality
- No beauty zone preserved
- No color clarity
- Looks like a mistake
- No aesthetic intention

### 9.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Establish one beauty zone
2. Preserve color clarity somewhere
3. Add glamour element
4. Create beauty vs damage tension

PARAMETER CHANGES:
- beauty_zone: [eyes_or_mouth]
- color_clarity_point: one_hot_spot
- add: bloom_or_gloss
- damage_focus: peripheral

TENSION ADJUSTMENTS:
- preserve: one_glamorous_element
- damage: everything_else
- add: emotional_contrast
- remove: uniform_degradation
```

### 9.4 Prevention

- Always preserve one beauty anchor
- Maintain color clarity somewhere
- Create intentional tension

---

## 10. Random Effect Soup Drift

### 10.1 Problem

Too many effects with no hierarchy — looks like everything was applied, no primary driver.

### 10.2 Diagnosis

- All drivers equally strong
- No clear primary effect
- Visual chaos without structure
- Can't identify what's happening
- Looks like a demo reel

### 10.3 Rescue Recipe

```
IMMEDIATE ACTIONS:
1. Pick one primary driver
2. Reduce all others to secondary
3. Establish driver hierarchy
4. Remove unnecessary drivers

PARAMETER CHANGES:
- primary_driver_strength: 0.8
- secondary_driver_strength: 0.4
- tertiary_driver_strength: 0.2
- remove_drivers: non_essential

HIERARCHY ADJUSTMENTS:
- primary: [one_driver]
- secondary: [1-2_drivers]
- remove: [excess_drivers]
- add: driver_relationship_logic
```

### 10.4 Prevention

- Always have one clear primary driver
- Limit secondary drivers to 2-3
- Remove drivers that don't serve the subtype

---

## 11. Quick Reference: Drift Type → Recipe

| Drift Type | Recipe Section | Key Fix |
|------------|----------------|---------|
| Face destroyed | 1 | Face anchor restore |
| Too polished | 2 | Add injury zone |
| Rainbow soup | 3 | Palette hierarchy |
| Generic filter | 4 | Subtype specificity |
| Motion blur | 5 | Present frame dominance |
| Poster text | 6 | Reduce legibility |
| Cinematic CCTV | 7 | Reduce quality |
| Op art CRT | 8 | Contour following |
| Just bad quality | 9 | Beauty zone |
| Effect soup | 10 | Driver hierarchy |

---

## 12. Short Anchor Rule

**When it drifts, diagnose before you fix.**
