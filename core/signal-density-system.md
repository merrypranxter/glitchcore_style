# Signal Density System

How much visual information should be corrupted vs preserved.

## Purpose

This file defines the signal density levels in glitchcore — how much of the image should be corrupted, how much should be preserved, and how to balance visual chaos with readable structure.

This is the part that helps the app stop going:
"make it glitchy"
and start going:
"dense signal = 70% corruption, 30% rest, one hot anchor preserved."

The density system here is designed to make corruption levels precise, measurable, and emotionally appropriate.

---

## 1. Density Level Definitions

### 1.1 Sparse Signal

**Visual Rest:** 70-80% of image
**Corruption:** 20-30% of image
**Anchor Preservation:** Maximum

**Description:**
Minimal corruption, maximum clarity. The glitch is subtle, like a whisper. Most of the image remains untouched.

**Visual Character:**
- Corruption feels like a trace
- One or two small glitch zones
- Subject is clearly visible
- Corruption is decorative, not dominant

**Best For:**
- Introducing glitch subtly
- Preserving maximum subject clarity
- Elegant, restrained aesthetics
- CRT contour (subtle)

**Parameter Values:**
```
primary_driver_strength: 0.2-0.3
secondary_driver_count: 0-1
corruption_coverage: 0.2-0.3
visual_rest: 0.7-0.8
anchor_protection: 0.9
```

---

### 1.2 Moderate Signal

**Visual Rest:** 50-60% of image
**Corruption:** 40-50% of image
**Anchor Preservation:** Strong

**Description:**
Balanced corruption and clarity. The glitch is noticeable but doesn't overwhelm. Subject remains clear but surrounded by corruption.

**Visual Character:**
- Corruption is clearly present
- Subject is still the focus
- Corruption frames and emphasizes
- Tension between order and chaos

**Best For:**
- General glitchcore applications
- Most subtypes at standard intensity
- Balanced emotional impact
- RGB phantom, pastel identity smear

**Parameter Values:**
```
primary_driver_strength: 0.4-0.5
secondary_driver_count: 1-2
corruption_coverage: 0.4-0.5
visual_rest: 0.5-0.6
anchor_protection: 0.7
```

---

### 1.3 Dense Signal

**Visual Rest:** 25-35% of image
**Corruption:** 65-75% of image
**Anchor Preservation:** Moderate

**Description:**
Heavy corruption with strategic preservation. The glitch dominates but one or two anchors hold the image together.

**Visual Character:**
- Corruption is the main event
- Subject is visible but pressured
- One hot anchor preserved (usually eyes)
- Beautiful instability

**Best For:**
- Candy broadcast hallucination
- Glitter signal overprint
- High-intensity moments
- Maximum emotional impact

**Parameter Values:**
```
primary_driver_strength: 0.6-0.7
secondary_driver_count: 2-3
corruption_coverage: 0.65-0.75
visual_rest: 0.25-0.35
anchor_protection: 0.5
```

---

### 1.4 Overloaded Signal

**Visual Rest:** 10-20% of image
**Corruption:** 80-90% of image
**Anchor Preservation:** Minimal

**Description:**
Maximum corruption with desperate preservation. The image is almost lost but one critical anchor holds on.

**Visual Character:**
- Corruption is overwhelming
- Subject is barely visible
- One critical anchor preserved
- Beautiful malfunction

**Best For:**
- Candy crash compression
- Extreme moments
- Internet-broken aesthetic
- Maximum chaos

**Parameter Values:**
```
primary_driver_strength: 0.8-0.9
secondary_driver_count: 3-4
corruption_coverage: 0.8-0.9
visual_rest: 0.1-0.2
anchor_protection: 0.3
```

---

### 1.5 Pile-Up Delirium

**Visual Rest:** 0-10% of image
**Corruption:** 90-100% of image
**Anchor Preservation:** Critical only

**Description:**
Total corruption with one desperate anchor. The image is a beautiful disaster, held together by a thread.

**Visual Character:**
- Maximum visual chaos
- One anchor barely visible
- Controlled delirium
- Beautiful disaster

**Best For:**
- Composite fever dream
- Maximum density experiments
- Artistic extremes
- When you want to push limits

**Parameter Values:**
```
primary_driver_strength: 0.9-1.0
secondary_driver_count: 4+
corruption_coverage: 0.9-1.0
visual_rest: 0.0-0.1
anchor_protection: 0.2 (critical only)
```

---

## 2. Density Selection Guide

### 2.1 By Subtype

| Subtype | Recommended Density |
|---------|---------------------|
| CRT Contour | Sparse to Moderate |
| Surveillance Apparition | Sparse to Moderate |
| Pastel Identity Smear | Moderate |
| RGB Phantom | Moderate to Dense |
| Ghost Frame Body | Moderate to Dense |
| Candy Broadcast | Dense |
| Glitter Signal | Dense |
| Candy Crash | Dense to Overloaded |
| Text Screen | Moderate to Dense |
| Composite Fever | Overloaded to Pile-Up |

### 2.2 By Emotion

| Emotion | Recommended Density |
|---------|---------------------|
| Intimate, vulnerable | Sparse |
| Dreamy, soft | Moderate |
| Seductive, loud | Dense |
| Bratty, broken | Dense to Overloaded |
| Chaotic, feverish | Overloaded to Pile-Up |
| Eerie, remote | Sparse to Moderate |
| Decadent, excessive | Overloaded to Pile-Up |

### 2.3 By Subject

| Subject | Recommended Density |
|---------|---------------------|
| Face close-up | Moderate to Dense |
| Full body | Moderate to Dense |
| Scene/landscape | Sparse to Moderate |
| Abstract | Any density |
| Text-heavy | Moderate |

---

## 3. Density Modulation

### 3.1 Increasing Density

```
+ Increase primary_driver_strength
+ Add secondary drivers
+ Reduce anchor_protection
+ Increase corruption_coverage
+ Reduce visual_rest
```

### 3.2 Decreasing Density

```
- Decrease primary_driver_strength
- Remove secondary drivers
- Increase anchor_protection
- Decrease corruption_coverage
- Increase visual_rest
```

### 3.3 Dynamic Density (Audio-Reactive)

```
Quiet sections → Sparse density
Building sections → Moderate density
Peak moments → Dense to Overloaded
Drop/chorus → Maximum density
Breakdown → Sparse with intense moments
```

---

## 4. Visual Rest Distribution

### 4.1 Where Rest Should Be

```
REST ZONES (clear areas):
├── Hot anchors (eyes, mouth)
├── Subject center
├── One readable focal point
└── Intentional negative space

CORRUPTION ZONES:
├── Edges
├── Background
├── Peripheral features
├── Duplicate layers
└── Echo trails
```

### 4.2 Rest Distribution by Density

| Density | Rest Location | Rest Amount |
|---------|---------------|-------------|
| Sparse | Scattered, small | 70-80% |
| Moderate | Around subject | 50-60% |
| Dense | Hot anchors only | 25-35% |
| Overloaded | One critical point | 10-20% |
| Pile-Up | Desperate anchor | 0-10% |

---

## 5. Density and Anchor Relationship

### 5.1 The Anchor Rule

```
As density increases, anchor protection becomes more critical.

Sparse:     Multiple anchors can be preserved
Moderate:   Key anchors preserved
Dense:      One hot anchor must survive
Overloaded: One critical anchor barely survives
Pile-Up:    One desperate anchor holds on
```

### 5.2 Anchor Selection by Density

| Density | Preserve These |
|---------|----------------|
| Sparse | Eyes, mouth, face, body |
| Moderate | Eyes, mouth, face center |
| Dense | Eyes, mouth |
| Overloaded | Eyes OR mouth |
| Pile-Up | One eye OR one readable phrase |

---

## 6. Density Drift Detection

### 6.1 Too Sparse for Intent

**Symptoms:** Corruption is barely visible, looks like a subtle filter

**Fix:** Increase primary_driver_strength, add secondary driver

### 6.2 Too Dense for Subject

**Symptoms:** Subject is lost, no readable anchor

**Fix:** Reduce primary_driver_strength, increase anchor_protection

### 6.3 Uneven Distribution

**Symptoms:** Some areas empty, others overloaded

**Fix:** Apply corruption more evenly, use flow patterns

### 6.4 Rest in Wrong Places

**Symptoms:** Clear areas where corruption should be, corrupted where should be clear

**Fix:** Rezone rest areas, apply region priority map

---

## 7. Density and Driver Relationship

### 7.1 Drivers by Density Suitability

| Driver | Sparse | Moderate | Dense | Overloaded |
|--------|--------|----------|-------|------------|
| Channel Split | ✓ | ✓ | ✓ | ✓ |
| Overprint | ✓ | ✓ | ✓ | Limited |
| Bloom | ✓ | ✓ | ✓ | Limited |
| Temporal Echo | Limited | ✓ | ✓ | ✓ |
| Compression | Limited | ✓ | ✓ | ✓ |
| Text Debris | ✓ | ✓ | Limited | Limited |
| Scanline | ✓ | ✓ | Limited | No |
| Capture Deg | ✓ | ✓ | Limited | No |

### 7.2 Driver Count by Density

| Density | Primary | Secondary | Total |
|---------|---------|-----------|-------|
| Sparse | 1 | 0-1 | 1-2 |
| Moderate | 1 | 1-2 | 2-3 |
| Dense | 1 | 2-3 | 3-4 |
| Overloaded | 1 | 3-4 | 4-5 |
| Pile-Up | 1 | 4+ | 5+ |

---

## 8. Summary Table

| Level | Rest | Corruption | Anchors | Use Case |
|-------|------|------------|---------|----------|
| Sparse | 70-80% | 20-30% | Many | Subtle, elegant |
| Moderate | 50-60% | 40-50% | Key | Balanced |
| Dense | 25-35% | 65-75% | One hot | Intense |
| Overloaded | 10-20% | 80-90% | One critical | Extreme |
| Pile-Up | 0-10% | 90-100% | Desperate | Maximum |

---

## 9. Short Anchor Rule

**Density is controlled chaos — know how much you're controlling.**
