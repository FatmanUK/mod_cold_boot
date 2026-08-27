# Pattern 08: Release, Echo, Return

Pattern 08 now begins with a half-time C-minor statement.

Its first and second sixteen-row phrases use the same rhythmic and melodic structure:

```text
Rows 00–15: full statement
Rows 16–31: quieter echo
```

The final 32 rows move into Pattern 00’s sparse eight-row pulse.

Everything not shown remains empty.

```text
Cold Boot
Pattern 08 - Release, Echo, Return

   Row   | Ch1             | Ch2             | Ch3             | Ch4
---------+-----------------+-----------------+-----------------+-----------------
00       | C-4 01 C30      | C-3 04 C40      | C-4 05 C28      | D#5 06 C28
01       | ...             | ...             | ... .. 037      | ...
02       | ...             | ...             | ... .. 037      | ...
03       | ...             | ...             | ... .. 037      | ...
04       | ...             | G-3 04 C40      | ...             | ...
08       | C-4 02 C28      | D#3 04 C40      | ...             | ...
12       | C-4 01 C2C      | G-3 04 C40      | ...             | C-5 06 C18

16       | C-4 01 C28      | C-3 04 C38      | C-4 05 C20      | D#5 06 C1C
17       | ...             | ...             | ... .. 037      | ...
18       | ...             | ...             | ... .. 037      | ...
19       | ...             | ...             | ... .. 037      | ...
20       | ...             | G-3 04 C38      | ...             | ...
24       | C-4 02 C20      | D#3 04 C38      | ... .. C20      | ...
28       | C-4 01 C24      | G-3 04 C38      | ...             | C-5 06 C14

32       | C-4 01 C2C      | F-3 04 C38      | F-3 05 C20      | ...
40       | C-4 01 C2C      | C-3 04 C38      | G-3 05 C1C      | ...
44       | ...             | ...             | ...             | C-5 03 C14
46       | ...             | G-3 04 C38      | ...             | ...

48       | C-4 01 C30      | F-3 04 C38      | G-3 05 C18      | ...
56       | C-4 01 C30      | G-3 04 C38      | ...             | ...
60       | ...             | ...             | ...             | C-5 03 C18
```

## Pattern 07 to Pattern 08 resolution

The resolution no longer depends on a lone `B-4 -> C-5` motion.

Pattern 07 ends with:

```text
G bass
G-major pad containing B
F-5 bell
```

Pattern 08 begins with:

```text
C bass
C-minor pad containing D#
D#5 bell
```

The voice leading is:

```text
B  -> C
F  -> D#
G  -> C
```

The audible top-note resolution is now:

```text
F-5 -> D#5
```

while the pad handles the leading-tone movement internally.

That is a proper dominant-seventh resolution into C minor, rather than asking one rather ordinary stab to carry the emotional weight of the entire module. It had neither the training nor the temperament.

## The climax release

Rows 00–15 use only:

```text
Kick
Snare
PopBass
KorgString
Two ExBells notes
```

There are:

```text
No hats
No Stabs
No continuous wall of arpeggio
```

The pad begins as a plain `C-4` at reduced volume. The arpeggio enters on rows 01–03, after the bell and kick transients. This should create a chord bloom instead of all four channels shouting on row 00.

The half-time drum shape is:

```text
Row 00   kick
Row 08   snare
Row 12   kick
```

That should feel broad and conclusive.

## The actual echo

Rows 16–31 repeat the same layout exactly sixteen rows later:

```text
00 -> 16   kick, C bass, C pad, D# bell
04 -> 20   G bass
08 -> 24   snare, D# bass
12 -> 28   kick, G bass, C bell
```

The echo uses lower values throughout:

```text
Bass:  C40 -> C38
Pad:   C28 -> C20
Bell:  C28/C18 -> C1C/C14
Drums: C30/C28/C2C -> C28/C20/C24
```

This should read as the first phrase reflecting back from farther away, not merely as “the next quiet bit.”

## Return to Pattern 00

Rows 32–63 use the same sparse timing vocabulary as Pattern 00:

```text
Row 32   kick, bass, pad
Row 40   kick, bass, pad
Row 44   hat
Row 48   kick, bass, pad
Row 56   kick, bass
Row 60   hat
```

The final bass movement is:

```text
F -> C -> G
F -> G
then Pattern 00: C
```

The final loop will probably remain perceptible to someone actively listening for it. The goal is now that it feels like the pulse has slowed, turned over, and begun another cycle, rather than that MilkyTracker reached the end of a list and started reading it again.

# Audition checklist

## Pattern 04 to Pattern 07

```text
[ ] The drum break continues across the boundary
[ ] Pattern 07 row 00 does not feel like a rhythmic reset
[ ] Delayed bass attacks are clearly audible
[ ] PopBass is no longer swallowed by kick and snare
```

## Pattern 07 final section

```text
[ ] Pulsed 047 is tense but not noisy
[ ] G, D, F, G bass movement is audible
[ ] Final F-5 bell feels consequential
[ ] The absence of a final Stab improves the dominant hold
```

## Pattern 08 release

```text
[ ] F-5 -> D#5 feels more satisfying than B-4 -> C-5
[ ] Opening row is strong without being noisy
[ ] Rows 00–15 feel broad and conclusive
[ ] Bass remains audible beneath the reduced drums
```

## Pattern 08 echo and loop

```text
[ ] Rows 16–31 clearly echo rows 00–15
[ ] Echo sounds quieter, not merely emptier
[ ] Rows 32–63 reduce energy smoothly
[ ] Pattern 08 -> Pattern 00 feels like phrase turnover
[ ] Two complete order-list passes remain musically convincing
```

Current state:

```text
Pattern 00 — Wake Pulse                  PASS
Pattern 01 — Main Thump A                PASS
Pattern 02 — Main Thump B                PASS
Pattern 03 — Dark Variation              PASS
Pattern 04 — Pressure Build              PASS
Pattern 05 — Diagnostic Chime            PASS
Pattern 06 — Breakdown                   PASS
Pattern 07 — Break to Dominant           REVISED, AWAITING AUDITION
Pattern 08 — Release, Echo, Return       REVISED, AWAITING AUDITION
```
