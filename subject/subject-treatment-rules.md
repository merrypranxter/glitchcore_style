# Subject Treatment Rules

Guidelines for how glitchcore should treat different subject types (faces, bodies, objects, scenes, abstract forms).

## Purpose

This file defines how the glitchcore system should handle different kinds of subjects — faces, bodies, objects, scenes, and abstract forms — so that the corruption feels intentional, not random.

This is the part that helps the app stop going:
"just apply glitch to everything"
and start going:
"this subject needs this kind of corruption logic."

The rules here are designed to make the corruption feel like it's responding to the subject's structure, not just decorating it.

---

## 1. Face Treatment Rules

### 1.1 General Face Philosophy

Faces are the most emotionally loaded subject in glitchcore. The corruption must feel like it's attacking or destabilizing the face, not just decorating it.

**Core Principle:**
- Preserve one hot anchor (usually eyes or mouth)
- Injure everything else first
- Make the corruption feel like it's coming from the periphery inward

### 1.2 Face Zone Priority Map

```
PRESERVE HIGH (Hot Anchors):
├── Eyes (most critical)
├── Mouth/lips
└── Nose bridge

PRESERVE MEDIUM (Warm Anchors):
├── Jawline
├── Face center
└── Cheekbone structure

DISTORT FIRST (Cool Zones):
├── Hair edges
├── Outer face planes
├── Cheeks (soft tissue)
├── Duplicate planes
└── Outer silhouette
```

### 1.3 Face-Specific Driver Behavior

| Driver | Face Behavior |
|--------|---------------|
| Channel Split | Wider offset at edges, tighter at eyes |
| Overprint Stacking | Stack duplicates outward from face center |
| Bloom Contamination | Glow strongest at cheeks/jaw, avoid eye clarity kill |
| Temporal Echo | Echo trails follow head movement, not random |
| Compression Chew | Block damage hits hair/edges first |

### 1.4 Face Drift Risks

- **Beauty Ad Drift:** Corruption becomes cosmetic polish
- **Rainbow Clown Soup:** Too many equal-strength colors
- **Generic Portrait Filter:** Glitch feels like Instagram overlay
- **Face Erasure:** Corruption destroys all facial structure

---

## 2. Body Treatment Rules

### 2.1 General Body Philosophy

Bodies in glitchcore should feel kinetic, sensual, or ceremonial. The corruption should emphasize movement, gesture, or pose — not just damage the figure.

**Core Principle:**
- Preserve gesture arcs and pose silhouettes
- Let corruption emphasize movement, not freeze it
- Make the body feel like it's dissolving into motion

### 2.2 Body Zone Priority Map

```
PRESERVE HIGH (Gesture Anchors):
├── Dominant pose line
├── Gesture arcs (arms, legs in motion)
└── Torso center line

PRESERVE MEDIUM (Figure Anchors):
├── Head position
├── Shoulder line
└── Hip line

DISTORT FIRST (Movement Zones):
├── Limb trails
├── Motion blur regions
├── Echo stack areas
└── Peripheral body edges
```

### 2.3 Body-Specific Driver Behavior

| Driver | Body Behavior |
|--------|---------------|
| Temporal Echo | Stack follows movement direction, fades backward |
| Ghost Frame | Multiple poses visible, current pose brightest |
| Channel Split | Offset emphasizes motion direction |
| Bloom Contamination | Glow pools at joints and movement peaks |
| Compression Chew | Block damage hits fast-moving regions hardest |

### 2.4 Body Drift Risks

- **Generic Motion Blur:** Just looks like camera shake
- **Equal Opacity Stack:** All frames same weight, no present moment
- **Frozen Ghost:** Body looks static, not kinetic
- **Figure Erasure:** Corruption destroys body silhouette

---

## 3. Object Treatment Rules

### 3.1 General Object Philosophy

Objects in glitchcore should feel like they're malfunctioning, not just damaged. The corruption should suggest the object is behaving wrong — screens showing wrong images, devices outputting noise.

**Core Principle:**
- Preserve object recognition (what is this?)
- Corrupt function and surface
- Make the object feel possessed by wrong signals

### 3.2 Object Type Behaviors

| Object Type | Corruption Logic |
|-------------|------------------|
| Screens/Monitors | Wrong content, scanline damage, phosphor bleed |
| Phones/Devices | Interface debris, notification ghosts, cracked glass |
| Vehicles | Motion trails, speed distortion, light streaks |
| Furniture | Surface texture corruption, impossible reflections |
| Clothing | Fabric pattern glitch, seam breaks, material confusion |

### 3.3 Object Drift Risks

- **Generic Damage:** Looks like physical destruction, not signal corruption
- **Unrecognizable:** Object becomes abstract shape
- **Decorative Glitch:** Corruption feels like sticker, not malfunction

---

## 4. Scene Treatment Rules

### 4.1 General Scene Philosophy

Scenes in glitchcore should feel like spaces where reality is unstable. The corruption should suggest the environment itself is generating wrong signals.

**Core Principle:**
- Preserve spatial depth cues
- Corrupt surfaces and atmospheres
- Make the space feel like it's broadcasting errors

### 4.2 Scene Element Behaviors

| Scene Element | Corruption Logic |
|---------------|------------------|
| Architecture | Surface pattern glitch, impossible geometry, reflection errors |
| Nature | Color wrongness, texture repetition, organic signal noise |
| Interiors | Light source corruption, shadow errors, surface contamination |
| Exteriors | Sky banding, horizon distortion, atmospheric signal noise |

### 4.3 Scene Drift Risks

- **Generic Filter:** Looks like color grading, not corruption
- **Flat Chaos:** No depth preservation, just noise soup
- **Unrecognizable Space:** Can't tell what kind of place this is

---

## 5. Abstract Form Treatment Rules

### 5.1 General Abstract Philosophy

Abstract forms in glitchcore should feel like pure signal behavior — corruption as the subject itself, not corruption of something else.

**Core Principle:**
- Let corruption define the form
- No preservation rules needed
- Make the artifact the aesthetic

### 5.2 Abstract Form Behaviors

| Form Type | Corruption Logic |
|-----------|------------------|
| Geometric | Pattern break, repetition errors, alignment glitches |
| Organic | Texture corruption, edge instability, growth errors |
| Textural | Surface noise, pattern repetition, material confusion |
| Chromatic | Color field collision, gradient banding, hue instability |

### 5.3 Abstract Drift Risks

- **Generic Noise:** Just looks like random pixels
- **No Structure:** No form to corrupt, just chaos
- **Decorative Pattern:** Looks like wallpaper, not glitch

---

## 6. Hybrid Subject Rules

### 6.1 Face + Body Hybrids

When both face and body are present:
- Face rules take priority for preservation
- Body rules guide motion and gesture
- Corruption flows from body toward face, not equally

### 6.2 Face + Object Hybrids

When face and object interact:
- Preserve face hot anchors
- Let object corruption echo face palette
- Make object feel like it's reflecting face signals

### 6.3 Body + Scene Hybrids

When body exists in space:
- Preserve body gesture and pose
- Let scene corruption emphasize body movement
- Make space feel like it's responding to body motion

---

## 7. Subject-Aware Driver Selection

### 7.1 Face-First Drivers

Best for faces:
- Channel Split (with edge bias)
- Overprint Stacking (outward from center)
- Bloom Contamination (peripheral glow)
- Compression Chew (edge-first damage)

### 7.2 Body-First Drivers

Best for bodies:
- Temporal Echo (motion trails)
- Ghost Frame (multi-pose visibility)
- Channel Split (motion-direction offset)
- Bloom Contamination (joint/movement glow)

### 7.3 Object-First Drivers

Best for objects:
- Text Interface Debris (screen/device corruption)
- Compression Chew (digital artifact)
- Scanline Contour (CRT/monitor behavior)
- Capture Degradation (surveillance feed)

### 7.4 Scene-First Drivers

Best for scenes:
- Color Field Collision (atmospheric)
- Compression Chew (surface damage)
- Noise Veil (atmospheric signal)
- Temporal Echo (environmental motion)

---

## 8. Summary Table: Subject → Driver Mapping

| Subject | Primary Drivers | Secondary Drivers | Avoid |
|---------|-----------------|-------------------|-------|
| Face | Channel Split, Overprint | Bloom, Compression | Temporal Echo (heavy) |
| Body | Temporal Echo, Ghost Frame | Channel Split, Bloom | Text Interface |
| Object | Text Interface, Compression | Scanline, Capture | Overprint Stacking |
| Scene | Color Collision, Compression | Noise Veil, Temporal | Overprint (unless text) |
| Abstract | Any driver can lead | Mix freely | None specifically |

---

## 9. Short Anchor Rule

**Let the subject guide the corruption, not the other way around.**
