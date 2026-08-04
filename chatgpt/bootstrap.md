# Cold Boot Bootstrap

**Project:** Cold Boot  
**Current status:** Composition in progress  
**Target environment:** MilkyTracker on Linux/PikaOS  
**Target format:** 4-channel ProTracker MOD

---

## 1. Current Goal

Compose an original suspenseful Amiga-style loading-screen tune called **Cold Boot**, using authentic ProTracker constraints and ST-01 samples.

The tune should feel like a machine booting into an uncertain state:

- steady mechanical thump
- dark sustained pad
- compact bass movement
- sparse diagnostic chimes
- gradual increase in tension
- seamless loop
- exact final runtime is no longer critical

### Next 3 Steps

1. **Enter and audition Pattern 01: Main Thump A**
   - Verify kick/snare balance
   - Confirm bass movement works with `PopBass`
   - Confirm pad sustains cleanly
   - Check that `Stabs` does not overpower the groove

2. **Enter and audition Pattern 02: Main Thump B**
   - Confirm the chromatic pad tension works
   - Check `ExBells` volume using `C20`
   - Verify the ending connects cleanly to both Pattern 01 and Pattern 05

3. **Compose Pattern 03: Dark Variation**
   - Reduce rhythmic certainty
   - Shift pad harmony
   - Introduce a more suspenseful bell or stab relationship
   - Preserve compatibility with the current order list

---

## 2. State of Play

### Core Design

```text
Title:           Cold Boot
Tracker:         MilkyTracker
Format:          ProTracker MOD
Channels:        4
Rows/pattern:    64
Speed:           6
Tempo/BPM:       145
Allowed notes:   C-3 through B-5 only
```

### Musical Architecture

Nine unique patterns are reused through a non-linear order list.

```text
Pattern 00  Wake Pulse
Pattern 01  Main Thump A
Pattern 02  Main Thump B
Pattern 03  Dark Variation
Pattern 04  Pressure Build
Pattern 05  Diagnostic Chime
Pattern 06  Breakdown
Pattern 07  Climax Pulse
Pattern 08  Loop Return
```

### Current Order List

```text
00 01 02 01 03 04 02 05 03 06 04 07 08
```

This order provides:

- introduction
- establishment of main groove
- variation
- reprise
- darker mutation
- build
- return of variation
- diagnostic section
- second dark reprise
- breakdown
- renewed build
- climax
- loop transition

### Compatibility Rules

Always preserve:

```text
4 channels only
ProTracker-compatible effects only
No XM-only features
No notes below C-3
No notes above B-5
Forward sample loops only
No ping-pong loops
Pattern reuse preferred
```

### Sample Map

```text
01 BassDrum1    Kick
02 Snare4       Snare
03 CloseHiHat   Closed hi-hat
04 PopBass      Main bass
05 KorgString   Dark sustained pad
06 ExBells      Diagnostic chime
07 Stabs        Accent stab
08 Sweep        Transition/noise sweep
```

### Suggested Starting Volumes

```text
01 BassDrum1    64
02 Snare4       48
03 CloseHiHat   32
04 PopBass      54
05 KorgString   40
06 ExBells      42
07 Stabs        44
08 Sweep        34
```

### Loop Configuration

Use forward loops only.

```text
04 PopBass      Forward loop
05 KorgString   Forward loop
```

Keep these as one-shots:

```text
01 BassDrum1
02 Snare4
03 CloseHiHat
06 ExBells
07 Stabs
08 Sweep
```

Where possible, preserve any clean loop metadata already present in the ST-01 samples. Otherwise choose a stable sustain region after the initial attack.

### Channel Roles

The exact assignment can vary by pattern, but the current groove architecture is:

```text
Channel 1   Kick and snare
Channel 2   PopBass
Channel 3   KorgString
Channel 4   Hi-hat, chime, stab, or sweep
```

---

## 3. Dependency Map & Version Log

### Dependency Map

```text
PikaOS / Debian-derived Linux
└── MilkyTracker
    ├── ST-01 sample archive
    │   ├── BassDrum1
    │   ├── Snare4
    │   ├── CloseHiHat
    │   ├── PopBass
    │   ├── KorgString
    │   ├── ExBells
    │   ├── Stabs
    │   └── Sweep
    └── Cold Boot working module
        ├── Pattern 00
        ├── Pattern 01
        ├── Pattern 02
        └── Patterns 03-08 pending
```

### Current Version Log

#### v1.0 — Project Specification Locked

```text
Title: Cold Boot
Format: 4-channel ProTracker MOD
Tracker: MilkyTracker
Platform: Linux/PikaOS
```

#### v1.1 — Sample Architecture Locked

```text
ST-01 sample set selected
Eight fixed sample slots established
PopBass and KorgString designated as looped samples
```

#### v1.2 — Structural Rules Locked

```text
Note range fixed at C-3 through B-5
Speed fixed at 6
BPM set to 145
Mixed 13-position order list established
```

#### v1.3 — Pattern 00 Composed

```text
Pattern 00: Wake Pulse
Sparse boot-up pulse with bass, pad, bells, and sweep
```

#### v1.4 — Pattern 01 Composed

```text
Pattern 01: Main Thump A
Core mechanical groove established
```

#### v1.5 — Pattern 02 Composed

```text
Pattern 02: Main Thump B
Syncopated variation with chromatic pad tension and diagnostic bells
```

---

## 4. Golden Code Blocks

These are the current authoritative pattern definitions.

### Module Header

```text
Title:        Cold Boot
Channels:     4
Speed:        6
BPM:          145
Rows:         64
Note range:   C-3 to B-5
```

### Order List

```text
00 01 02 01 03 04 02 05 03 06 04 07 08
```

### Pattern 00 — Wake Pulse

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

### Pattern 01 — Main Thump A

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-3 04 F91      | C-4 05 ...      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | C-3 04 ...      | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
08 (08)      | C-4 02 ...      | G-3 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | A#3 04 ...      | ...             | ...
14 (0E)      | ...             | ...             | ...             | C-5 03 ...

16 (10)      | C-4 01 ...      | C-3 04 ...      | A#3 05 ...      | ...
18 (12)      | ...             | ...             | ...             | C-5 03 ...
20 (14)      | ...             | D#3 04 ...      | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | G-3 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 01 ...      | F-3 04 ...      | ...             | ...
30 (1E)      | ...             | ...             | ...             | C-5 07 ...

32 (20)      | C-4 01 ...      | G#3 04 ...      | G#3 05 ...      | ...
34 (22)      | ...             | ...             | ...             | C-5 03 ...
36 (24)      | ...             | G#3 04 ...      | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
40 (28)      | C-4 02 ...      | D#3 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 01 ...      | G-3 04 ...      | ...             | ...
46 (2E)      | ...             | ...             | ...             | C-5 03 ...

48 (30)      | C-4 01 ...      | F-3 04 ...      | F-3 05 ...      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | ...             | G-3 04 ...      | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | G#3 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | G-3 04 ...      | ...             | ...
62 (3E)      | ...             | ...             | ...             | G-4 07 ...
```

### Pattern 02 — Main Thump B

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-3 04 F91      | C-4 05 ...      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | G-3 04 ...      | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | C-3 04 ...      | ...             | C-5 03 ...
08 (08)      | C-4 02 ...      | ...             | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | D#3 04 ...      | ...             | C-5 03 ...
14 (0E)      | ...             | A#3 04 ...      | ...             | D#5 06 C20

16 (10)      | C-4 01 ...      | G#3 04 ...      | C#4 05 ...      | ...
18 (12)      | ...             | ...             | ...             | C-5 03 ...
20 (14)      | C-4 01 ...      | D#3 04 ...      | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | G-3 04 ...      | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | ...             | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 01 ...      | F-3 04 ...      | ...             | C-5 03 ...
30 (1E)      | ...             | D#3 04 ...      | ...             | D-5 06 C20

32 (20)      | C-4 01 ...      | D#3 04 ...      | A#3 05 ...      | ...
34 (22)      | ...             | ...             | ...             | C-5 03 ...
36 (24)      | ...             | A#3 04 ...      | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | G#3 04 ...      | ...             | C-5 03 ...
40 (28)      | C-4 02 ...      | ...             | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 01 ...      | D#3 04 ...      | ...             | C-5 03 ...
46 (2E)      | ...             | G-3 04 ...      | ...             | C#5 06 C20

48 (30)      | C-4 01 ...      | F-3 04 ...      | G-3 05 ...      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | C-4 01 ...      | C-3 04 ...      | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | D#3 04 ...      | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | ...             | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | G-3 04 ...      | ...             | C-5 03 ...
62 (3E)      | ...             | C-3 04 ...      | ...             | C-5 06 C20
```

### Effect Reference

```text
F06   Set speed to 6
F91   Set BPM to hexadecimal 91 = decimal 145
C20   Set current channel volume to hexadecimal 20 = decimal 32
```

---

## 5. Tested & Passing Status Confirmation

### Confirmed Working

```text
MilkyTracker selected and available
ST-01 samples downloaded/prepared by user
Eight-sample mapping established
4-channel module architecture established
ProTracker-safe note range established
Sample wiring test completed successfully
User returned "Ready" after the sample/setup test
```

### Composed but Not Yet Confirmed by Audition

```text
Pattern 00 — Wake Pulse
Pattern 01 — Main Thump A
Pattern 02 — Main Thump B
```

Pattern 01 was reviewed visually by the user and described as looking good, but the user explicitly said it would be tested later.

Pattern 02 has been composed but has not yet been entered or auditioned.

### Current Validation State

```text
Environment/setup:      PASS
Sample slot mapping:    PASS
Basic sample test:      PASS
Pattern 00 audio test:  NOT CONFIRMED
Pattern 01 audio test:  NOT YET TESTED
Pattern 02 audio test:  NOT YET TESTED
Final MOD export:       NOT YET TESTED
Seamless loop:          NOT YET TESTED
```

### Resume Instruction

On resuming:

1. Enter and audition Pattern 01.
2. Enter and audition Pattern 02.
3. Report any balance, pitch, loop, timing, or transition issues.
4. If both pass, compose Pattern 03: Dark Variation.
