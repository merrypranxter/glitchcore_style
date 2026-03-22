# Temporal Echo and Motion Stacks

Time-based glitch systems for movement, memory, and kinetic energy.

## Purpose

This file defines temporal glitchcore — how time becomes visible, how movement creates trails, and how memory lingers as visual corruption.

This is the part that helps the app stop going:
"add motion blur"
and start going:
"temporal echo with exponential fade, present frame dominance, motion-direction bias."

The temporal system here is designed to make time visible — not as a technical effect, but as emotional residue.

---

## 1. Temporal Philosophy

### 1.1 Core Principle

Time in glitchcore is not invisible. It's a visible layer.

The past lingers. The present flickers. The future echoes backward.

**Wrong:**
- Generic motion blur
- Equal opacity frames
- No present moment
- Camera shake

**Right:**
- Temporal hierarchy
- Present frame brightest
- Past fades exponentially
- Motion has direction

---

### 1.2 The Temporal Stack

```
PRESENT FRAME (brightest, sharpest)
    ↓
ECHO 1 (50% opacity, slight offset)
    ↓
ECHO 2 (25% opacity, more offset)
    ↓
ECHO 3 (12% opacity, further offset)
    ↓
ECHO 4+ (fading to invisible)
```

The present is always brightest. The past always fades.

---

## 2. Temporal Echo Types

### 2.1 Standard Temporal Echo

**What It Is:**
Previous frames linger as fading ghosts, creating a trail through time.

**Visual Character:**
- Fading copies of previous moments
- Exponential opacity falloff
- Present moment clearest
- Sense of history visible

**Parameters:**
```
echo_count: 2-10           # Number of historical frames
fade_curve: string         # "linear", "exponential", "ease_out"
opacity_start: 0.5-1.0     # First echo opacity
opacity_end: 0.0-0.1       # Last echo opacity
offset_direction: string   # "motion", "radial", "random"
```

**Best For:**
- Ghost frame body
- Dance and movement
- Memory aesthetics
- Time-visible moments

---

### 2.2 Motion-Directed Echo

**What It Is:**
Echoes follow the direction of movement, creating kinetic trails.

**Visual Character:**
- Trails follow motion vectors
- Echoes behind moving objects
- Directional, purposeful
- Sense of speed and energy

**Parameters:**
```
motion_detection: 0.0-1.0   # How motion is detected
trail_length: float         # How long trails extend
trail_fade: 0.0-1.0         # How fast trails fade
direction_lock: boolean     # Lock to specific direction
```

**Best For:**
- Action shots
- Dance
- Sports
- Any moving subject

---

### 2.3 Ghost Frame Stack

**What It Is:**
Multiple complete frames visible simultaneously, like a multi-exposure photograph.

**Visual Character:**
- Multiple poses visible
- Each frame semi-transparent
- Present pose brightest
- Sense of time compressed

**Parameters:**
```
frame_count: 2-8           # Number of frames visible
frame_spacing: float       # Time between frames
opacity_curve: string      # How opacity changes across frames
pose_variation: 0.0-1.0    # How different poses are
```

**Best For:**
- Dance photography
- Movement studies
- Time compression
- Multiple moments at once

---

### 2.4 Stutter Echo

**What It Is:**
Brief, sharp repeats at transient moments — like a record skip or digital stutter.

**Visual Character:**
- Sharp, brief duplicates
- Triggered by transients
- Sudden, jarring
- Rhythmic, musical

**Parameters:**
```
stutter_count: 2-5         # Number of stutter copies
stutter_duration: float    # How long stutter lasts
trigger_threshold: 0.0-1.0 # What triggers stutter
recovery_speed: 0.0-1.0    # How fast image recovers
```

**Best For:**
- Audio-reactive moments
- Transient emphasis
- Rhythmic effects
- Musical synchronization

---

### 2.5 Feedback Loop

**What It Is:**
The output feeds back into the input, creating accumulating, recursive corruption.

**Visual Character:**
- Image eats itself
- Recursive patterns
- Increasing chaos over time
- Self-generating complexity

**Parameters:**
```
feedback_amount: 0.0-1.0   # How much output feeds back
feedback_decay: 0.0-1.0    # How fast feedback fades
feedback_offset: float     # Position offset for feedback
stability_threshold: 0.0-1.0 # When to reset
```

**Best For:**
- Experimental effects
- Recursive aesthetics
- Self-generating art
- Maximum chaos

---

## 3. Fade Curves

### 3.1 Linear Fade

```
Opacity: 100% → 75% → 50% → 25% → 0%
```

**Character:** Even, predictable, mechanical
**Use For:** Technical precision, uniform decay

---

### 3.2 Exponential Fade

```
Opacity: 100% → 50% → 25% → 12% → 6% → 0%
```

**Character:** Present dominant, past fades fast
**Use For:** Natural feel, present moment emphasis
**Recommended:** Most glitchcore applications

---

### 3.3 Ease-Out Fade

```
Opacity: 100% → 90% → 70% → 40% → 10% → 0%
```

**Character:** Slow start, fast finish
**Use For:** Lingering ghosts, memory emphasis

---

### 3.4 Step Fade

```
Opacity: 100% → 50% → 50% → 25% → 25% → 0%
```

**Character:** Discrete levels, digital feel
**Use For:** Digital aesthetics, quantized time

---

## 4. Motion Direction Bias

### 4.1 Following Motion

Echoes trail behind moving objects.

```
[ECHO 3] [ECHO 2] [ECHO 1] [PRESENT] → → → motion direction
```

**Use For:** Natural movement, speed emphasis

---

### 4.2 Opposing Motion

Echoes lead moving objects (anticipation).

```
← ← ← [PRESENT] [ECHO 1] [ECHO 2] [ECHO 3]
```

**Use For:** Uncanny effects, time reversal

---

### 4.3 Radial Expansion

Echoes expand outward from center.

```
       [ECHO]
          ↓
    [ECHO] [ECHO]
       ↓  ↓  ↓
[ECHO] [PRESENT] [ECHO]
       ↑  ↑  ↑
    [ECHO] [ECHO]
          ↑
       [ECHO]
```

**Use For:** Explosive moments, radial energy

---

### 4.4 Random Scatter

Echoes scatter in random directions.

**Use For:** Chaos, instability, dream logic

---

## 5. Temporal + Other Drivers

### 5.1 Temporal + Channel Split

**Effect:**
Color separation echoes through time, creating chromatic trails.

**Use For:**
- RGB phantom + motion
- Colorful movement
- Spectral effects

---

### 5.2 Temporal + Bloom

**Effect:**
Glow accumulates and trails, creating luminous motion.

**Use For:**
- Ghost frame + glamour
- Luminous movement
- Radiant trails

---

### 5.3 Temporal + Compression

**Effect:**
Compression errors persist and propagate, creating damaged memory.

**Use For:**
- Corrupted memory
- Persistent damage
- Digital decay

---

### 5.4 Temporal + Overprint

**Effect:**
Multiple moments stack and overlap, creating time compression.

**Use For:**
- Ghost frame body
- Multiple poses
- Time collapse

---

## 6. Temporal Parameters by Subtype

| Subtype | Echo Type | Fade Curve | Motion Bias |
|---------|-----------|------------|-------------|
| Ghost Frame | Ghost Stack | Exponential | Motion |
| RGB Phantom | Color Echo | Exponential | Motion |
| Candy Broadcast | Light Echo | Ease-Out | Radial |
| Pastel Smear | Soft Echo | Exponential | Random |
| CRT Contour | Scan Echo | Linear | Vertical |
| Surveillance | Stutter | Step | Random |

---

## 7. Temporal Drift Detection

### 7.1 Generic Motion Blur

**Symptoms:**
- Looks like camera motion blur
- No frame separation
- No temporal hierarchy
- Just smeared

**Fix:**
- Add frame separation
- Use exponential fade
- Make present frame brightest
- Add motion direction

---

### 7.2 Equal Opacity Stack

**Symptoms:**
- All frames same brightness
- No present moment
- Looks like multiple exposure
- No temporal hierarchy

**Fix:**
- Add exponential fade
- Make present frame 100%
- Reduce echo opacity
- Create temporal hierarchy

---

### 7.3 Frozen Ghost

**Symptoms:**
- Echoes don't follow motion
- Looks static
- No kinetic energy
- Dead feeling

**Fix:**
- Add motion detection
- Follow motion vectors
- Add direction bias
- Create kinetic trails

---

## 8. Audio-Reactive Temporal

### 8.1 Beat-Reinforced Present

On each beat, present frame gets brighter, echoes fade faster.

**Use For:** Musical synchronization, rhythmic emphasis

---

### 8.2 Amplitude-Driven Echo Count

Louder sounds = more echoes visible.

**Use For:** Dynamic density, musical response

---

### 8.3 Transient Stutter

Sharp transients trigger stutter echoes.

**Use For:** Rhythmic glitch, transient emphasis

---

### 8.4 Sustained Tone Persistence

Long notes = longer echo persistence.

**Use For:** Pad sounds, sustained emotion

---

## 9. Short Anchor Rule

**Time should be visible, not just passing.**
