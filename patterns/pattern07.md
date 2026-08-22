## Pattern 07: Climax Pulse

Pattern 07 is the fullest section of **Cold Boot**. It combines:

* Dense kick/snare activity
* Persistent arpeggiated pad
* Faster bass movement
* Rising diagnostic bells
* A continuation of Pattern 04’s chromatically rising stab sequence

It appears here:

```text
Pattern 04 -> Pattern 07 -> Pattern 08
```

Pattern 04 ends with:

```text
G-3 bass
D#4 minor arpeggio
A-4 stab
```

Pattern 07 resolves forcefully to C minor, then moves through:

```text
C minor
G# minor
F minor
G major / dominant tension
```

The final G-major arpeggio is intentionally unresolved. Pattern 08 will use that tension to dismantle the climax and return to Pattern 00.

Everything not shown remains empty.

```text
Cold Boot
Pattern 07 - Climax Pulse

   Row   | Ch1             | Ch2             | Ch3             | Ch4
---------+-----------------+-----------------+-----------------+-----------------
00       | C-4 01 F06      | C-3 04 F91      | C-4 05 037      | ...
02       | ...             | ...             | ... .. 037      | C-5 03 ...
04       | C-4 01 ...      | G-3 04 ...      | ... .. 037      | C-5 03 ...
06       | C-4 01 ...      | C-3 04 ...      | ... .. 037      | C-5 03 ...
07       | ...             | ...             | ...             | G-4 06 C1C
08       | C-4 02 ...      | ...             | ... .. 037      | ...
10       | C-4 01 ...      | D#3 04 ...      | ... .. 037      | C-5 03 ...
12       | C-4 01 ...      | A#3 04 ...      | ... .. 037      | C-5 03 ...
14       | C-4 01 ...      | G-3 04 ...      | ... .. 037      | A#4 07 C28

16       | C-4 01 ...      | G#3 04 ...      | G#3 05 037      | ...
18       | ...             | ...             | ... .. 037      | C-5 03 ...
20       | C-4 01 ...      | D#3 04 ...      | ... .. 037      | C-5 03 ...
22       | C-4 01 ...      | G#3 04 ...      | ... .. 037      | C-5 03 ...
23       | ...             | ...             | ...             | G#4 06 C20
24       | C-4 02 ...      | ...             | ... .. 037      | ...
26       | C-4 01 ...      | B-3 04 ...      | ... .. 037      | C-5 03 ...
28       | C-4 01 ...      | F#3 04 ...      | ... .. 037      | C-5 03 ...
30       | C-4 01 ...      | D#3 04 ...      | ... .. 037      | B-4 07 C2C

32       | C-4 01 ...      | F-3 04 ...      | F-3 05 037      | ...
33       | ...             | ...             | ... .. 037      | ...
34       | C-4 01 ...      | C-3 04 ...      | ... .. 037      | C-5 03 ...
35       | ...             | ...             | ... .. 037      | ...
36       | C-4 01 ...      | ...             | ... .. 037      | C-5 03 ...
37       | ...             | ...             | ... .. 037      | ...
38       | C-4 01 ...      | F-3 04 ...      | ... .. 037      | C-5 03 ...
39       | ...             | ...             | ... .. 037      | A-4 06 C20
40       | C-4 02 ...      | ...             | ... .. 037      | ...
41       | ...             | ...             | ... .. 037      | ...
42       | C-4 01 ...      | G#3 04 ...      | ... .. 037      | C-5 03 ...
43       | ...             | ...             | ... .. 037      | ...
44       | C-4 01 ...      | C-3 04 ...      | ... .. 037      | C-5 03 ...
45       | ...             | ...             | ... .. 037      | ...
46       | C-4 01 ...      | D#3 04 ...      | ... .. 037      | C-5 07 C30
47       | ...             | ...             | ... .. 037      | ...

48       | C-4 01 ...      | G-3 04 ...      | G-3 05 047      | ...
49       | ...             | ...             | ... .. 047      | ...
50       | C-4 01 ...      | D-3 04 ...      | ... .. 047      | C-5 03 ...
51       | ...             | ...             | ... .. 047      | ...
52       | C-4 01 ...      | G-3 04 ...      | ... .. 047      | C-5 03 ...
53       | ...             | ...             | ... .. 047      | ...
54       | C-4 01 ...      | B-3 04 ...      | ... .. 047      | C-5 03 ...
55       | ...             | ...             | ... .. 047      | B-4 06 C24
56       | C-4 02 ...      | ...             | ... .. 047      | ...
57       | ...             | ...             | ... .. 047      | ...
58       | C-4 01 ...      | D-3 04 ...      | ... .. 047      | C-5 03 ...
59       | ...             | ...             | ... .. 047      | ...
60       | C-4 01 ...      | F-3 04 ...      | ... .. 047      | C-5 03 ...
61       | ...             | ...             | ... .. 047      | ...
62       | C-4 01 ...      | G-3 04 ...      | ... .. 047      | C#5 07 C34
63       | ...             | ...             | ... .. 047      | ...
```

## New effect: `047`

```text
047 = major arpeggio

0 = arpeggio effect
4 = four semitones above the base note
7 = seven semitones above the base note
```

Thus:

```text
G-3 05 047
```

cycles through:

```text
G-3
B-3
D-4
```

This is a G-major chord. In the context of C minor, it behaves as a dominant chord, producing a strong unresolved pull back toward C.

That tension is deliberate. Pattern 08 will not begin like another climax pattern; it will progressively strip this dominant energy away before reconnecting with Pattern 00.

## Pad behavior

The first two sections use alternating arpeggio rows:

```text
Arpeggio active on even rows
Base sample pitch held on odd rows
```

The third and fourth sections use continuous arpeggios:

```text
Rows 32–47: continuous F-minor 037
Rows 48–63: continuous G-major 047
```

That gives the pattern an internal rise in harmonic density.

## Stab sequence

Pattern 04 established:

```text
F#4 -> G-4 -> G#4 -> A-4
```

Pattern 07 continues it:

```text
A#4 -> B-4 -> C-5 -> C#5
```

Volumes rise at the same time:

```text
A#4  C28 = decimal 40
B-4   C2C = decimal 44
C-5   C30 = decimal 48
C#5   C34 = decimal 52
```

The result is an eight-stage chromatic climb spanning Patterns 04 and 07:

```text
F#4 G-4 G#4 A-4 | A#4 B-4 C-5 C#5
```

A perfectly reasonable thing for a loading screen to do while pretending nothing alarming is happening.

## Diagnostic bells

The four bell events also climb:

```text
G-4
G#4
A-4
B-4
```

Their volume rises slightly:

```text
C1C
C20
C20
C24
```

The bells sit on odd-numbered rows, leaving the even rows available for hats.

## Rhythmic pressure

Rows 00–31 retain a dense but familiar groove.

Rows 32–63 use nearly continuous two-row drum movement:

```text
kick
kick
kick
kick
snare
kick
kick
kick
```

The final section is the rhythmic peak of the module. Do not increase the global sample volumes for this pattern. Its intensity should come from density and harmony, not from simply making everything louder like a television advertisement.

## Transition intent

### Pattern 04 -> Pattern 07

Pattern 04 ends on:

```text
G-3 bass
D# minor arpeggio
A-4 stab
```

Pattern 07 begins on:

```text
C-3 bass
C minor arpeggio
Kick
```

This should sound like a forceful resolution into the climax.

### Pattern 07 -> Pattern 08

Pattern 07 ends on:

```text
G-3 bass
G-major arpeggio
C#5 stab
```

That combination is intentionally unresolved and somewhat abrasive. Pattern 08 will begin by cutting or replacing those sounds immediately, then reduce the arrangement toward the sparse texture of Pattern 00.

## Audition checklist

```text
[ ] Pattern 04 -> Pattern 07 resolution feels forceful and natural
[ ] Alternating arpeggio in rows 00–31 remains clear
[ ] Continuous 037 in rows 32–47 does not mask the bass
[ ] Continuous 047 in rows 48–63 creates tension rather than cheerfulness
[ ] Bells remain audible among the denser drums
[ ] Rising stab volumes do not clip or dominate
[ ] C#5 final stab sounds intentional
[ ] Final G-major section feels unresolved and ready for Pattern 08
[ ] Overall mix is intense but not overcrowded
```

Current state:

```text
Pattern 00 — Wake Pulse          PASS
Pattern 01 — Main Thump A        PASS
Pattern 02 — Main Thump B        PASS
Pattern 03 — Dark Variation      PASS
Pattern 04 — Pressure Build      PASS
Pattern 05 — Diagnostic Chime    PASS
Pattern 06 — Breakdown           PASS
Pattern 07 — Climax Pulse        COMPOSED, AWAITING AUDITION
```
