## Pattern 06: Breakdown

Pattern 06 removes most of the rhythmic machinery, lets the pad and bass hang in exposed space, then gradually restarts the pulse during the final sixteen rows.

It appears here:

```text
Pattern 03 -> Pattern 06 -> Pattern 04
```

The design has four stages:

```text
Rows 00-15   Residual pulse
Rows 16-31   Further withdrawal
Rows 32-47   Lowest-energy section
Rows 48-63   Controlled restart
```

Everything not shown remains empty.

```text
Cold Boot
Pattern 06 - Breakdown

   Row   | Ch1             | Ch2             | Ch3             | Ch4
---------+-----------------+-----------------+-----------------+-----------------
00       | ... .. F06      | C-4 04 F91      | C-4 05 C20      | ...
06       | ...             | ...             | ...             | G-4 06 C18
08       | C-4 01 C30      | G-4 04 ...      | ...             | ...
14       | C-4 02 C20      | D#4 04 ...      | ...             | ...

16       | ...             | G#4 04 ...      | A#3 05 C1C      | ...
22       | C-4 01 C28      | ...             | ...             | F#4 06 C14
24       | ...             | D#4 04 ...      | ...             | ...
28       | C-4 02 C1C      | ...             | ...             | ...
30       | ...             | F-4 04 ...      | ...             | ...

32       | ...             | F-4 04 ...      | G#3 05 C18      | ...
38       | ...             | ...             | ...             | F-4 06 C10
40       | ...             | C-4 04 ...      | ...             | ...
44       | C-4 02 C18      | ...             | ...             | ...
46       | ...             | G-4 04 ...      | ...             | ...

48       | C-4 01 C28      | D#4 04 ...      | G-3 05 C20      | ...
50       | ...             | ...             | ...             | C-5 03 C14
52       | C-4 01 C30      | F-4 04 ...      | ...             | ...
54       | ...             | ...             | ...             | C-5 03 C18
56       | C-4 01 C34      | F#4 04 ...      | A#3 05 C24      | ...
58       | ...             | ...             | ...             | C-5 03 C1C
60       | C-4 01 C38      | G-4 04 ...      | C-4 05 C28      | ...
62       | ...             | ...             | ...             | C-4 08 C18
```

### Row 00 detail

```text
... .. F06
```

sets the speed without triggering a drum. Pattern 06 therefore begins with bass and pad alone rather than dutifully thumping on the first row like every machine in existence apparently signed the same percussion contract.

## Dynamic structure

### Rows 00–15: residual pulse

```text
Pad:     C-4 at C20
Bass:    C-3 -> G-3 -> D#3
Drums:   one reduced kick, one reduced snare
Bell:    G-4 at C18
```

This should feel like the remains of Pattern 03 rather than a completely new section.

### Rows 16–31: further withdrawal

```text
Pad:     A#3 at C1C
Bass:    G#3 -> D#3 -> F-3
Kick:    C28
Snare:   C1C
Bell:    F#4 at C14
```

The bell continues the descending diagnostic residue from earlier patterns, but more quietly.

### Rows 32–47: lowest-energy section

```text
Pad:     G#3 at C18
Bass:    F-3 -> C-3 -> G-3
Drums:   one ghost snare only
Bell:    F-4 at C10
```

This is the actual breakdown. The bell should be faint but still detectable.

### Rows 48–63: controlled restart

The kick rises in volume:

```text
Row 48   C28 = decimal 40
Row 52   C30 = decimal 48
Row 56   C34 = decimal 52
Row 60   C38 = decimal 56
```

The hats also rise:

```text
Row 50   C14 = decimal 20
Row 54   C18 = decimal 24
Row 58   C1C = decimal 28
```

The bass climbs:

```text
D#3 -> F-3 -> F#3 -> G-3
```

The pad climbs:

```text
G-3 -> A#3 -> C-4
```

The sweep at row 62 leads directly into Pattern 04. Pattern 04’s first hi-hat on row 02 will cut the sweep, so it should form a short transition rather than lingering around like an unwanted firmware update.

## New volume values

```text
C10 = decimal 16
C14 = decimal 20
C28 = decimal 40
C30 = decimal 48
C34 = decimal 52
C38 = decimal 56
```

All remain valid within ProTracker’s `00–40` hexadecimal volume range.

## Audition checklist

```text
[ ] Pattern 03 -> Pattern 06 transition feels like a deliberate energy drop
[ ] First half remains tense despite the sparse drums
[ ] F-4 bell at C10 is audible but distant
[ ] Ghost snare at row 44 is not too prominent
[ ] Final four kicks produce a convincing volume rise
[ ] Returning hats remain quieter than the kicks
[ ] Sweep at row 62 leads cleanly into Pattern 04
[ ] Pattern 06 -> Pattern 04 transition feels like the machinery restarting
```
