# Cold Boot — Bootstrap Markdown File

**Project:** Cold Boot  
**Status:** Composition in progress  
**Tracker:** MilkyTracker  
**Platform:** Linux / PikaOS  
**Target format:** 4-channel ProTracker MOD  
**Current checkpoint:** Patterns 00–04 composed; Patterns 00–02 auditioned and passing

---

# 1. Current Goal & Next 3 Steps

## Current Goal

Complete an original suspenseful Amiga-style loading-screen tune titled **Cold Boot** using authentic ProTracker constraints, ST-01 samples, four channels, compact pattern reuse, and a seamless loop.

The intended character is:

- mechanical and tense
- steady low thump
- dark sustained pad
- compact bass movement
- sparse diagnostic chimes
- increasing pressure rather than a conventional melodic build
- unmistakably early-1990s tracker in construction

Exact final runtime is no longer important. Musical flow, authenticity, and looping matter more.

## Next 3 Steps

1. **Enter and audition Pattern 03 — Dark Variation**
   - Check reduced rhythmic certainty
   - Confirm descending chromatic pad movement works
   - Verify `ExBells` at `C20`
   - Verify `Stabs` at `C18`
   - Check transition from Pattern 01 into Pattern 03

2. **Enter and audition Pattern 04 — Pressure Build**
   - Confirm `037` arpeggio works well with `KorgString`
   - Check progressive stab-volume rise
   - Check denser hats/kicks do not overcrowd the mix
   - Verify Pattern 03 -> 04 transition

3. **Compose Pattern 05 — Diagnostic Chime**
   - Make it compatible with Pattern 02 -> 05
   - Make it compatible with Pattern 05 -> 03
   - Use the already-tested `ExBells` behavior as a defining feature

---

# 2. State of Play

## Core Module Settings

```text
Title:           Cold Boot
Format:          ProTracker MOD
Tracker:         MilkyTracker
Channels:        4
Rows/pattern:    64
Speed:           6
Tempo/BPM:       145
Allowed notes:   C-3 through B-5 only
```

## Compatibility Rules

```text
4 channels only
ProTracker-compatible effects only
No XM-only composition features
No notes below C-3
No notes above B-5
Forward sample loops only
No ping-pong loops
Pattern reuse preferred
```

## Pattern Architecture

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

## Current Order List

```text
00 01 02 01 03 04 02 05 03 06 04 07 08
```

## Sample Map

```text
01 BassDrum1    Kick
02 Snare4       Snare
03 CloseHiHat   Closed hi-hat
04 PopBass      Main bass
05 KorgString   Dark sustained pad
06 ExBells      Diagnostic chime
07 Stabs        Accent stab
08 Sweep        Transition / noise sweep
```

## Sample Looping

Forward loops only.

Loop:

```text
04 PopBass
05 KorgString
```

One-shot:

```text
01 BassDrum1
02 Snare4
03 CloseHiHat
06 ExBells
07 Stabs
08 Sweep
```

### Authoritative Local Settings

The user has already reconfigured the actual loop points in MilkyTracker and boosted the volume of `PopBass`.

Those locally tested MilkyTracker settings are authoritative. Do not overwrite them unless a later audition proves a change is needed.

## Channel Roles

```text
Channel 1   Kick / snare
Channel 2   PopBass
Channel 3   KorgString
Channel 4   Hi-hat / ExBells / Stabs / Sweep
```

## Current Effect Vocabulary

```text
F06   Set speed to 6

F91   Set BPM to hexadecimal 91
      = decimal 145

C20   Set current channel volume to hexadecimal 20
      = decimal 32

C18   Set current channel volume to hexadecimal 18
      = decimal 24

C1C   Set current channel volume to hexadecimal 1C
      = decimal 28

C24   Set current channel volume to hexadecimal 24
      = decimal 36

037   Arpeggio:
      base note
      +3 semitones
      +7 semitones
```

Example:

```text
C-4 05 037
```

produces:

```text
C-4
D#4
G-4
```

An effect-only entry such as:

```text
... .. 037
```

continues the arpeggio on the note already playing on that channel.

---

# 3. Dependency Map & Version Log

## Dependency Map

```text
PikaOS / Debian-derived Linux
└── MilkyTracker
    ├── ST-01 sample archive
    │   ├── 01 BassDrum1
    │   ├── 02 Snare4
    │   ├── 03 CloseHiHat
    │   ├── 04 PopBass
    │   ├── 05 KorgString
    │   ├── 06 ExBells
    │   ├── 07 Stabs
    │   └── 08 Sweep
    │
    └── Cold Boot working module
        ├── Pattern 00 — PASS
        ├── Pattern 01 — PASS
        ├── Pattern 02 — PASS
        ├── Pattern 03 — composed, awaiting audition
        ├── Pattern 04 — composed, awaiting audition
        ├── Pattern 05 — pending
        ├── Pattern 06 — pending
        ├── Pattern 07 — pending
        └── Pattern 08 — pending
```

## Version Log

### v1.0 — Core Project Locked

```text
Title: Cold Boot
Tracker: MilkyTracker
Target: 4-channel ProTracker MOD
Platform: Linux / PikaOS
```

### v1.1 — Sample Architecture Locked

```text
Eight ST-01 sample slots fixed
PopBass and KorgString use forward loops
User-tuned loop settings are authoritative
PopBass volume increased after audition
```

### v1.2 — Structural Rules Locked

```text
Allowed note range: C-3 through B-5
Speed: 6
BPM: 145
Order list:
00 01 02 01 03 04 02 05 03 06 04 07 08
```

### v1.3 — Pattern 00 Validated

```text
Pattern 00 — Wake Pulse
Entered and auditioned successfully
Sample mapping, balance, and atmosphere confirmed good
```

### v1.4 — Pattern 01 Validated

```text
Pattern 01 — Main Thump A
Entered and auditioned successfully
Kick/snare balance confirmed good
Pad, Stabs, and PopBass confirmed good
```

### v1.5 — Pattern 02 Validated

```text
Pattern 02 — Main Thump B
Entered and auditioned successfully
Transition from Pattern 01 confirmed smooth
Tension confirmed good
ExBells at C20 confirmed good
Pattern 02 -> Pattern 05 check deferred until Pattern 05 exists
```

### v1.6 — Pattern 03 Composed

```text
Pattern 03 — Dark Variation
Composed
Awaiting entry and audition
```

### v1.7 — Pattern 04 Composed

```text
Pattern 04 — Pressure Build
Composed
Awaiting entry and audition
```

---

# 4. Golden Code Blocks

## Module Header

```text
Title:        Cold Boot
Channels:     4
Speed:        6
BPM:          145
Rows:         64
Note range:   C-3 through B-5
```

## Order List

```text
00 01 02 01 03 04 02 05 03 06 04 07 08
```

## Sample Map

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

## Pattern 01 — Main Thump A

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

## Pattern 02 — Main Thump B

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
46 (2E)      | ...             | G-3 04 ...       | ...             | C#5 06 C20

48 (30)      | C-4 01 ...      | F-3 04 ...      | G-3 05 ...      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | C-4 01 ...      | C-3 04 ...      | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | D#3 04 ...      | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | ...             | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | G-3 04 ...      | ...             | C-5 03 ...
62 (3E)      | ...             | C-3 04 ...      | ...             | C-5 06 C20
```

## Pattern 03 — Dark Variation

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-3 04 F91      | D#4 05 ...      | ...
04 (04)      | ...             | ...             | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | ...             | ...             | ...
08 (08)      | ...             | G-3 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 02 ...      | ...             | ...             | ...
14 (0E)      | ...             | F#3 04 ...      | ...             | G-4 06 C20

16 (10)      | C-4 01 ...      | G#3 04 ...      | D-4 05 ...      | ...
20 (14)      | ...             | ...             | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | ...             | ...             | ...
24 (18)      | ...             | D#3 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 02 ...      | ...             | ...             | ...
30 (1E)      | ...             | G-3 04 ...      | ...             | C#5 07 C18

32 (20)      | C-4 01 ...      | F-3 04 ...      | C#4 05 ...      | ...
36 (24)      | ...             | ...             | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | ...
40 (28)      | ...             | C-3 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 02 ...      | ...             | ...             | ...
46 (2E)      | ...             | C#3 04 ...      | ...             | F#4 06 C20

48 (30)      | C-4 01 ...      | D#3 04 ...      | C-4 05 ...      | ...
52 (34)      | ...             | ...             | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | ...             | ...             | ...
56 (38)      | ...             | A#3 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 02 ...      | ...             | ...             | ...
62 (3E)      | ...             | G-3 04 ...      | ...             | C-5 07 C18
```

## Pattern 04 — Pressure Build

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-3 04 F91      | C-4 05 037      | ...
01 (01)      | ...             | ...             | ... .. 037      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | C-3 04 ...      | ...             | ...
06 (06)      | C-4 01 ...      | ...             | ...             | ...
08 (08)      | C-4 02 ...      | G-3 04 ...      | ... .. 037      | ...
09 (09)      | ...             | ...             | ... .. 037      | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | D#3 04 ...      | ...             | ...
14 (0E)      | ...             | G-3 04 ...       | ...             | F#4 07 C18

16 (10)      | C-4 01 ...      | C#3 04 ...      | C#4 05 037      | ...
17 (11)      | ...             | ...             | ... .. 037      | ...
18 (12)      | ...             | ...             | ... .. 037      | C-5 03 ...
20 (14)      | C-4 01 ...      | G#3 04 ...      | ...             | ...
22 (16)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | E-3 04 ...       | ... .. 037      | ...
25 (19)      | ...             | ...             | ... .. 037      | ...
26 (1A)      | ...             | ...             | ... .. 037      | C-5 03 ...
28 (1C)      | C-4 01 ...      | C#3 04 ...      | ...             | ...
30 (1E)      | C-4 01 ...      | G#3 04 ...      | ...             | G-4 07 C1C

32 (20)      | C-4 01 ...      | D-3 04 ...       | D-4 05 037      | ...
33 (21)      | ...             | ...             | ... .. 037      | ...
34 (22)      | ...             | ...             | ... .. 037      | C-5 03 ...
35 (23)      | ...             | ...             | ... .. 037      | ...
36 (24)      | C-4 01 ...      | A-3 04 ...       | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | ...
40 (28)      | C-4 02 ...      | F-3 04 ...       | ... .. 037      | ...
41 (29)      | ...             | ...             | ... .. 037      | ...
42 (2A)      | ...             | ...             | ... .. 037      | C-5 03 ...
43 (2B)      | ...             | ...             | ... .. 037      | ...
44 (2C)      | C-4 01 ...      | D-3 04 ...       | ...             | C-5 03 ...
46 (2E)      | C-4 01 ...      | A-3 04 ...       | ...             | G#4 07 C20

48 (30)      | C-4 01 ...      | D#3 04 ...      | D#4 05 037      | ...
49 (31)      | ...             | ...             | ... .. 037      | ...
50 (32)      | ...             | ...             | ... .. 037      | C-5 03 ...
51 (33)      | ...             | ...             | ... .. 037      | ...
52 (34)      | C-4 01 ...      | A#3 04 ...      | ... .. 037      | C-5 03 ...
53 (35)      | ...             | ...             | ... .. 037      | ...
54 (36)      | C-4 01 ...      | ...             | ... .. 037      | C-5 03 ...
55 (37)      | ...             | ...             | ... .. 037      | ...
56 (38)      | C-4 02 ...      | F#3 04 ...      | ... .. 037      | ...
57 (39)      | ...             | ...             | ... .. 037      | ...
58 (3A)      | C-4 01 ...      | D#3 04 ...      | ... .. 037      | C-5 03 ...
59 (3B)      | ...             | ...             | ... .. 037      | ...
60 (3C)      | C-4 01 ...      | A#3 04 ...      | ... .. 037      | C-5 03 ...
61 (3D)      | ...             | ...             | ... .. 037      | ...
62 (3E)      | C-4 01 ...      | G-3 04 ...       | ... .. 037      | A-4 07 C24
63 (3F)      | ...             | ...             | ... .. 037      | ...
```

### Pattern 04 Conservative Arpeggio Adjustment

Only if the final section sounds too buzzy with the actual `KorgString`, remove `037` from:

```text
49
51
53
55
57
59
61
63
```

Do not make this change pre-emptively. Audition the composed version first.

---

# 5. Tested & Passing Status Confirmation

## Confirmed Passing

### Environment / Architecture

```text
MilkyTracker workflow:              PASS
ST-01 sample mapping:               PASS
4-channel architecture:             PASS
ProTracker-safe note range:         PASS
Sample looping configuration:       PASS after user adjustment
PopBass balance:                    PASS after user volume boost
```

### Pattern 00 — Wake Pulse

```text
Entered:                              YES
Auditioned:                           YES
Sample mapping:                       PASS
Balance:                              PASS
Atmosphere:                           PASS
Overall status:                       PASS
```

### Pattern 01 — Main Thump A

```text
Entered:                              YES
Auditioned:                           YES
Kick/snare balance:                   PASS
Pad:                                  PASS
Stabs:                                PASS
PopBass:                              PASS
Overall status:                       PASS
```

### Pattern 02 — Main Thump B

```text
Entered:                              YES
Auditioned:                           YES
Pattern 01 -> Pattern 02 transition:  PASS
Tension:                              PASS
ExBells at C20:                       PASS
Overall status:                       PASS
```

Deferred:

```text
Pattern 02 -> Pattern 05 transition:
DEFERRED until Pattern 05 exists
```

## Awaiting Audition

```text
Pattern 03 — Dark Variation
Status: COMPOSED / NOT YET AUDITIONED

Pattern 04 — Pressure Build
Status: COMPOSED / NOT YET AUDITIONED
```

## Remaining Patterns

```text
Pattern 05 — Diagnostic Chime
Pattern 06 — Breakdown
Pattern 07 — Climax Pulse
Pattern 08 — Loop Return
```

## Resume Point

```text
1. Enter and audition Pattern 03.
2. Enter and audition Pattern 04.
3. Report any issues.
4. If both pass, compose Pattern 05 — Diagnostic Chime.
```
