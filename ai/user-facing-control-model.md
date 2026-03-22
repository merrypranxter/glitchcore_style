# User-Facing Control Model

How to present glitchcore controls to users without overwhelming them or dumbing it down to uselessness.

## Purpose

This file defines the user-facing control model for glitchcore applications.

Its job is to translate the full complexity of the glitchcore system into controls that:
- Are intuitive to use
- Don't require reading 20 docs
- Still produce authentic glitchcore outputs
- Give users meaningful creative agency
- Scale from simple to advanced

---

## 1. Control Philosophy

### 1.1 The Balance

User controls should be:
- **Simple enough** that someone can use them without a manual
- **Deep enough** that someone who cares can get specific
- **Smart enough** that defaults produce good results
- **Transparent enough** that users understand what's happening

### 1.2 Control Tiers

**Tier 1: Quick Select (One-Click)**
- Preset styles
- Mood-based selections
- "Make it like this" references

**Tier 2: Guided Controls (Sliders + Dropdowns)**
- Style branch selection
- Intensity controls
- Color mood
- Motion amount
- Text amount

**Tier 3: Advanced (Full Parameter Access)**
- Individual driver controls
- Palette customization
- Density tuning
- Anchor protection zones
- Hybrid mixing

---

## 2. Tier 1: Quick Select

### 2.1 Preset Gallery

Present users with visual presets they can click:

| Preset Name | Subtype | Mood |
|-------------|---------|------|
| Candy Angel | Candy Broadcast | Seductive, loud |
| Soft Dream | Pastel Smear | Dreamy, romantic |
| Electric Ghost | RGB Phantom | Electric, unstable |
| Motion Memory | Ghost-Frame | Kinetic, haunted |
| Terminal Confession | Text-Screen | Lonely, confessional |
| Signal Saint | CRT Contour | Iconic, ceremonial |
| Internet Broken | Candy-Crash | Bratty, cheap-beautiful |
| Diva Glitter | Glitter-Signal | Glamorous, radiant |
| Fever Dream | Composite | Decadent, overloaded |
| Watched | Surveillance | Cold, institutional |

Each preset shows:
- Thumbnail preview
- Mood tags
- Intensity indicator

---

### 2.2 Mood-Based Selection

Let users pick by emotion:

**I want something...**
- Seductive and loud → Candy Broadcast
- Dreamy and soft → Pastel Smear
- Electric and unstable → RGB Phantom
- Lonely and confessional → Text-Screen
- Glamorous and radiant → Glitter-Signal
- Cold and watched → Surveillance
- Bratty and broken → Candy-Crash
- Kinetic and haunted → Ghost-Frame
- Iconic and ceremonial → CRT Contour
- Everything at once → Composite

---

## 3. Tier 2: Guided Controls

### 3.1 Main Control Panel

```
┌─────────────────────────────────────────┐
│  STYLE BRANCH                           │
│  [Dropdown: Select glitch type]         │
│                                         │
│  INTENSITY                              │
│  [Slider: Subtle ←──────→ Extreme]      │
│                                         │
│  COLOR MOOD                             │
│  [Dropdown: Select palette]             │
│                                         │
│  HUMAN vs CORRUPTED                     │
│  [Slider: Preserve ←──→ Destroy]        │
│                                         │
│  DREAMY vs AGGRESSIVE                   │
│  [Slider: Soft ←──────→ Harsh]          │
│                                         │
│  [ADVANCED OPTIONS ▼]                   │
└─────────────────────────────────────────┘
```

---

### 3.2 Style Branch Dropdown

Options:
- Candy Broadcast (bright, hyperpop)
- Pastel Smear (soft, dreamy)
- RGB Phantom (electric, chromatic)
- Ghost-Frame (motion, time)
- Text-Screen (confessional, language)
- CRT Contour (striped, iconic)
- Candy-Crash (broken, internet)
- Glitter-Signal (glossy, diva)
- Surveillance (cold, watched)
- Composite (everything)

Each option shows:
- Brief description
- Example thumbnail
- Key emotion tags

---

### 3.3 Intensity Slider

Maps to density levels:

| Slider Position | Density | Description |
|-----------------|---------|-------------|
| 1 (Subtle) | Sparse | Gentle corruption, mostly clear |
| 2 (Light) | Moderate | Noticeable but balanced |
| 3 (Medium) | Dense | Strong corruption, one anchor |
| 4 (Heavy) | Overloaded | Maximum corruption, desperate anchor |
| 5 (Extreme) | Pile-Up | Beautiful chaos, barely holding |

---

### 3.4 Color Mood Dropdown

Options:
- Hyperpop (magenta + cyan, loud)
- Pastel (pink + lavender, soft)
- Gloss (hot pink + violet, expensive)
- Noir (teal + ice blue, cold)
- Codec (magenta + flat cyan, broken)
- Rainbow (full spectrum, electric)
- Custom (user-defined)

---

### 3.5 Human vs Corrupted Slider

Maps to anchor protection:

| Slider Position | Protection | Effect |
|-----------------|------------|--------|
| Preserve | High | Face stays mostly clear |
| Balanced | Medium | Some face corruption |
| Destroy | Low | Face heavily corrupted |

---

### 3.6 Dreamy vs Aggressive Slider

Maps to driver selection and palette:

| Slider Position | Drivers | Palette |
|-----------------|---------|---------|
| Dreamy | Bloom, overprint, soft split | Pastel, soft |
| Balanced | Mix of soft and hard | Moderate saturation |
| Aggressive | Channel split, compression, tear | High saturation, harsh |

---

## 4. Tier 3: Advanced Controls

### 4.1 Advanced Panel

```
┌─────────────────────────────────────────┐
│  ADVANCED OPTIONS                       │
├─────────────────────────────────────────┤
│                                         │
│  PRIMARY DRIVER                         │
│  [Dropdown: Channel Split]              │
│  Strength: [Slider]                     │
│                                         │
│  SECONDARY DRIVERS                      │
│  [☑] Bloom Contamination                │
│  [☑] Overprint Stacking                 │
│  [ ] Compression Chew                   │
│  [ ] Text Debris                        │
│                                         │
│  PALETTE CUSTOMIZATION                  │
│  Dominant: [Color picker]               │
│  Collision: [Color picker]              │
│  Accent: [Color picker]                 │
│                                         │
│  ANCHOR ZONES                           │
│  [☑] Eyes                               │
│  [☑] Lips                               │
│  [☑] Face Center                        │
│  [ ] Full Face                          │
│                                         │
│  TEMPORAL SETTINGS                      │
│  Echo Count: [Number]                   │
│  Fade Curve: [Dropdown]                 │
│                                         │
│  TEXT SETTINGS                          │
│  Amount: [Slider]                       │
│  Legibility: [Slider]                   │
│  Overlap: [Slider]                      │
│                                         │
└─────────────────────────────────────────┘
```

---

### 4.2 Driver Controls

Each driver has:
- Enable/disable toggle
- Strength slider (0-100%)
- Advanced parameters (expandable)

**Example: Channel Split**
```
[☑] Channel Split
    Strength: [████████░░] 80%
    Edge Bias: [████████░░] 80%
    [Advanced ▼]
        Red Offset: X[░░░░] Y[░░░░]
        Green Offset: X[░░░░] Y[░░░░]
        Blue Offset: X[░░░░] Y[░░░░]
```

---

### 4.3 Palette Customization

```
PALETTE ARCHITECTURE

Dominant Hue (60-70%)
[Color: #FF0080] Magenta
Saturation: [████████░░]

Collision Hue (20-30%)
[Color: #00FFFF] Cyan
Saturation: [██████░░░░]

Accent Puncture (5-10%)
[Color: #FFFFFF] White
Intensity: [██████████]

[Save Palette] [Load Palette] [Randomize]
```

---

### 4.4 Anchor Zone Map

Visual face/body map where users can click zones to protect:

```
        [HAIR]
          │
    [EYE]─┼─[EYE]
          │
       [NOSE]
          │
       [MOUTH]
          │
      [JAWLINE]
          │
        [NECK]

Click zones to toggle protection:
[☑] Eyes  [☑] Nose  [☑] Mouth
[☑] Face Center  [ ] Full Face
```

---

## 5. Output Preview & Iteration

### 5.1 Preview Modes

| Mode | Shows |
|------|-------|
| Full Preview | Complete output |
| Before/After | Side-by-side comparison |
| Layer View | Individual driver contributions |
| Heat Map | Corruption density visualization |

---

### 5.2 Quick Adjustments

After preview, offer one-click adjustments:

- "More intense" → Increase density
- "Softer" → Decrease density, increase bloom
- "More color" → Increase saturation
- "More glitch" → Add secondary driver
- "Protect face more" → Increase anchor protection
- "More broken" → Add compression, reduce quality

---

### 5.3 Save & Share

```
[Save Preset] [Export Settings] [Share]

Preset Name: [__________]
Tags: [__________]
[Save to Library]

Export Format:
( ) JSON Config
( ) Prompt Text
( ) URL Share Link
```

---

## 6. Smart Defaults

### 6.1 Default Configurations

**Default (Balanced):**
- Subtype: Candy Broadcast
- Intensity: Medium (3)
- Color: Hyperpop
- Human vs Corrupted: Balanced
- Dreamy vs Aggressive: Balanced

**Fast Start Presets:**
- Portrait: Candy Broadcast, Medium, Preserve face
- Landscape: Pastel Smear, Light, Balanced
- Action: Ghost-Frame, Dense, Motion emphasis
- Text-heavy: Text-Screen, Medium, High text
- Dark mood: Surveillance, Medium, Noir palette

---

### 6.2 Context-Aware Defaults

If user uploads:
- **Portrait photo** → Default to face-preserving settings
- **Landscape** → Default to atmospheric settings
- **Text in image** → Offer text-screen options
- **Motion blur** → Offer ghost-frame options
- **Low quality source** → Offer candy-crash options

---

## 7. Help & Guidance

### 7.1 Inline Help

Hover tooltips explain each control:

```
[?] Style Branch
    The main type of glitch corruption.
    Each branch has different artifact
    behaviors and emotional tones.

[?] Intensity
    How much of the image is corrupted.
    Higher = more damage, less clarity.
```

---

### 7.2 Suggestion Engine

Based on user's image and selections, suggest:

```
Based on your image, you might like:
• Candy Broadcast (bright, seductive)
• Try increasing intensity for more drama
• Your image has motion — consider Ghost-Frame
```

---

### 7.3 Learning Mode

For new users, show:

```
┌─────────────────────────────────────────┐
│  NEW TO GLITCHCORE?                     │
│                                         │
│  Start with presets, then explore:      │
│  1. Style Branch — type of glitch       │
│  2. Intensity — how much corruption     │
│  3. Color Mood — emotional palette      │
│                                         │
│  [Start Tutorial] [Skip]                │
└─────────────────────────────────────────┘
```

---

## 8. Mobile Adaptation

### 8.1 Mobile Control Layout

```
┌─────────────────┐
│   [Preview]     │
├─────────────────┤
│ [Style] [Color] │
│ [Intensity]     │
│ ○────●────○     │
├─────────────────┤
│ [Apply] [Save]  │
└─────────────────┘
```

- Swipe for presets
- Tap for quick options
- Long-press for advanced
- Pinch to compare before/after

---

## 9. Summary

The user-facing control model provides:
- Three tiers of control depth
- Smart defaults that produce good results
- Clear mappings to underlying system
- Visual, intuitive interface
- Advanced options for power users
- Context-aware suggestions
- Help and guidance throughout

---

## 10. Short Anchor Rule

Give users control without drowning them in parameters.
