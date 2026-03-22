# Region Priority Map

Zone-by-zone preservation and corruption rules for faces, bodies, and scenes.

## Purpose

This file defines exactly which regions of an image should be preserved, which should be corrupted first, and how the corruption should flow across the composition.

This is the part that helps the app stop going:
"apply glitch evenly everywhere"
and start going:
"protect the eyes, attack the edges, let corruption flow inward."

The maps here are designed to make glitchcore feel spatially intelligent — like the corruption knows where it is and what it's doing.

---

## 1. Face Region Priority Map

### 1.1 Standard Portrait Face

```
                    [HAIR - DISTORT FIRST]
                           │
        [TEMPLE] ────┬──── [FOREHEAD] ────┬──── [TEMPLE]
         DISTORT     │      MEDIUM         │     DISTORT
                     │                     │
    [EYE] ◄──────────┼─────────────────────┼──────────► [EYE]
   PRESERVE          │                     │          PRESERVE
   HIGH              │                     │          HIGH
                     │                     │
   [CHEEK] ──────────┼──── [NOSE] ─────────┼───────── [CHEEK]
    DISTORT          │    PRESERVE         │          DISTORT
                     │    HIGH             │
                     │                     │
   [CHEEKBONE] ──────┼─────────────────────┼───── [CHEEKBONE]
    MEDIUM           │                     │      MEDIUM
                     │                     │
        [MOUTH] ◄────┴─────────────────────┴────► [MOUTH]
       PRESERVE                                    PRESERVE
       HIGH                                       HIGH
                           │
                    [JAWLINE - MEDIUM]
                           │
                    [NECK - DISTORT FIRST]
```

### 1.2 Profile Face

```
                    [HAIR - DISTORT FIRST]
                           │
        [FOREHEAD] ────────┼──────── [BACK OF HEAD]
         MEDIUM            │          DISTORT
                         │
    [EYE SOCKET] ◄─────────┼─────────► [EAR]
   PRESERVE               │          DISTORT
   HIGH                   │
                         │
   [NOSE BRIDGE] ─────────┼────────── [CHEEK BACK]
    PRESERVE              │           DISTORT
    HIGH                  │
                         │
   [LIPS/MOUTH] ◄─────────┴─────────── [JAW BACK]
  PRESERVE                              DISTORT
  HIGH
                         │
                    [NECK - DISTORT FIRST]
                         │
                    [SHOULDER - DISTORT FIRST]
```

### 1.3 Face Zone Definitions

| Zone | Priority | Why |
|------|----------|-----|
| Eyes | Preserve High | Emotional anchor, recognition point |
| Mouth/Lips | Preserve High | Expression, emotional communication |
| Nose Bridge | Preserve High | Facial structure anchor |
| Forehead | Medium | Structure, but less critical |
| Jawline | Medium | Face shape definition |
| Cheekbones | Medium | Structure, but can take damage |
| Cheeks (soft) | Distort First | Soft tissue, safe to corrupt |
| Temples | Distort First | Edge zone, peripheral |
| Hair | Distort First | Frame, can take heavy damage |
| Neck | Distort First | Transition zone |

---

## 2. Body Region Priority Map

### 2.1 Standing Figure

```
                    [HEAD - See Face Map]
                           │
              [NECK - MEDIUM]
                           │
    [SHOULDER] ◄───────────┼───────────► [SHOULDER]
   PRESERVE                │            PRESERVE
   MEDIUM                  │            MEDIUM
                           │
        [TORSO CENTER] ────┼──── [TORSO CENTER]
         PRESERVE          │      PRESERVE
         HIGH              │      HIGH
                           │
    [ARM UPPER] ───────────┼────────── [ARM UPPER]
     DISTORT               │           DISTORT
                           │
    [ARM LOWER] ───────────┼────────── [ARM LOWER]
     DISTORT               │           DISTORT
                           │
        [HAND] ◄───────────┴──────────► [HAND]
       PRESERVE                          PRESERVE
       MEDIUM                            MEDIUM
       (gesture anchor)                  (gesture anchor)
                           │
              [HIP] ───────┼────── [HIP]
               MEDIUM      │       MEDIUM
                           │
        [THIGH] ───────────┼────────── [THIGH]
         DISTORT           │           DISTORT
                           │
        [KNEE] ────────────┼────────── [KNEE]
         MEDIUM            │           MEDIUM
                           │
        [CALF] ────────────┼────────── [CALF]
         DISTORT           │           DISTORT
                           │
        [FOOT] ◄───────────┴──────────► [FOOT]
       PRESERVE                          PRESERVE
       MEDIUM                            MEDIUM
```

### 2.2 Dancing/Moving Figure

```
                    [HEAD - See Face Map]
                           │
              [NECK - MEDIUM]
                           │
    [SHOULDER] ◄───────────┼───────────► [SHOULDER]
   MEDIUM                  │            MEDIUM
   (motion origin)         │            (motion origin)
                           │
        [TORSO CENTER] ────┼──── [TORSO CENTER]
         PRESERVE          │      PRESERVE
         HIGH              │      HIGH
         (pose anchor)     │      (pose anchor)
                           │
    [ARM - TRAIL SIDE] ────┼────────── [ARM - LEAD SIDE]
     DISTORT               │           PRESERVE
     (follows motion)      │           MEDIUM
                           │           (gesture anchor)
        [HAND - TRAIL] ────┼──────── [HAND - LEAD]
         DISTORT           │           PRESERVE
         (echo)            │           MEDIUM
                           │           (gesture anchor)
              [HIP] ───────┼────── [HIP]
               MEDIUM      │       MEDIUM
               (pose line) │       (pose line)
                           │
        [LEG - TRAIL] ─────┼──────── [LEG - LEAD]
         DISTORT           │           PRESERVE
         (echo)            │           MEDIUM
                           │           (pose anchor)
        [FOOT - TRAIL] ────┴──────── [FOOT - LEAD]
         DISTORT                       PRESERVE
         (echo)                        MEDIUM
                                      (pose anchor)
```

### 2.3 Body Zone Definitions

| Zone | Priority | Why |
|------|----------|-----|
| Torso Center | Preserve High | Body anchor, pose definition |
| Shoulders | Preserve Medium | Frame, structure |
| Lead Hand/Foot | Preserve Medium | Gesture anchor, motion direction |
| Trail Limbs | Distort First | Echo zones, motion blur regions |
| Knees/Elbows | Medium | Joint definition, can take some damage |
| Upper Arms/Thighs | Distort First | Large surfaces, safe to corrupt |
| Lower Arms/Legs | Distort First | Peripheral, motion-heavy |

---

## 3. Scene Region Priority Map

### 3.1 Interior Space

```
    [CEILING - DISTORT FIRST]
              │
    [WALL UPPER] ───────── [WALL UPPER]
     DISTORT               DISTORT
              │
    [WALL MIDDLE] ──────── [WALL MIDDLE]
     MEDIUM                MEDIUM
              │
    [WALL LOWER] ───────── [WALL LOWER]
     DISTORT               DISTORT
              │
    [FLOOR - DISTORT FIRST]
              │
    [FOREGROUND OBJECTS - DISTORT FIRST]
```

### 3.2 Exterior Space

```
    [SKY - DISTORT FIRST]
              │
    [HORIZON LINE - PRESERVE MEDIUM]
              │
    [MIDGROUND] ────────── [MIDGROUND]
     DISTORT               DISTORT
              │
    [FOREGROUND] ───────── [FOREGROUND]
     MEDIUM                MEDIUM
              │
    [GROUND PLANE - DISTORT FIRST]
```

### 3.3 Scene Zone Definitions

| Zone | Priority | Why |
|------|----------|-----|
| Horizon Line | Preserve Medium | Depth anchor, spatial reference |
| Subject Position | Preserve High | Whatever the subject is |
| Foreground | Medium | Can take damage, but defines depth |
| Midground | Distort First | Large area, safe to corrupt |
| Background | Distort First | Furthest, heaviest corruption OK |
| Sky | Distort First | Atmospheric, can take heavy damage |
| Ground Plane | Distort First | Base, can take heavy damage |

---

## 4. Object Region Priority Map

### 4.1 Screen/Monitor

```
    [BEZEL - DISTORT FIRST]
              │
    [SCREEN EDGE] ──────── [SCREEN EDGE]
     DISTORT               DISTORT
              │
    [SCREEN CENTER] ────── [SCREEN CENTER]
     PRESERVE              PRESERVE
     MEDIUM                MEDIUM
     (content area)        (content area)
              │
    [SCREEN CONTENT] ───── [SCREEN CONTENT]
     PRESERVE              PRESERVE
     HIGH                  HIGH
     (what's displayed)    (what's displayed)
```

### 4.2 Phone/Device

```
    [CASE/EDGE - DISTORT FIRST]
              │
    [SCREEN] ───────────── [SCREEN]
     PRESERVE               PRESERVE
     HIGH                   HIGH
     (interface)            (interface)
              │
    [BUTTONS - MEDIUM]
```

---

## 5. Corruption Flow Patterns

### 5.1 Inward Flow (Face Default)

```
    Corruption starts at edges...
              │
        [HAIR] [TEMPLE]
              ↓
           [CHEEK]
              ↓
        [EYE] [MOUTH] ←─── Preserved center
```

### 5.2 Outward Flow (Explosion Default)

```
    Corruption starts at center...
              │
        [EYE] [MOUTH]
              ↓
           [CHEEK]
              ↓
        [HAIR] [TEMPLE] ←─── Heavy edge damage
```

### 5.3 Directional Flow (Motion Default)

```
    Motion direction → → →
              │
    [TRAIL]   [PRESENT]   [LEAD]
    DISTORT   PRESERVE    MEDIUM
    (echo)    (anchor)    (anticipation)
```

### 5.4 Layered Flow (Stack Default)

```
    Top layer (most preserved)
              │
        [CURRENT FRAME]
              ↓
        [ECHO 1]
              ↓
        [ECHO 2]
              ↓
    Bottom layer (most distorted)
        [ECHO 3+]
```

---

## 6. Region-Driver Matching

### 6.1 Face Regions → Drivers

| Region | Best Drivers |
|--------|--------------|
| Eyes | Channel Split (tight), Overprint (minimal) |
| Mouth | Bloom (subtle), Channel Split (tight) |
| Cheeks | Bloom (strong), Compression Chew |
| Hair | Channel Split (wide), Compression Chew |
| Face Edges | All drivers at full strength |

### 6.2 Body Regions → Drivers

| Region | Best Drivers |
|--------|--------------|
| Torso | Temporal Echo, Overprint |
| Lead Limbs | Temporal Echo (minimal), Channel Split (tight) |
| Trail Limbs | Temporal Echo (strong), Ghost Frame |
| Joints | Bloom (subtle), Channel Split |

### 6.3 Scene Regions → Drivers

| Region | Best Drivers |
|--------|--------------|
| Subject | See Face/Body maps |
| Foreground | Color Collision, Compression |
| Midground | All drivers |
| Background | All drivers, heavy |
| Sky | Color Collision, Noise Veil |

---

## 7. Priority Level Definitions

### 7.1 Preserve High
- Corruption must not destroy recognition
- Maximum 20% corruption in this zone
- Anchor restoration always applied
- Drift rescue triggered if violated

### 7.2 Preserve Medium
- Corruption can be noticeable
- Maximum 50% corruption in this zone
- Anchor restoration often applied
- Some drift acceptable

### 7.3 Distort First
- Corruption should concentrate here
- Up to 90% corruption acceptable
- No anchor restoration needed
- Let drivers run at full strength

---

## 8. Summary Table: Priority by Subject Type

| Zone | Face | Body | Scene | Object |
|------|------|------|-------|--------|
| Center | High | High | Medium | High |
| Edges | Distort | Distort | Distort | Distort |
| Motion Lead | N/A | Medium | N/A | N/A |
| Motion Trail | N/A | Distort | N/A | N/A |
| Frame | Distort | Medium | Distort | Distort |

---

## 9. Short Anchor Rule

**Corruption should know where it is and act accordingly.**
