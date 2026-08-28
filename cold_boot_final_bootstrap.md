# Cold Boot - Final Bootstrap Markdown File

**Project:** Cold Boot  
**Status:** Composition complete; final export and post-export validation pending  
**Tracker:** MilkyTracker  
**Platform:** Linux / PikaOS  
**Target format:** 4-channel ProTracker MOD  
**Working format:** Current MilkyTracker project/module  
**Current order:** `00 01 02 01 03 04 02 05 03 06 04 07 08`

---

## Source-of-Truth Hierarchy

Use this hierarchy whenever records disagree:

1. **The current auditioned MilkyTracker project/module is authoritative** for:
   - exact sample loop points
   - exact sample volumes
   - exact per-row volume edits
   - exact finetune values
   - any last by-ear edits
2. **This bootstrap file is authoritative** for:
   - project architecture
   - pattern roles
   - order list
   - note/rhythm/effect structure
   - final sample identities
   - tested status
3. The ST-01 archive is only the source of the sample files.

The final by-ear Pulse volume edits and most exact finetune values were not transcribed into chat. Do not overwrite the working module with older generic values.

---

# 1. Current Goal & Next 3 Steps

## Current Goal

Finish and validate **Cold Boot** as an original, suspenseful, early-1990s-style Amiga loading-screen tune in authentic 4-channel ProTracker MOD format.

The composition itself is complete. The remaining work is production validation and export.

The final musical character is:

- mechanical and suspenseful
- sparse boot-up opening
- steady thumping groove
- chromatic dark variations
- diagnostic bell sequence
- breakdown and restart
- sustained dominant build
- broad minor-key release
- gradual phrase turnover back into the opening

Exact runtime is not a constraint. Musical structure, ProTracker compatibility, and convincing looping take priority.

## Next 3 Steps

### 1. Record the final sample metadata

Before changing anything else, write down the actual settings from the auditioned MilkyTracker file:

```text
Sample number
Sample filename
Default volume
Finetune
Loop start
Loop length/end
Loop type
```

Important fixed facts:

```text
Instrument 04 = ST-01/Pulse
Instrument 04 uses a tested forward loop
Instrument 05 = ST-01/KorgString
Instrument 05 uses a tested forward loop
Instrument 06 = ST-01/ExBells
Instrument 06 finetune = 0
```

### 2. Save the working master and export the MOD

Recommended filenames:

```text
cold_boot_working.xm
coldboot.mod
```

The XM is a safety master for MilkyTracker editing. The MOD is the authentic deliverable.

### 3. Reopen and validate the exported MOD

After export:

```text
Close or unload the working project
Open coldboot.mod
Play the full order list at least twice
Check all sample loops
Check all finetunes
Check the Pattern 07 -> 08 payoff
Check the Pattern 08 -> 00 phrase turnover
Check for clipping in Patterns 04 and 07
Confirm no XM-only behavior was required
```

A second ProTracker-compatible player may be used as an additional compatibility check.

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
Unique patterns: 00 through 08
Order length:    13
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
Exact final runtime is secondary
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
Pattern 07  Break to Dominant
Pattern 08  Release, Echo, Return
```

## Final Order List

```text
00 01 02 01 03 04 02 05 03 06 04 07 08
```

Structural arc:

```text
Wake
-> establish groove
-> variation
-> reprise
-> dark mutation
-> pressure build
-> return of variation
-> diagnostic sequence
-> dark reprise
-> breakdown
-> machinery restarts
-> dominant climax
-> release, echo, and phrase turnover
-> Wake Pulse begins again
```

## Final Sample Map

```text
01 BassDrum1    Kick
02 Snare4       Snare
03 CloseHiHat   Closed hi-hat
04 Pulse        Main looped bass/pulse voice
05 KorgString   Dark sustained pad
06 ExBells      Diagnostic chime
07 Stabs        Accent stab
08 Sweep        Transition / noise sweep
```

## Final Sample Behavior

Forward-looped:

```text
04 Pulse
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

Authoritative tuning rules:

```text
Pulse:
- all written octave-3 Pulse notes were moved to octave 4
- exact final volume edits are stored in the working module
- exact loop points are stored in the working module

KorgString:
- tested forward loop
- Pattern 07 final dominant pad root is G-4, not G-3

ExBells:
- finetune removed
- final finetune value is 0
```

Other samples have user-applied finetuning as stored in the working module. Exact values were not transcribed into chat.

## Locked Production Lessons

These are design constraints for any later revision:

```text
Establish sample loopability before detailed pattern writing.
Reject unsuitable sustained samples early.
Apply finetuning before committing note registers where possible.
Audition register choices with the actual sample and mix.
Written pitch legality does not guarantee audibility.
The saved module outranks theoretical pattern assumptions.
```

## Channel Architecture

Typical channel roles:

```text
Channel 1   Kick / snare
Channel 2   Pulse
Channel 3   KorgString
Channel 4   Hi-hat / ExBells / Stabs / Sweep
```

Channel 2 was intentionally given clearer attack space in the final climax patterns so the Pulse voice would not be swallowed by kick and snare.

## Effect Vocabulary

```text
F06   Set speed to 6

F91   Set BPM to hexadecimal 91
      = decimal 145

C00   Set channel volume to 0
C10   Set channel volume to decimal 16
C14   Set channel volume to decimal 20
C18   Set channel volume to decimal 24
C1C   Set channel volume to decimal 28
C20   Set channel volume to decimal 32
C24   Set channel volume to decimal 36
C28   Set channel volume to decimal 40
C2C   Set channel volume to decimal 44
C30   Set channel volume to decimal 48
C34   Set channel volume to decimal 52
C38   Set channel volume to decimal 56
C40   Set channel volume to decimal 64

037   Minor arpeggio:
      base note, +3 semitones, +7 semitones

047   Major arpeggio:
      base note, +4 semitones, +7 semitones
```

Example:

```text
C-4 05 037
```

cycles through:

```text
C-4
D#4
G-4
```

An effect-only event such as:

```text
... .. 037
```

continues the arpeggio on the note already active on that channel.

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
    │   ├── 04 Pulse
    │   ├── 05 KorgString
    │   ├── 06 ExBells
    │   ├── 07 Stabs
    │   └── 08 Sweep
    │
    ├── Cold Boot working master
    │   └── auditioned sample settings and final mix
    │
    └── Final deliverable
        └── coldboot.mod
```

## Release Caution

The ST-01/ST-XX archives are historically authentic but do not have clearly documented modern Creative Commons licensing in this project record.

Because a MOD embeds its samples:

```text
Do not assume coldboot.mod is automatically safe for unrestricted public redistribution.
Do not publish the ST-01 sample files as if they were newly licensed assets.
Resolve sample rights separately before a public release.
```

## Version Log

### v1.0 - Core Specification Locked

```text
Title: Cold Boot
Tracker: MilkyTracker
Target: 4-channel ProTracker MOD
Platform: Linux / PikaOS
Speed: 6
BPM: 145
Allowed note range: C-3 through B-5
```

### v1.1 - Final Sample Architecture Locked

```text
Eight ST-01 sample slots fixed
Instrument 04 locked as Pulse
Pulse and KorgString use tested forward loops
ExBells finetune locked at 0
Other exact tuning and volume settings stored in the module
```

### v1.2 - Patterns 00-06 Validated

```text
00 Wake Pulse          PASS
01 Main Thump A        PASS
02 Main Thump B        PASS
03 Dark Variation      PASS
04 Pressure Build      PASS
05 Diagnostic Chime    PASS
06 Breakdown           PASS
```

### v1.3 - Final Climax and Loop Pair Validated

```text
07 Break to Dominant           PASS
08 Release, Echo, Return       PASS
```

Final pair behavior:

```text
Pattern 04 -> 07 continues the established break
Pattern 07 ends in controlled dominant tension
Pattern 08 provides a broad C-minor release
Rows 16-31 echo the release at lower intensity
Rows 32-63 inherit Pattern 00 timing
Pattern 08 -> 00 works as phrase turnover
```

### v1.4 - Final Audition Edits Applied

```text
Pulse notes moved from octave 3 to octave 4
Pulse volume balance adjusted throughout
Pattern 07 dominant KorgString root raised from G-3 to G-4
Sample finetuning applied by ear
ExBells finetune removed
All nine patterns accepted
Composition phase complete
```

---

# 4. Golden Code Blocks

## Important Accuracy Note

The following pattern tables preserve the final **note, rhythm, instrument, and effect architecture** available in chat.

They already include:

```text
Instrument 04 changed to Pulse
All Instrument 04 octave-3 notes moved to octave 4
Pattern 07 KorgString dominant root raised to G-4
Final Patterns 07 and 08
```

However:

```text
Exact final Pulse volumes
Exact final sample volumes
Exact final loop points
Exact non-ExBells finetunes
Any last per-row mix edits
```

exist only in the auditioned MilkyTracker module and override these tables.

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
04 Pulse
05 KorgString
06 ExBells
07 Stabs
08 Sweep
```

## Pattern 00 - Wake Pulse

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | C-4 05 ...      | ...
08 (08)      | C-4 01 ...      | C-4 04 ...      | ...             | ...
12 (0C)      | C-5 03 ...      | ...             | ...             | ...
16 (10)      | C-4 01 ...      | G-4 04 ...      | G-3 05 ...      | ...
24 (18)      | C-4 01 ...      | A#4 04 ...      | ...             | G-4 06 ...
28 (1C)      | C-5 03 ...      | ...             | ...             | ...
32 (20)      | C-4 01 ...      | C-4 04 ...      | D#4 05 ...      | ...
40 (28)      | C-4 01 ...      | G#4 04 ...      | ...             | ...
44 (2C)      | C-5 03 ...      | ...             | ...             | D#5 06 ...
48 (30)      | C-4 01 ...      | F-4 04 ...      | G-3 05 ...      | ...
56 (38)      | C-4 01 ...      | G-4 04 ...      | ...             | C-4 08 ...
60 (3C)      | C-5 03 ...      | ...             | ...             | ...
```

## Pattern 01 - Main Thump A

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | C-4 05 ...      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | C-4 04 ...      | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
08 (08)      | C-4 02 ...      | G-4 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | A#4 04 ...      | ...             | ...
14 (0E)      | ...             | ...             | ...             | C-5 03 ...

16 (10)      | C-4 01 ...      | C-4 04 ...      | A#3 05 ...      | ...
18 (12)      | ...             | ...             | ...             | C-5 03 ...
20 (14)      | ...             | D#4 04 ...      | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | G-4 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 01 ...      | F-4 04 ...      | ...             | ...
30 (1E)      | ...             | ...             | ...             | C-5 07 ...

32 (20)      | C-4 01 ...      | G#4 04 ...      | G#3 05 ...      | ...
34 (22)      | ...             | ...             | ...             | C-5 03 ...
36 (24)      | ...             | G#4 04 ...      | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
40 (28)      | C-4 02 ...      | D#4 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 01 ...      | G-4 04 ...      | ...             | ...
46 (2E)      | ...             | ...             | ...             | C-5 03 ...

48 (30)      | C-4 01 ...      | F-4 04 ...      | F-3 05 ...      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | ...             | G-4 04 ...      | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | G#4 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | G-4 04 ...      | ...             | ...
62 (3E)      | ...             | ...             | ...             | G-4 07 ...
```

## Pattern 02 - Main Thump B

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | C-4 05 ...      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | G-4 04 ...      | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | C-4 04 ...      | ...             | C-5 03 ...
08 (08)      | C-4 02 ...      | ...             | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | D#4 04 ...      | ...             | C-5 03 ...
14 (0E)      | ...             | A#4 04 ...      | ...             | D#5 06 C20

16 (10)      | C-4 01 ...      | G#4 04 ...      | C#4 05 ...      | ...
18 (12)      | ...             | ...             | ...             | C-5 03 ...
20 (14)      | C-4 01 ...      | D#4 04 ...      | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | G-4 04 ...      | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | ...             | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 01 ...      | F-4 04 ...      | ...             | C-5 03 ...
30 (1E)      | ...             | D#4 04 ...      | ...             | D-5 06 C20

32 (20)      | C-4 01 ...      | D#4 04 ...      | A#3 05 ...      | ...
34 (22)      | ...             | ...             | ...             | C-5 03 ...
36 (24)      | ...             | A#4 04 ...      | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | G#4 04 ...      | ...             | C-5 03 ...
40 (28)      | C-4 02 ...      | ...             | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 01 ...      | D#4 04 ...      | ...             | C-5 03 ...
46 (2E)      | ...             | G-4 04 ...      | ...             | C#5 06 C20

48 (30)      | C-4 01 ...      | F-4 04 ...      | G-3 05 ...      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | C-4 01 ...      | C-4 04 ...      | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | D#4 04 ...      | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | ...             | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | G-4 04 ...      | ...             | C-5 03 ...
62 (3E)      | ...             | C-4 04 ...      | ...             | C-5 06 C20
```

## Pattern 03 - Dark Variation

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | D#4 05 ...      | ...
04 (04)      | ...             | ...             | ...             | C-5 03 ...
06 (06)      | C-4 01 ...      | ...             | ...             | ...
08 (08)      | ...             | G-4 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 02 ...      | ...             | ...             | ...
14 (0E)      | ...             | F#4 04 ...      | ...             | G-4 06 C20

16 (10)      | C-4 01 ...      | G#4 04 ...      | D-4 05 ...      | ...
20 (14)      | ...             | ...             | ...             | C-5 03 ...
22 (16)      | C-4 01 ...      | ...             | ...             | ...
24 (18)      | ...             | D#4 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 02 ...      | ...             | ...             | ...
30 (1E)      | ...             | G-4 04 ...      | ...             | C#5 07 C18

32 (20)      | C-4 01 ...      | F-4 04 ...      | C#4 05 ...      | ...
36 (24)      | ...             | ...             | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | ...
40 (28)      | ...             | C-4 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 02 ...      | ...             | ...             | ...
46 (2E)      | ...             | C#4 04 ...      | ...             | F#4 06 C20

48 (30)      | C-4 01 ...      | D#4 04 ...      | C-4 05 ...      | ...
52 (34)      | ...             | ...             | ...             | C-5 03 ...
54 (36)      | C-4 01 ...      | ...             | ...             | ...
56 (38)      | ...             | A#4 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 02 ...      | ...             | ...             | ...
62 (3E)      | ...             | G-4 04 ...      | ...             | C-5 07 C18
```

## Pattern 04 - Pressure Build

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | C-4 05 037      | ...
01 (01)      | ...             | ...             | ... .. 037      | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | C-4 04 ...      | ...             | ...
06 (06)      | C-4 01 ...      | ...             | ...             | ...
08 (08)      | C-4 02 ...      | G-4 04 ...      | ... .. 037      | ...
09 (09)      | ...             | ...             | ... .. 037      | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | D#4 04 ...      | ...             | ...
14 (0E)      | ...             | G-4 04 ...      | ...             | F#4 07 C18

16 (10)      | C-4 01 ...      | C#4 04 ...      | C#4 05 037      | ...
17 (11)      | ...             | ...             | ... .. 037      | ...
18 (12)      | ...             | ...             | ... .. 037      | C-5 03 ...
20 (14)      | C-4 01 ...      | G#4 04 ...      | ...             | ...
22 (16)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | E-4 04 ...      | ... .. 037      | ...
25 (19)      | ...             | ...             | ... .. 037      | ...
26 (1A)      | ...             | ...             | ... .. 037      | C-5 03 ...
28 (1C)      | C-4 01 ...      | C#4 04 ...      | ...             | ...
30 (1E)      | C-4 01 ...      | G#4 04 ...      | ...             | G-4 07 C1C

32 (20)      | C-4 01 ...      | D-4 04 ...      | D-4 05 037      | ...
33 (21)      | ...             | ...             | ... .. 037      | ...
34 (22)      | ...             | ...             | ... .. 037      | C-5 03 ...
35 (23)      | ...             | ...             | ... .. 037      | ...
36 (24)      | C-4 01 ...      | A-4 04 ...      | ...             | C-5 03 ...
38 (26)      | C-4 01 ...      | ...             | ...             | ...
40 (28)      | C-4 02 ...      | F-4 04 ...      | ... .. 037      | ...
41 (29)      | ...             | ...             | ... .. 037      | ...
42 (2A)      | ...             | ...             | ... .. 037      | C-5 03 ...
43 (2B)      | ...             | ...             | ... .. 037      | ...
44 (2C)      | C-4 01 ...      | D-4 04 ...      | ...             | C-5 03 ...
46 (2E)      | C-4 01 ...      | A-4 04 ...      | ...             | G#4 07 C20

48 (30)      | C-4 01 ...      | D#4 04 ...      | D#4 05 037      | ...
49 (31)      | ...             | ...             | ... .. 037      | ...
50 (32)      | ...             | ...             | ... .. 037      | C-5 03 ...
51 (33)      | ...             | ...             | ... .. 037      | ...
52 (34)      | C-4 01 ...      | A#4 04 ...      | ... .. 037      | C-5 03 ...
53 (35)      | ...             | ...             | ... .. 037      | ...
54 (36)      | C-4 01 ...      | ...             | ... .. 037      | C-5 03 ...
55 (37)      | ...             | ...             | ... .. 037      | ...
56 (38)      | C-4 02 ...      | F#4 04 ...      | ... .. 037      | ...
57 (39)      | ...             | ...             | ... .. 037      | ...
58 (3A)      | C-4 01 ...      | D#4 04 ...      | ... .. 037      | C-5 03 ...
59 (3B)      | ...             | ...             | ... .. 037      | ...
60 (3C)      | C-4 01 ...      | A#4 04 ...      | ... .. 037      | C-5 03 ...
61 (3D)      | ...             | ...             | ... .. 037      | ...
62 (3E)      | C-4 01 ...      | G-4 04 ...      | ... .. 037      | A-4 07 C24
63 (3F)      | ...             | ...             | ... .. 037      | ...
```

## Pattern 05 - Diagnostic Chime

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | C-4 04 F91      | C-4 05 ...      | ...
02 (02)      | ...             | ...             | ...             | G-4 06 C1C
06 (06)      | C-4 01 ...      | ...             | ...             | C-5 06 C20
08 (08)      | C-4 02 ...      | G-4 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | D#5 06 C20
12 (0C)      | C-4 01 ...      | D#4 04 ...      | ...             | ...
14 (0E)      | ...             | ...             | ...             | D-5 06 C1C

16 (10)      | C-4 01 ...      | C#4 04 ...      | C#4 05 ...      | ...
18 (12)      | ...             | ...             | ...             | G#4 06 C1C
22 (16)      | C-4 01 ...      | ...             | ...             | C#5 06 C20
24 (18)      | C-4 02 ...      | G#4 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | E-5 06 C20
28 (1C)      | C-4 01 ...      | E-4 04 ...      | ...             | ...
30 (1E)      | ...             | ...             | ...             | D#5 06 C1C

32 (20)      | C-4 01 ...      | D-4 04 ...      | D-4 05 ...      | ...
34 (22)      | ...             | ...             | ...             | A-4 06 C1C
38 (26)      | C-4 01 ...      | ...             | ...             | D-5 06 C20
40 (28)      | C-4 02 ...      | A-4 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | F-5 06 C20
44 (2C)      | C-4 01 ...      | F-4 04 ...      | ...             | ...
46 (2E)      | ...             | ...             | ...             | E-5 06 C1C

48 (30)      | C-4 01 ...      | D#4 04 ...      | D#4 05 ...      | ...
50 (32)      | ...             | ...             | ...             | A#4 06 C1C
54 (36)      | C-4 01 ...      | ...             | ...             | D#5 06 C20
56 (38)      | C-4 02 ...      | A#4 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | F#5 06 C20
60 (3C)      | C-4 01 ...      | F#4 04 ...      | ...             | ...
62 (3E)      | ...             | G-4 04 ...      | ...             | F-5 06 C1C
```

## Pattern 06 - Breakdown

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | ... .. F06      | C-4 04 F91      | C-4 05 C20      | ...
06 (06)      | ...             | ...             | ...             | G-4 06 C18
08 (08)      | C-4 01 C30      | G-4 04 ...      | ...             | ...
14 (0E)      | C-4 02 C20      | D#4 04 ...      | ...             | ...

16 (10)      | ...             | G#4 04 ...      | A#3 05 C1C      | ...
22 (16)      | C-4 01 C28      | ...             | ...             | F#4 06 C14
24 (18)      | ...             | D#4 04 ...      | ...             | ...
28 (1C)      | C-4 02 C1C      | ...             | ...             | ...
30 (1E)      | ...             | F-4 04 ...      | ...             | ...

32 (20)      | ...             | F-4 04 ...      | G#3 05 C18      | ...
38 (26)      | ...             | ...             | ...             | F-4 06 C10
40 (28)      | ...             | C-4 04 ...      | ...             | ...
44 (2C)      | C-4 02 C18      | ...             | ...             | ...
46 (2E)      | ...             | G-4 04 ...      | ...             | ...

48 (30)      | C-4 01 C28      | D#4 04 ...      | G-3 05 C20      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 C14
52 (34)      | C-4 01 C30      | F-4 04 ...      | ...             | ...
54 (36)      | ...             | ...             | ...             | C-5 03 C18
56 (38)      | C-4 01 C34      | F#4 04 ...      | A#3 05 C24      | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 C1C
60 (3C)      | C-4 01 C38      | G-4 04 ...      | C-4 05 C28      | ...
62 (3E)      | ...             | ...             | ...             | C-4 08 C18
```

## Pattern 07 - Break to Dominant

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 C38      | ...             | D#4 05 037      | ...
01 (01)      | ...             | D#4 04 C40      | ... .. 037      | ...
02 (02)      | ...             | ...             | ... .. 037      | C-5 03 C18
03 (03)      | ...             | ...             | ... .. 037      | ...
04 (04)      | C-4 01 C34      | ...             | ... .. 037      | C-5 03 C18
05 (05)      | ...             | A#4 04 C40      | ... .. 037      | ...
06 (06)      | C-4 01 C34      | ...             | ... .. 037      | C-5 03 C18
07 (07)      | ...             | ...             | ... .. 037      | A#4 06 C1C
08 (08)      | C-4 02 C2C      | ...             | ... .. 037      | ...
09 (09)      | ...             | F#4 04 C40      | ... .. 037      | ...
10 (0A)      | C-4 01 C34      | ...             | ... .. 037      | C-5 03 C18
11 (0B)      | ...             | ...             | ... .. 037      | ...
12 (0C)      | C-4 01 C34      | ...             | ... .. 037      | C-5 03 C18
13 (0D)      | ...             | A#4 04 C40      | ... .. 037      | ...
14 (0E)      | C-4 01 C34      | ...             | ... .. 037      | A#4 07 C24
15 (0F)      | ...             | ...             | ... .. 037      | ...

16 (10)      | C-4 01 C34      | ...             | E-4 05 037      | ...
17 (11)      | ...             | E-4 04 C40      | ... .. 037      | ...
18 (12)      | ...             | ...             | ... .. 037      | C-5 03 C18
19 (13)      | ...             | ...             | ... .. 037      | ...
20 (14)      | C-4 01 C34      | ...             | ...             | C-5 03 C18
21 (15)      | ...             | B-4 04 C40      | ...             | ...
22 (16)      | C-4 01 C34      | ...             | ...             | C-5 03 C18
23 (17)      | ...             | ...             | ...             | B-4 06 C1C
24 (18)      | C-4 02 C2C      | ...             | ... .. 037      | ...
25 (19)      | ...             | G-4 04 C40      | ... .. 037      | ...
26 (1A)      | C-4 01 C34      | ...             | ... .. 037      | C-5 03 C18
27 (1B)      | ...             | ...             | ... .. 037      | ...
28 (1C)      | C-4 01 C34      | ...             | ...             | C-5 03 C18
29 (1D)      | ...             | B-4 04 C40      | ...             | ...
30 (1E)      | C-4 01 C34      | ...             | ...             | B-4 07 C28

32 (20)      | C-4 01 C30      | ...             | F-4 05 037      | ...
33 (21)      | ...             | F-4 04 C40      | ... .. 037      | ...
34 (22)      | C-4 01 C30      | ...             | ...             | C-5 03 C18
36 (24)      | C-4 01 C30      | ...             | ... .. 037      | C-5 03 C18
37 (25)      | ...             | C-4 04 C40      | ... .. 037      | ...
38 (26)      | C-4 01 C30      | ...             | ...             | C-5 03 C18
39 (27)      | ...             | ...             | ...             | C-5 06 C20
40 (28)      | C-4 02 C28      | ...             | ... .. 037      | ...
41 (29)      | ...             | G#4 04 C40      | ... .. 037      | ...
42 (2A)      | C-4 01 C30      | ...             | ...             | C-5 03 C18
44 (2C)      | C-4 01 C30      | ...             | ... .. 037      | C-5 03 C18
45 (2D)      | ...             | C-4 04 C40      | ... .. 037      | ...
46 (2E)      | C-4 01 C30      | ...             | ...             | C-5 07 C2C

48 (30)      | C-4 01 C30      | ...             | G-4 05 047      | ...
49 (31)      | ...             | G-4 04 C40      | ... .. 047      | ...
50 (32)      | ...             | ...             | ...             | C-5 03 C14
52 (34)      | C-4 01 C30      | ...             | ... .. 047      | ...
53 (35)      | ...             | D-4 04 C40      | ... .. 047      | ...
54 (36)      | ...             | ...             | ...             | C-5 03 C14
56 (38)      | C-4 02 C28      | ...             | ... .. 047      | ...
57 (39)      | ...             | F-4 04 C40      | ... .. 047      | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 C14
60 (3C)      | C-4 01 C30      | ...             | ... .. 047      | ...
61 (3D)      | ...             | G-4 04 C40      | ... .. 047      | ...
62 (3E)      | ...             | ...             | ...             | F-5 06 C24
```

## Pattern 08 - Release, Echo, Return

```text
Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 C30      | C-4 04 C40      | C-4 05 C28      | D#5 06 C28
01 (01)      | ...             | ...             | ... .. 037      | ...
02 (02)      | ...             | ...             | ... .. 037      | ...
03 (03)      | ...             | ...             | ... .. 037      | ...
04 (04)      | ...             | G-4 04 C40      | ...             | ...
08 (08)      | C-4 02 C28      | D#4 04 C40      | ...             | ...
12 (0C)      | C-4 01 C2C      | G-4 04 C40      | ...             | C-5 06 C18

16 (10)      | C-4 01 C28      | C-4 04 C38      | C-4 05 C20      | D#5 06 C1C
17 (11)      | ...             | ...             | ... .. 037      | ...
18 (12)      | ...             | ...             | ... .. 037      | ...
19 (13)      | ...             | ...             | ... .. 037      | ...
20 (14)      | ...             | G-4 04 C38      | ...             | ...
24 (18)      | C-4 02 C20      | D#4 04 C38      | ... .. C20      | ...
28 (1C)      | C-4 01 C24      | G-4 04 C38      | ...             | C-5 06 C14

32 (20)      | C-4 01 C2C      | F-4 04 C38      | F-3 05 C20      | ...
40 (28)      | C-4 01 C2C      | C-4 04 C38      | G-3 05 C1C      | ...
44 (2C)      | ...             | ...             | ...             | C-5 03 C14
46 (2E)      | ...             | G-4 04 C38      | ...             | ...

48 (30)      | C-4 01 C30      | F-4 04 C38      | G-3 05 C18      | ...
56 (38)      | C-4 01 C30      | G-4 04 C38      | ...             | ...
60 (3C)      | ...             | ...             | ...             | C-5 03 C18
```

---

# 5. Tested & Passing Status Confirmation

## Environment and Architecture

```text
MilkyTracker workflow:                 PASS
ST-01 sample import/map:               PASS
4-channel architecture:                PASS
ProTracker-safe note range:            PASS
Pulse forward loop:                    PASS
KorgString forward loop:               PASS
Final by-ear balance:                  PASS
ExBells with finetune 0:               PASS
```

## Pattern Status

```text
Pattern 00 - Wake Pulse                PASS
Pattern 01 - Main Thump A              PASS
Pattern 02 - Main Thump B              PASS
Pattern 03 - Dark Variation            PASS
Pattern 04 - Pressure Build            PASS
Pattern 05 - Diagnostic Chime          PASS
Pattern 06 - Breakdown                 PASS
Pattern 07 - Break to Dominant         PASS
Pattern 08 - Release, Echo, Return     PASS
```

## Confirmed Transitions

```text
Pattern 01 -> Pattern 02               PASS
Pattern 01 -> Pattern 03               PASS
Pattern 02 -> Pattern 05               PASS
Pattern 03 -> Pattern 04               PASS
Pattern 03 -> Pattern 06               PASS
Pattern 05 -> Pattern 03               PASS
Pattern 06 -> Pattern 04               PASS
Pattern 04 -> Pattern 07               PASS
Pattern 07 -> Pattern 08               PASS
Pattern 08 -> Pattern 00               PASS as phrase turnover
```

## Confirmed Musical Behaviors

```text
Wake atmosphere                         PASS
Main thump balance                      PASS
Chromatic pad tension                   PASS
037 minor arpeggios                     PASS
Progressive stab-volume rise            PASS
Diagnostic chime sequence               PASS
Breakdown and restart                   PASS
Dominant climax                         PASS
Broad C-minor release                   PASS
Reduced echo phrase                     PASS
Gradual return to Pattern 00 feel       PASS
```

## Completion State

```text
All patterns composed:                  YES
All patterns entered:                   YES
All patterns auditioned:                YES
All patterns accepted:                  YES
Final sample identity locked:           YES
Final composition phase complete:       YES
Exported MOD reopen test:               PENDING
Full two-cycle post-export test:        PENDING
Secondary-player compatibility test:    OPTIONAL / PENDING
```

## Resume Instruction

When resuming this project, do not rewrite the composition by default.

Resume at final production:

```text
1. Record exact final sample metadata from MilkyTracker.
2. Save the working master and export coldboot.mod.
3. Reopen coldboot.mod and perform the post-export loop/compatibility checks.
```

The current MilkyTracker module remains the definitive record of the final mix.
