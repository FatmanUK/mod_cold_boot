## Pattern 04: Pressure Build

Pattern 04 increases tension in four stages. The drums and hats become progressively denser, the bass climbs through four chromatic minor centres, and the pad introduces a classic ProTracker minor-chord arpeggio.

It must work in two places:

```text
Pattern 03 -> Pattern 04 -> Pattern 02
Pattern 06 -> Pattern 04 -> Pattern 07
```

The ending therefore sits on a strong `G-3` bass tension, ready to resolve into a C-centred following pattern.

Everything not shown remains empty.

```text
Cold Boot
Pattern 04 - Pressure Build

   Row   | Ch1             | Ch2             | Ch3             | Ch4
---------+-----------------+-----------------+-----------------+-----------------
00       | C-4 01 F06      | C-3 04 F91      | C-4 05 037      | ...
01       | ...             | ...             | ... .. 037      | ...
02       | ...             | ...             | ...             | C-5 03 ...
04       | ...             | C-3 04 ...      | ...             | ...
06       | C-4 01 ...      | ...             | ...             | ...
08       | C-4 02 ...      | G-3 04 ...      | ... .. 037      | ...
09       | ...             | ...             | ... .. 037      | ...
10       | ...             | ...             | ...             | C-5 03 ...
12       | C-4 01 ...      | D#3 04 ...      | ...             | ...
14       | ...             | G-3 04 ...      | ...             | F#4 07 C18

16       | C-4 01 ...      | C#3 04 ...      | C#4 05 037      | ...
17       | ...             | ...             | ... .. 037      | ...
18       | ...             | ...             | ... .. 037      | C-5 03 ...
20       | C-4 01 ...      | G#3 04 ...      | ...             | ...
22       | C-4 01 ...      | ...             | ...             | C-5 03 ...
24       | C-4 02 ...      | E-3 04 ...      | ... .. 037      | ...
25       | ...             | ...             | ... .. 037      | ...
26       | ...             | ...             | ... .. 037      | C-5 03 ...
28       | C-4 01 ...      | C#3 04 ...      | ...             | ...
30       | C-4 01 ...      | G#3 04 ...      | ...             | G-4 07 C1C

32       | C-4 01 ...      | D-3 04 ...      | D-4 05 037      | ...
33       | ...             | ...             | ... .. 037      | ...
34       | ...             | ...             | ... .. 037      | C-5 03 ...
35       | ...             | ...             | ... .. 037      | ...
36       | C-4 01 ...      | A-3 04 ...      | ...             | C-5 03 ...
38       | C-4 01 ...      | ...             | ...             | ...
40       | C-4 02 ...      | F-3 04 ...      | ... .. 037      | ...
41       | ...             | ...             | ... .. 037      | ...
42       | ...             | ...             | ... .. 037      | C-5 03 ...
43       | ...             | ...             | ... .. 037      | ...
44       | C-4 01 ...      | D-3 04 ...      | ...             | C-5 03 ...
46       | C-4 01 ...      | A-3 04 ...      | ...             | G#4 07 C20

48       | C-4 01 ...      | D#3 04 ...      | D#4 05 037      | ...
49       | ...             | ...             | ... .. 037      | ...
50       | ...             | ...             | ... .. 037      | C-5 03 ...
51       | ...             | ...             | ... .. 037      | ...
52       | C-4 01 ...      | A#3 04 ...      | ... .. 037      | C-5 03 ...
53       | ...             | ...             | ... .. 037      | ...
54       | C-4 01 ...      | ...             | ... .. 037      | C-5 03 ...
55       | ...             | ...             | ... .. 037      | ...
56       | C-4 02 ...      | F#3 04 ...      | ... .. 037      | ...
57       | ...             | ...             | ... .. 037      | ...
58       | C-4 01 ...      | D#3 04 ...      | ... .. 037      | C-5 03 ...
59       | ...             | ...             | ... .. 037      | ...
60       | C-4 01 ...      | A#3 04 ...      | ... .. 037      | C-5 03 ...
61       | ...             | ...             | ... .. 037      | ...
62       | C-4 01 ...      | G-3 04 ...      | ... .. 037      | A-4 07 C24
63       | ...             | ...             | ... .. 037      | ...
```

### New effect: `037`

```text
037 = arpeggio

0 = effect number
3 = play three semitones above the base note
7 = play seven semitones above the base note
```

For example:

```text
C-4 05 037
```

cycles rapidly through:

```text
C-4
D#4
G-4
```

That produces a C-minor chord from a single channel. At Speed 6, ProTracker cycles through the three pitches twice during each row.

An effect-only event such as:

```text
... .. 037
```

continues applying the arpeggio to the pad note already playing on that channel.

### Stab-volume rise

The four stabs gradually become louder:

```text
C18 = decimal 24
C1C = decimal 28
C20 = decimal 32
C24 = decimal 36
```

Their pitches also rise chromatically:

```text
F#4 -> G-4 -> G#4 -> A-4
```

Each is a tritone above its current pad root, preserving the cold, unstable character.

### Intended pressure curve

```text
Rows 00-15:
C minor centre
Sparse hats
Short arpeggio flashes

Rows 16-31:
C# minor centre
More kick activity
Longer arpeggio bursts

Rows 32-47:
D minor centre
Denser percussion
Stronger stab

Rows 48-63:
D# minor centre
Continuous pad arpeggio
Maximum drum density
G-3 bass ending prepares the next pattern
```

If the continuous `037` effect in rows 48–63 feels too buzzy with your particular `KorgString`, the conservative adjustment is to remove it from the odd-numbered rows:

```text
49, 51, 53, 55, 57, 59, 61, 63
```

That preserves the build while making the final arpeggio pulse every other row.
