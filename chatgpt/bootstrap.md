# Cold Boot Bootstrap
**Project:** Cold Boot
**Status:** Active
**Target:** MilkyTracker (Linux/PikaOS) → authentic 4-channel ProTracker `.MOD`

---

# 1. CURRENT GOAL

Compose an **original** suspenseful Amiga-style loading-screen tune in the style of **Ray Norish** and **Alistair Brimble** while remaining entirely original.

Design goals:

- Authentic early-1990s ProTracker style
- Four channels only
- Approximately one-minute seamless loop (exact runtime no longer critical)
- Sparse beginning that develops into a rhythmic loading-screen pulse
- Economical pattern reuse
- Compatible with original ProTracker playback
- Built in MilkyTracker on Linux

---

# NEXT THREE STEPS

## Step 1

Complete entry and audition of **Pattern 00 – Wake Pulse**.

Confirm:

- sample mapping
- balance
- looping
- atmosphere

## Step 2

Compose **Pattern 01 – Main Thump A**

This introduces the main rhythmic groove that becomes the foundation of the entire module.

## Step 3

Compose **Pattern 02 – Main Thump B**

A variation of the groove that introduces harmonic movement without losing the loading-screen pulse.

---

# 2. STATE OF PLAY

## Platform

Linux

Distribution:

PikaOS (Debian-derived)

Tracker:

MilkyTracker

Target export:

ProTracker MOD

---

## Musical Direction

Working title:

**Cold Boot**

Mood:

A machine powers up.

Everything appears normal.

Something isn't.

Not horror.

Not action.

Slow mechanical tension.

---

## Authenticity Rules

Always obey:

- 4 channels
- ProTracker effects only
- No XM features
- No instruments beyond ProTracker capabilities
- Pattern reuse preferred
- Simple forward loops only
- No stereo
- No modern tracker tricks

---

## Note Range

Use only:

```
C-3 through B-5
```

Nothing outside that range.

---

## Module Settings

```
Channels      4
Speed         6
Tempo/BPM     145
Rows          64
```

---

## Pattern Structure

Nine unique patterns.

Order list deliberately reuses material.

```
00
01
02
01
03
04
02
05
03
06
04
07
08
```

Pattern roles:

```
00 Wake Pulse

01 Main Thump A

02 Main Thump B

03 Dark Variation

04 Pressure Build

05 Diagnostic Chime

06 Breakdown

07 Climax Pulse

08 Loop Return
```

---

# Sample Set

Decision:

Use ST-01 archive.

No procedural synthesis.

Sample mapping:

```
01 BassDrum1
02 Snare4
03 CloseHiHat
04 PopBass
05 KorgString
06 ExBells
07 Stabs
08 Sweep
```

---

## Looping

Forward loops only.

Loop:

```
04 PopBass

05 KorgString
```

Do NOT loop:

```
BassDrum1

Snare4

CloseHiHat

ExBells

Stabs

Sweep
```

---

## Volume Starting Points

```
01 64

02 48

03 32

04 54

05 40

06 42

07 44

08 34
```

Finetune:

```
All zero
```

---

# 3. DEPENDENCY MAP

```
Linux

└── MilkyTracker

        │

        ├── ST-01 Samples

        │

        └── Cold Boot.mod
```

External dependency:

```
ST-01 archive
```

Everything else:

Manual composition.

---

# VERSION LOG

## v0.1

Decision:

Use MilkyTracker.

Abandon OpenMPT.

---

## v0.2

Decision:

Abandon procedural sample generator.

Use ST-01 archive.

---

## v0.3

Decision:

Restrict note range:

```
C-3 through B-5
```

---

## v0.4

Decision:

Use mixed order list rather than sequential.

---

## v0.5 (Current)

Pattern 00 composed.

Awaiting verification in MilkyTracker.

---

# 4. GOLDEN BLOCKS

## Module Settings

```text
Title      Cold Boot

Channels   4

Speed      6

Tempo      145

Rows       64
```

---

## Sample Mapping

```text
01 BassDrum1

02 Snare4

03 CloseHiHat

04 PopBass

05 KorgString

06 ExBells

07 Stabs

08 Sweep
```

---

## Order List

```text
00
01
02
01
03
04
02
05
03
06
04
07
08
```

---

## Pattern 00 — Wake Pulse

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-3 04 F91      | C-4 05 ...      | ...
08 (08)      | C-4 01 ...      | C-3 04 ...      | ...             | ...
12 (0C)      | C-5 03 ...      | ...             | ...             | ...
16 (10)      | C-4 01 ...      | G-3 04 ...      | G-3 05 ...      | ...
24 (18)      | C-4 01 ...      | A#3 04 ...      | ...             | G-4 06 ...
28 (1C)      | C-5 03 ...      | ...             | ...             | ...
32 (20)      | C-4 01 ...      | C-3 04 ...      | D#4 05 ...      | ...
40 (28)      | C-4 01 ...      | G#3 04 ...      | ...             | ...
44 (2C)      | C-5 03 ...      | ...             | ...             | D#5 06 ...
48 (30)      | C-4 01 ...      | F-3 04 ...      | G-3 05 ...      | ...
56 (38)      | C-4 01 ...      | G-3 04 ...      | ...             | C-4 08 ...
60 (3C)      | C-5 03 ...      | ...             | ...             | ...
```

---

# 5. TESTED & PASSING STATUS

## Environment

✅ MilkyTracker selected

✅ Linux workflow established

✅ ST-01 sample strategy chosen

---

## Architecture

✅ 4-channel design fixed

✅ Sample map fixed

✅ Order list fixed

✅ Tempo fixed

✅ Pattern layout fixed

---

## Pattern Status

Pattern 00:

**Entered by user**

Pending auditory verification.

No issues reported yet.

---

## Ready State

The project is fully configured.

The next conversation should begin by either:

1. Addressing any issues discovered while auditioning Pattern 00, **or**
2. Proceeding directly to composing **Pattern 01 – Main Thump A**.
