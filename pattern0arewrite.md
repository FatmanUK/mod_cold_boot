Pattern09 is good, audition passed, but pattern0a is rejected. Its rhythm is scattered to the four winds. What happened there? Pattern0a needs a rewrite.

---

Pattern 09 is now **auditioned and passing**. The old Pattern 0A is discarded.

What went wrong was fairly specific: it did not contain one phase shift. It contained several unrelated displacements. The Pulse attacks changed their relationship to the drums, the pad entered at inconsistent points, arpeggio flashes appeared sporadically, and the phrase markers moved around. In four-channel music, that is enough to make the rhythm sound as though it has been distributed by a malfunctioning leaf blower.

The replacement uses one simple rule:

```text
Every major four-row beat begins on an even row.
The Pulse answers exactly one row later.
```

That relationship repeats through the entire pattern:

```text
Drum/downbeat: 00 04 08 12
Pulse answer:  01 05 09 13
```

The same 16-row rhythmic cell is repeated four times. Only the harmony changes.

## Replacement Pattern 0A: Phase Lock

It sits in the unchanged sequence:

```text
Pattern 01 -> Pattern 0A -> Pattern 02
```

The harmonic path is:

```text
F minor -> C minor -> A-flat -> G dominant -> Pattern 02 in C minor
```

Pattern 01 leaves `F-3` playing on KorgString. Pattern 0A deliberately does **not** retrigger the pad at row 00, so that F pad carries naturally across the boundary.

Audition this pattern in song context rather than beginning directly at Pattern 0A. Otherwise the first sixteen rows will lack the inherited pad, because trackers are literal-minded little bureaucrats.

Everything not listed remains empty.

```text
Cold Boot
Pattern 0A - Phase Lock

Row dec(hex) | Ch1             | Ch2             | Ch3             | Ch4
-------------+-----------------+-----------------+-----------------+-----------------
00 (00)      | C-4 01 F06      | ... .. F91      | ...             | ...
01 (01)      | ...             | F-4 04 ...      | ...             | ...
02 (02)      | ...             | ...             | ...             | C-5 03 ...
04 (04)      | ...             | ...             | ...             | C-5 03 ...
05 (05)      | ...             | C-4 04 ...      | ...             | ...
06 (06)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
08 (08)      | C-4 02 ...      | ...             | ...             | ...
09 (09)      | ...             | G#4 04 ...      | ...             | ...
10 (0A)      | ...             | ...             | ...             | C-5 03 ...
12 (0C)      | C-4 01 ...      | ...             | ...             | ...
13 (0D)      | ...             | C-4 04 ...      | ...             | ...
14 (0E)      | ...             | ...             | ...             | C-5 03 ...
15 (0F)      | ...             | ...             | ...             | G#4 06 C14

16 (10)      | C-4 01 ...      | ...             | C-4 05 ...      | ...
17 (11)      | ...             | C-4 04 ...      | ...             | ...
18 (12)      | ...             | ...             | ...             | C-5 03 ...
20 (14)      | ...             | ...             | ...             | C-5 03 ...
21 (15)      | ...             | G-4 04 ...      | ...             | ...
22 (16)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
24 (18)      | C-4 02 ...      | ...             | ...             | ...
25 (19)      | ...             | D#4 04 ...      | ...             | ...
26 (1A)      | ...             | ...             | ...             | C-5 03 ...
28 (1C)      | C-4 01 ...      | ...             | ...             | ...
29 (1D)      | ...             | G-4 04 ...      | ...             | ...
30 (1E)      | ...             | ...             | ...             | C-5 03 ...
31 (1F)      | ...             | ...             | ...             | D#5 06 C14

32 (20)      | C-4 01 ...      | ...             | G#3 05 ...      | ...
33 (21)      | ...             | G#4 04 ...      | ...             | ...
34 (22)      | ...             | ...             | ...             | C-5 03 ...
36 (24)      | ...             | ...             | ...             | C-5 03 ...
37 (25)      | ...             | D#4 04 ...      | ...             | ...
38 (26)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
40 (28)      | C-4 02 ...      | ...             | ...             | ...
41 (29)      | ...             | C-4 04 ...      | ...             | ...
42 (2A)      | ...             | ...             | ...             | C-5 03 ...
44 (2C)      | C-4 01 ...      | ...             | ...             | ...
45 (2D)      | ...             | D#4 04 ...      | ...             | ...
46 (2E)      | ...             | ...             | ...             | C-5 03 ...
47 (2F)      | ...             | ...             | ...             | C-5 06 C14

48 (30)      | C-4 01 ...      | ...             | G-4 05 ...      | ...
49 (31)      | ...             | G-4 04 ...      | ...             | ...
50 (32)      | ...             | ...             | ...             | C-5 03 ...
52 (34)      | ...             | ...             | ...             | C-5 03 ...
53 (35)      | ...             | D-4 04 ...      | ...             | ...
54 (36)      | C-4 01 ...      | ...             | ...             | C-5 03 ...
56 (38)      | C-4 02 ...      | ...             | ...             | ...
57 (39)      | ...             | B-4 04 ...      | ...             | ...
58 (3A)      | ...             | ...             | ...             | C-5 03 ...
60 (3C)      | C-4 01 ...      | ...             | ...             | ...
61 (3D)      | ...             | D-4 04 ...      | ...             | ...
62 (3E)      | ...             | ...             | ...             | C-5 03 ...
63 (3F)      | ...             | ...             | ...             | G-4 06 C10
```

## The fixed rhythmic cell

Every sixteen-row section now uses exactly this layout:

```text
Row +00   Kick
Row +01   Pulse
Row +02   Hat
Row +04   Hat
Row +05   Pulse
Row +06   Kick + Hat
Row +08   Snare
Row +09   Pulse
Row +10   Hat
Row +12   Kick
Row +13   Pulse
Row +14   Hat
Row +15   Quiet bell
```

That is the entire rhythmic premise. No wandering attack positions, no surprise arpeggio fragments, no percussion suddenly deciding it belongs to another pattern.

## Pulse phrases

The Pulse rhythm remains unchanged while its notes outline each harmonic section.

### Rows 00–15: F minor

```text
F-4
C-4
G#4
C-4
```

The `F-3` KorgString pad inherited from Pattern 01 continues beneath it.

### Rows 16–31: C minor

```text
C-4
G-4
D#4
G-4
```

### Rows 32–47: A-flat region

```text
G#4
D#4
C-4
D#4
```

### Rows 48–63: G dominant

```text
G-4
D-4
B-4
D-4
```

Pattern 02 then begins with C, resolving the final dominant section.

The `B-4` here is not being asked to act as a grand emotional climax. It is an internal note in a repeating Pulse phrase, where it can perform the modest harmonic function for which it is actually qualified.

## Bell markers

The quiet ExBells notes appear at the same point in each section:

```text
Row 15   G#4
Row 31   D#5
Row 47   C-5
Row 63   G-4
```

The first three use:

```text
C14 = decimal 20
```

The final bell uses:

```text
C10 = decimal 16
```

That last G bell may ring briefly into Pattern 02 before the row-02 hi-hat cuts it. It should behave as a subdued dominant afterimage, not announce the border crossing with a small ceremonial gong.

## Transition behavior

### Pattern 01 → Pattern 0A

Pattern 01 ends with:

```text
F-3 KorgString still playing
G-4 Pulse
G-4 Stab
```

Pattern 0A begins with:

```text
Kick
the same F pad continuing
F-4 Pulse delayed until row 01
```

The groove remains familiar, but the Pulse shifts consistently behind the beat.

### Pattern 0A → Pattern 02

Pattern 0A ends with:

```text
G-4 KorgString
G-dominant Pulse phrase
quiet G-4 ExBells
```

Pattern 02 begins with:

```text
C-4 Pulse
C-4 KorgString
Kick
```

That supplies the intended:

```text
G dominant -> C minor
```

return.

## Audition checklist

```text
[ ] Pattern 01 -> Pattern 0A feels like one groove changing phase
[ ] Pulse attacks at rows 01, 05, 09, and 13 are easy to anticipate
[ ] Pulse remains audible between the drum events
[ ] Every sixteen-row section has the same rhythmic footing
[ ] Harmonic changes provide variety without disturbing the pulse
[ ] Quiet bells sound like phrase markers, not a second lead
[ ] G-major/dominant final section remains controlled
[ ] Pattern 0A -> Pattern 02 resolves naturally
[ ] The pattern has a distinct identity without sounding scattered
```

Current state:

```text
Patterns 00–09:              PASS
Pattern 0A — Phase Lock:     REWRITTEN, AWAITING AUDITION
Revised order list:          UNCHANGED
Final export validation:     PENDING PATTERN 0A PASS
```
