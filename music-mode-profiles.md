# Music Mode Profiles

Audio-reactive behavior maps for glitchcore subtypes — how corruption should respond to sound.

## Purpose

This file defines how glitchcore subtypes should behave when audio-reactive modes are enabled. It maps sound characteristics (frequency, amplitude, transients, emotional content) to visual corruption behaviors.

This is the part that helps the app stop going:
"make it move to the beat"
and start going:
"the bass should widen the rgb offset, the vocals should make the face glow, the transients should cause rupture pops."

The profiles here are designed to make audio-reactive glitchcore feel musically intelligent, not just visually reactive.

---

## 1. Audio-Reactive Mode Types

### 1.1 Spectrum Reactive

Responds to frequency bands across the spectrum.

**Best for:** Candy Broadcast, RGB Phantom, Glitter Signal, Candy Crash

**Mapping:**
- Bass → Structural distortion, wide offsets
- Low Mids → Duplicate spacing, echo count
- High Mids → Edge activity, face glow
- Highs → Sparkle density, fringe chatter
- Transients → Rupture pops, snap jumps

### 1.2 Semantic Reactive

Responds to vocal/speech content and emotional delivery.

**Best for:** Text Screen, Soft Internet Heartbreak, Terminal Confession

**Mapping:**
- Speech Presence → Emit phrase fragments
- Emotional Peaks → Increase face-text overlap
- Silence → Linger ghost text
- Amplitude → Adjust phrase density
- High Mids → Increase text clarity

### 1.3 Trail Reactive

Responds to sustained sounds and movement in music.

**Best for:** Ghost Frame, Temporal Echo subtypes

**Mapping:**
- Beat → Reinforce current frame
- Low Mids → Increase echo count
- Pads → Increase trail persistence
- Transients → Add stutter copy
- Amplitude → Increase trail brightness

### 1.4 Compression Reactive

Responds to dynamic range and codec-like behavior.

**Best for:** Candy Crash, Compression-heavy subtypes

**Mapping:**
- Bass → Increase block size
- Transients → Packet loss puncture
- High Mids → Edge buzz, chroma damage
- Vocals → Face zone smear
- Amplitude → Global compression pressure

### 1.5 Pulse Reactive

Responds to rhythmic pulse and sustained tones.

**Best for:** CRT Contour, Scanline subtypes

**Mapping:**
- Bass → Contour thickness
- Highs → Scanline shimmer
- Sustained Tones → Halo build
- Transients → Row jitter
- Vocals → Face contour emphasis

### 1.6 Tear Reactive (Subtle)

Responds to signal weakness and degradation.

**Best for:** Surveillance Apparition, Weak Feed subtypes

**Mapping:**
- Low Bass → Feed roll
- Highs → Hiss static
- Transients → Glitch flash
- Speech → Monitor focus shift
- Silence → Weak feed stillness

---

## 2. Subtype-Specific Music Profiles

### 2.1 Candy Broadcast Hallucination — Hyperpop Rupture Mode

**Audio Mode:** Spectrum Reactive

**Behavior Bias:**
- Channel Split: High
- Bloom Contamination: High
- Color Field Collision: Medium-High
- Compression Chew: Medium
- Text Interface Debris: Low-Medium

**Frequency Mapping:**
```
Bass (20-250Hz)
└── Widen structural distortion
    └── RGB offset increases
    └── Duplicate spacing expands

Low Mids (250-500Hz)
└── Increase duplicate spacing
    └── More visible separation between copies

High Mids (500-2000Hz)
└── Edge activity and face glow
    └── Face becomes brighter, edges chatter

Highs (2000-8000Hz)
└── Sparkle static and fringe chatter
    └── Peripheral glitter increases

Transients (peaks)
└── Rupture pops
    └── Brief overdrive moments
```

**State Switch Rules:**
- Chorus → Increase density
- Drop → Brief overdrive then recover
- Verse → Preserve anchor clarity

---

### 2.2 RGB Phantom — Spectral Dance Mode

**Audio Mode:** Spectrum Reactive

**Behavior Bias:**
- Channel Split: Very High
- Phase Lag Duplication: High
- Edge Emphasis: Medium-High
- Soft Bloom: Medium

**Frequency Mapping:**
```
Bass
└── Widen RGB offset dramatically
    └── Colors separate widest at edges

Low Mids
└── Increase phase lag
    └── Temporal offset between channels

High Mids
└── Enhance edge chatter
    └── Edge becomes more active, electric

Highs
└── Fringe flicker
    └── Peripheral color flicker

Transients
└── Channel snap jump
    └── Sudden color position shifts
```

**State Switch Rules:**
- Build-up → Gradually increase offset
- Peak → Maximum separation
- Release → Colors drift back together

---

### 2.3 Ghost Frame Body — Kinetic Echo Mode

**Audio Mode:** Trail Reactive

**Behavior Bias:**
- Temporal Echo: Very High
- Multi-Exposure Stack: High
- Soft Channel Split: Medium
- Bloom Trail Haze: Medium-High

**Frequency Mapping:**
```
Beat
└── Reinforce current frame
    └── Present moment becomes brightest

Low Mids
└── Increase echo count
    └── More historical frames visible

Pads
└── Increase trail persistence
    └── Echoes linger longer

Transients
└── Add stutter copy
    └── Brief duplicate at transient moment

Amplitude
└── Increase trail brightness
    └── Louder = brighter echoes
```

**State Switch Rules:**
- Breakdown → Maximum echo density
- Build → Echoes compress toward present
- Drop → Present frame dominates

---

### 2.4 Candy Crash Compression — Bratty File Damage Mode

**Audio Mode:** Compression Reactive

**Behavior Bias:**
- Compression Chew: Very High
- Macroblock Breakup: High
- Chroma Smear: High
- Quantization Banding: Medium-High

**Frequency Mapping:**
```
Bass
└── Increase block size
    └── Larger compression artifacts

Transients
└── Packet loss puncture
    └── Brief data-loss moments

High Mids
└── Edge buzz and chroma damage
    └── Color bleeding at edges

Vocals
└── Face zone smear
    └── Corruption concentrates on face

Amplitude
└── Global compression pressure
    └── Overall quality degrades with volume
```

**State Switch Rules:**
- Loud sections → Maximum compression damage
- Quiet sections → Partial recovery
- Transitions → Packet loss spikes

---

### 2.5 Text Screen Heartbreak — Spoken Confession Mode

**Audio Mode:** Semantic Reactive

**Behavior Bias:**
- Text Interface Debris: Very High
- Subtitle Ghosting: Very High
- Overprint Stacking: Medium
- Compression Haze: Medium-Low

**Frequency Mapping:**
```
Speech Presence
└── Emit phrase fragments
    └── Text appears with speech

Emotional Peaks
└── Increase face-text overlap
    └── Text layers onto face more

Silence
└── Linger ghost text
    └── Previous text fades slowly

Amplitude
└── Adjust phrase density
    └── Louder = more text

High Mids
└── Increase text clarity
    └── Speech frequencies = readable text
```

**State Switch Rules:**
- Whispery sections → Lower density, raise intimacy
- Louder sections → Increase text pressure
- Pause → Linger phrase residue

---

### 2.6 CRT Contour — Signal Saint Mode

**Audio Mode:** Pulse Reactive

**Behavior Bias:**
- Scanline Contour Banding: Very High
- Phosphor Bloom: High
- Faint Static Veil: Medium
- Subtle Capture Degradation: Low-Medium

**Frequency Mapping:**
```
Bass
└── Contour thickness
    └── Scanline bands get thicker

Highs
└── Scanline shimmer
    └── Lines sparkle and shift

Sustained Tones
└── Halo build
    └── Glow accumulates around figure

Transients
└── Row jitter
    └── Brief line displacement

Vocals
└── Face contour emphasis
    └── Face scanlines become more prominent
```

**State Switch Rules:**
- Sustained notes → Halo grows
- Percussion → Row jitter spikes
- Silence → Static veil thickens

---

### 2.7 Surveillance Apparition — Monitored Ghost Mode

**Audio Mode:** Tear Reactive (Subtle)

**Behavior Bias:**
- Capture Degradation: Very High
- Noise Veil: High
- Pixel Matrix Visibility: Medium
- Weak Interface Trace: Low

**Frequency Mapping:**
```
Low Bass
└── Feed roll
    └── Image slowly rolls vertically

Highs
└── Hiss static
    └── Noise increases

Transients
└── Glitch flash
    └── Brief corruption spike

Speech
└── Monitor focus shift
    └── Image sharpens slightly on speech

Silence
└── Weak feed stillness
    └── Image degrades in quiet
```

**State Switch Rules:**
- Speech → Brief clarity
- Silence → Gradual degradation
- Loud sounds → Glitch flash

---

### 2.8 Glitter Signal Overprint — Gloss Disaster Mode

**Audio Mode:** Pulse Reactive

**Behavior Bias:**
- Overprint Stacking: Very High
- Bloom Contamination: High
- Soft Channel Split: Medium
- Sparkle Static: High

**Frequency Mapping:**
```
Highs
└── Sparkle density
    └── More glitter particles

Vocals
└── Gloss bloom
    └── Face becomes more luminous

Bass
└── Duplicate drift
    └── Copies separate wider

Chorus
└── Overprint expansion
    └── More layers visible

Sustained Harmonics
└── Halo growth
    └── Glow accumulates
```

**State Switch Rules:**
- Chorus → Maximum overprint
- Verse → Reduced layers, clearer face
- Bridge → Sparkle density peaks

---

## 3. Universal Audio Behaviors

### 3.1 Amplitude Response

| Amplitude Level | Visual Response |
|-----------------|-----------------|
| Very Low | Minimal corruption, anchors clearest |
| Low | Subtle corruption, preserved structure |
| Medium | Balanced corruption and preservation |
| High | Strong corruption, anchors under pressure |
| Very High | Maximum corruption, brief anchor loss OK |

### 3.2 Transient Response

| Transient Type | Visual Response |
|----------------|-----------------|
| Sharp Attack | Rupture pop, snap jump |
| Soft Attack | Gradual corruption increase |
| Sharp Decay | Quick corruption release |
| Soft Decay | Slow corruption fade |

### 3.3 Sustained Sound Response

| Sustained Type | Visual Response |
|----------------|-----------------|
| Drone/Pad | Accumulating glow/trail |
| Sustained Note | Halo build |
| Long Tone | Contour thickness increase |
| Ambient Texture | Noise veil thickening |

---

## 4. State Switch Logic

### 4.1 Musical Section Responses

| Section | Behavior |
|---------|----------|
| Intro | Minimal corruption, establish anchors |
| Verse | Balanced, preserve clarity |
| Pre-Chorus | Build corruption tension |
| Chorus | Maximum density, release tension |
| Bridge | Experimental corruption, different drivers |
| Breakdown | Sparse but intense moments |
| Build | Increasing corruption pressure |
| Drop | Corruption explosion then recovery |
| Outro | Fading corruption, lingering ghosts |

### 4.2 Emotional Content Response

| Emotional Quality | Visual Response |
|-------------------|-----------------|
| Joy/Euphoria | Bright palette, high sparkle, wide offsets |
| Sadness/Melancholy | Soft palette, long trails, gentle bloom |
| Anger/Intensity | Harsh corruption, compression damage, high density |
| Intimacy/Vulnerability | Low density, preserved anchors, subtle text |
| Chaos/Confusion | Maximum density, multiple drivers, pile-up |

---

## 5. Summary Table: Subtype → Audio Mode

| Subtype | Audio Mode | Key Mapping |
|---------|------------|-------------|
| Candy Broadcast | Spectrum Reactive | Bass = wide offset, highs = sparkle |
| RGB Phantom | Spectrum Reactive | Bass = RGB separation, transients = snap |
| Ghost Frame | Trail Reactive | Beat = reinforce present, pads = persistence |
| Candy Crash | Compression Reactive | Bass = block size, vocals = face smear |
| Text Screen | Semantic Reactive | Speech = text, silence = ghosts |
| CRT Contour | Pulse Reactive | Bass = thickness, sustained = halo |
| Surveillance | Tear Reactive (Subtle) | Speech = clarity, silence = degradation |
| Glitter Signal | Pulse Reactive | Highs = sparkle, vocals = gloss |

---

## 6. Short Anchor Rule

**The music should conduct the corruption, not just trigger it.**
