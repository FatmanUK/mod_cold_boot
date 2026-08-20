## Pattern 05: Diagnostic Chime

Time for the machine to begin issuing reassuring diagnostic tones, which naturally means increasingly suspicious chromatic beeping.

Pattern 05 is the tune’s clearest melodic focal point, but it still behaves like a system-status sequence rather than a conventional lead melody.

Its pad rises chromatically:

```text
C-4 -> C#4 -> D-4 -> D#4
```

That deliberately mirrors Pattern 03’s descent:

```text
D#4 -> D-4 -> C#4 -> C-4
```

So the sequence:

```text
Pattern 05 -> Pattern 03
```

forms an ascending scan followed by a descending response.

Pattern 05 must support:

```text
Pattern 02 -> Pattern 05 -> Pattern 03
```

Everything not listed remains empty.

```text
Cold Boot
Pattern 05 - Diagnostic Chime

   Row   | Ch1             | Ch2             | Ch3             | Ch4
---------+-----------------+-----------------+-----------------+-----------------
00       | C-4 01 F06      | C-3 04 F91      | C-4 05 ...      | ...
02       | ...             | ...             | ...             | G-4 06 C1C
06       | C-4 01 ...      | ...             | ...             | C-5 06 C20
08       | C-4 02 ...      | G-3 04 ...      | ...             | ...
10       | ...             | ...             | ...             | D#5 06 C20
12       | C-4 01 ...      | D#3 04 ...      | ...             | ...
14       | ...             | ...             | ...             | D-5 06 C1C

16       | C-4 01 ...      | C#3 04 ...      | C#4 05 ...      | ...
18       | ...             | ...             | ...             | G#4 06 C1C
22       | C-4 01 ...      | ...             | ...             | C#5 06 C20
24       | C-4 02 ...      | G#3 04 ...      | ...             | ...
26       | ...             | ...             | ...             | E-5 06 C20
28       | C-4 01 ...      | E-3 04 ...      | ...             | ...
30       | ...             | ...             | ...             | D#5 06 C1C

32       | C-4 01 ...      | D-3 04 ...      | D-4 05 ...      | ...
34       | ...             | ...             | ...             | A-4 06 C1C
38       | C-4 01 ...      | ...             | ...             | D-5 06 C20
40       | C-4 02 ...      | A-3 04 ...      | ...             | ...
42       | ...             | ...             | ...             | F-5 06 C20
44       | C-4 01 ...      | F-3 04 ...      | ...             | ...
46       | ...             | ...             | ...             | E-5 06 C1C

48       | C-4 01 ...      | D#3 04 ...      | D#4 05 ...      | ...
50       | ...             | ...             | ...             | A#4 06 C1C
54       | C-4 01 ...      | ...             | ...             | D#5 06 C20
56       | C-4 02 ...      | A#3 04 ...      | ...             | ...
58       | ...             | ...             | ...             | F#5 06 C20
60       | C-4 01 ...      | F#3 04 ...      | ...             | ...
62       | ...             | G-3 04 ...      | ...             | F-5 06 C1C
```

### Chime logic

Each 16-row section follows the same diagnostic shape:

```text
fifth
root
minor third
warning note one semitone below the minor third
```

The four sequences are:

```text
C minor:
G-4  C-5  D#5  D-5

C# minor:
G#4  C#5  E-5  D#5

D minor:
A-4  D-5  F-5  E-5

D# minor:
A#4  D#5  F#5  F-5
```

The pattern therefore sounds systematic rather than tuneful. It is effectively the same diagnostic test being repeated at successively higher pitches. Humans do enjoy assuming rising beeps mean progress.

### Chime volume contour

```text
C1C = decimal 28
C20 = decimal 32
```

Each four-note sequence uses:

```text
C1C -> C20 -> C20 -> C1C
```

That makes the middle two notes the clearest part of each diagnostic phrase while keeping the outer notes slightly recessed.

### Drum and texture design

Pattern 05 deliberately contains:

```text
Kick
Snare
Bass
Pad
ExBells
```

It contains no hi-hats and no stabs. Removing the hats creates enough space for the much denser bell activity.

The drum cycle repeats every 16 rows:

```text
Section start: kick
Row +6:        kick
Row +8:        snare
Row +12:       kick
```

### Transition intent

#### Pattern 02 -> Pattern 05

Pattern 02 ends with:

```text
C-3 bass
C-5 ExBells
G-3 pad still sounding
```

Pattern 05 begins with:

```text
C-3 bass
C-4 pad
Kick
```

The first new bell waits until row 02, preventing an immediate chime collision at the pattern boundary.

#### Pattern 05 -> Pattern 03

Pattern 05 ends with:

```text
D#4 pad
G-3 bass
F-5 bell
```

Pattern 03 begins with:

```text
D#4 pad
C-3 bass
Kick
```

The retained `D#4` pad ties the two patterns together while the bass resolves from `G-3` to `C-3`. Pattern 03 then begins its chromatic pad descent.

### Audition checklist

```text
[x] Pattern 02 -> Pattern 05 transition is smooth
[x] Diagnostic motif is clear without sounding cheerful
[x] ExBells density does not overwhelm the rhythm
[x] C1C notes remain audible
[x] Chromatic pad rise works
[x] Pattern 05 -> Pattern 03 transition is smooth
[x] Repeated D#4 pad at the boundary does not click unpleasantly
```
