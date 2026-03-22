# Face and Body Anchor Profiles

Pre-configured anchor preservation settings for different subject types and compositions.

## Purpose

This file provides ready-to-use anchor preservation configurations for common subject types in glitchcore — different face angles, body poses, and compositions.

This is the part that helps the app stop going:
"how do I know what to preserve?"
and start going:
"frontal face = preserve eyes, mouth, nose bridge."

The profiles here are designed to make anchor preservation automatic and intelligent based on subject type.

---

## 1. Face Anchor Profiles

### 1.1 Frontal Face (Standard)

**Profile ID:** `face_frontal_standard`

**Preserve High:**
- Both eyes
- Mouth/lips
- Nose bridge

**Preserve Medium:**
- Face center
- Jawline
- Cheekbones

**Distort First:**
- Hair edges
- Temples
- Outer face planes
- Cheeks (soft tissue)
- Neck

**Recommended Drivers:**
- Primary: Channel Split
- Secondary: Overprint Stacking, Bloom Contamination

**Notes:**
- Most common face type
- Symmetric preservation
- Corruption flows inward from edges

---

### 1.2 Profile Face (Side View)

**Profile ID:** `face_profile`

**Preserve High:**
- Visible eye socket
- Lips/mouth (if visible)
- Nose bridge
- Profile line

**Preserve Medium:**
- Forehead
- Jawline
- Ear (if visible)

**Distort First:**
- Back of head
- Hair (full)
- Neck
- Far cheek

**Recommended Drivers:**
- Primary: Channel Split
- Secondary: Temporal Echo, Bloom

**Notes:**
- Profile line is critical anchor
- Less symmetry to work with
- Corruption emphasizes silhouette

---

### 1.3 Three-Quarter Face

**Profile ID:** `face_three_quarter`

**Preserve High:**
- Both eyes (near eye more than far eye)
- Near eye (critical)
- Mouth/lips
- Nose bridge

**Preserve Medium:**
- Near cheekbone
- Jawline (near side)
- Face center

**Distort First:**
- Far side of face
- Far eye (can take more damage)
- Far cheek
- Hair on far side
- Neck

**Recommended Drivers:**
- Primary: Channel Split
- Secondary: Overprint Stacking, Bloom

**Notes:**
- Asymmetric preservation
- Near side gets more protection
- Far side can take heavier corruption

---

### 1.4 Close-Up Face (Beauty Shot)

**Profile ID:** `face_closeup_beauty`

**Preserve High:**
- Both eyes (maximum protection)
- Lips (maximum protection)
- Nose bridge
- Cheekbones (structure)

**Preserve Medium:**
- Forehead
- Jawline
- Face center

**Distort First:**
- Hair edges
- Temples
- Outer face planes
- Neck (if visible)

**Recommended Drivers:**
- Primary: Channel Split (tight)
- Secondary: Bloom Contamination, Overprint

**Notes:**
- Maximum anchor preservation
- Corruption must feel cosmetic, not destructive
- Glamour emphasis

---

### 1.5 Partial Face (Cropped)

**Profile ID:** `face_partial`

**Preserve High:**
- Any visible eye
- Any visible mouth
- Most complete facial feature

**Preserve Medium:**
- Visible face structure
- Jawline (if visible)
- Cheekbones (if visible)

**Distort First:**
- Cropped edges
- Partial features
- Background visible through crop

**Recommended Drivers:**
- Primary: Channel Split
- Secondary: Bloom, Compression

**Notes:**
- Work with what's visible
- Cropped edges can take heavy damage
- Make partial feel intentional

---

## 2. Body Anchor Profiles

### 2.1 Standing Figure (Static)

**Profile ID:** `body_standing`

**Preserve High:**
- Head (see face profiles)
- Torso center
- Shoulder line

**Preserve Medium:**
- Hip line
- Upper arms
- Upper legs

**Distort First:**
- Hands
- Feet
- Lower arms
- Lower legs
- Hair
- Clothing edges

**Recommended Drivers:**
- Primary: Temporal Echo
- Secondary: Overprint, Bloom

**Notes:**
- Pose is the anchor
- Vertical structure preservation
- Corruption emphasizes stillness

---

### 2.2 Dancing Figure (Dynamic)

**Profile ID:** `body_dancing`

**Preserve High:**
- Head (see face profiles)
- Torso center (pose anchor)
- Lead gesture (arm/leg in motion)

**Preserve Medium:**
- Shoulder line
- Hip line
- Current pose silhouette

**Distort First:**
- Trail limbs (following motion)
- Echo regions
- Fast-moving parts
- Hair in motion

**Recommended Drivers:**
- Primary: Temporal Echo
- Secondary: Ghost Frame, Channel Split

**Notes:**
- Motion direction is critical
- Lead vs. trail distinction
- Corruption emphasizes movement

---

### 2.3 Reclining Figure

**Profile ID:** `body_reclining`

**Preserve High:**
- Head (see face profiles)
- Torso center
- Hip anchor point

**Preserve Medium:**
- Shoulder line
- Leg line
- Body curve

**Distort First:**
- Extended limbs
- Feet
- Hands
- Hair spread
- Background contact points

**Recommended Drivers:**
- Primary: Bloom Contamination
- Secondary: Overprint, Temporal Echo

**Notes:**
- Horizontal composition
- Body curve is anchor
- Soft, flowing corruption

---

### 2.4 Action Figure (Sports/Movement)

**Profile ID:** `body_action`

**Preserve High:**
- Head (see face profiles)
- Action focal point (ball, equipment, contact)
- Torso center

**Preserve Medium:**
- Shoulder line
- Hip line
- Supporting limbs

**Distort First:**
- Fast-moving limbs
- Motion blur regions
- Background
- Equipment trails

**Recommended Drivers:**
- Primary: Temporal Echo
- Secondary: Ghost Frame, Channel Split

**Notes:**
- Action moment is anchor
- Speed emphasis
- Corruption emphasizes motion

---

### 2.5 Portrait with Body (Medium Shot)

**Profile ID:** `body_portrait_medium`

**Preserve High:**
- Face (see face profiles)
- Shoulders
- Upper chest

**Preserve Medium:**
- Arms (upper)
- Neck
- Torso top

**Distort First:**
- Lower body (if visible)
- Hands
- Background
- Clothing details

**Recommended Drivers:**
- Primary: Channel Split
- Secondary: Bloom, Overprint

**Notes:**
- Face priority over body
- Upper body preservation
- Corruption flows downward

---

## 3. Composition Anchor Profiles

### 3.1 Single Subject Centered

**Profile ID:** `comp_single_center`

**Preserve High:**
- Subject face
- Subject center

**Preserve Medium:**
- Subject full body
- Immediate background

**Distort First:**
- Far background
- Frame edges
- Corners

**Notes:**
- Classic composition
- Clear subject priority
- Radial corruption flow

---

### 3.2 Single Subject Off-Center

**Profile ID:** `comp_single_offcenter`

**Preserve High:**
- Subject face
- Subject center of mass

**Preserve Medium:**
- Subject full body
- Negative space

**Distort First:**
- Far from subject
- Opposite side of frame
- Background

**Notes:**
- Asymmetric composition
- Negative space is intentional
- Corruption respects negative space

---

### 3.3 Two Subjects

**Profile ID:** `comp_two_subjects`

**Preserve High:**
- Both faces
- Connection point between subjects

**Preserve Medium:**
- Both bodies
- Space between subjects

**Distort First:**
- Far background
- Outer edges
- Non-subject areas

**Notes:**
- Relationship is anchor
- Both subjects need preservation
- Corruption emphasizes connection

---

### 3.4 Group Shot

**Profile ID:** `comp_group`

**Preserve High:**
- Central figure(s) face(s)
- Group formation center

**Preserve Medium:**
- All visible faces
- Group silhouette

**Distort First:**
- Background
- Frame edges
- Partial figures

**Notes:**
- Group composition is anchor
- Central figures get more protection
- Corruption flows outward

---

### 3.5 Subject with Object

**Profile ID:** `comp_subject_object`

**Preserve High:**
- Subject face
- Object of interaction

**Preserve Medium:**
- Subject body
- Object context

**Distort First:**
- Background
- Non-interacting areas
- Frame edges

**Notes:**
- Interaction is anchor
- Both subject and object matter
- Corruption emphasizes relationship

---

## 4. Quick Reference: Profile Selection

### 4.1 Face Selection Guide

| Face Angle | Profile ID |
|------------|------------|
| Straight on | `face_frontal_standard` |
| Side view | `face_profile` |
| 3/4 turn | `face_three_quarter` |
| Beauty close-up | `face_closeup_beauty` |
| Cropped | `face_partial` |

### 4.2 Body Selection Guide

| Body Pose | Profile ID |
|-----------|------------|
| Standing still | `body_standing` |
| Dancing/moving | `body_dancing` |
| Lying down | `body_reclining` |
| Sports/action | `body_action` |
| Medium portrait | `body_portrait_medium` |

### 4.3 Composition Selection Guide

| Composition | Profile ID |
|-------------|------------|
| Centered subject | `comp_single_center` |
| Off-center subject | `comp_single_offcenter` |
| Two people | `comp_two_subjects` |
| Group | `comp_group` |
| Subject + object | `comp_subject_object` |

---

## 5. Combining Profiles

### 5.1 Face + Body Combination

```
Primary: Face Profile (based on angle)
Secondary: Body Profile (based on pose)

Example: Frontal face + dancing body
- Preserve: Eyes, mouth (from face_frontal_standard)
- Preserve: Torso center, lead gesture (from body_dancing)
- Distort: Hair, trail limbs
```

### 5.2 Subject + Composition Combination

```
Primary: Subject Profile (face/body)
Secondary: Composition Profile

Example: Face profile + two subjects composition
- Preserve: Both faces (from comp_two_subjects)
- Preserve: Face features (from face profile)
- Distort: Background, outer edges
```

---

## 6. Custom Profile Creation

### 6.1 Template

```json
{
  "profile_id": "custom_[name]",
  "based_on": "[parent_profile_id]",
  "preserve_high": ["zone1", "zone2"],
  "preserve_medium": ["zone3", "zone4"],
  "distort_first": ["zone5", "zone6"],
  "recommended_drivers": {
    "primary": "[driver]",
    "secondary": ["driver1", "driver2"]
  },
  "notes": "[special considerations]"
}
```

### 6.2 Example Custom Profile

```json
{
  "profile_id": "custom_diva_performance",
  "based_on": "body_dancing",
  "preserve_high": [
    "face_eyes",
    "face_mouth",
    "torso_center",
    "lead_arm_gesture"
  ],
  "preserve_medium": [
    "face_structure",
    "shoulder_line",
    "costume_center"
  ],
  "distort_first": [
    "hair_motion",
    "trail_limbs",
    "costume_edges",
    "background"
  ],
  "recommended_drivers": {
    "primary": "temporal_echo",
    "secondary": ["overprint", "bloom", "sparkle"]
  },
  "notes": "For stage performance, emphasize motion and glamour"
}
```

---

## 7. Short Anchor Rule

**Know what you're preserving before you start corrupting.**
