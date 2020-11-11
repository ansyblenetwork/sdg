---
title: "Diatonic modes: A scale of scales from major to minor"
---

While I was researching the origins of the major scale, I found very many articles trying to answer the question of why the major scale sounds happy, while the minor scale sound sad. The most satisfactory answer seems to be via the spectrum of brightness and darkness assigned to the various modes of the diatonic scale.

### By frequency pattern

One way to organize the multiple diatonic modes which makes transparent their close relationship, is to group the modes which use the same notes, and enumerate them by their starting note:

| Starting note | Name |
| ------------- | ------------- |
| 1 | Ionian (major) |
| 2 | Dorian  |
| 3 | Phrygian |
| 4 | Lydian |
| 5 | Mixolydian |
| 7 | Aeolian (natural minor) |
| 7 | Locrian |

However, the symmetry provided by this view obscures why the major scale has risen to the top of many musical traditions. It also fails to explain why the major scale sounds "happy" while the minor scale sounds "sad." 

The former question seems to be more difficult to answer, and I will attempt to address it in a later post.

### By sharps and flats

To answer the latter question, we can group the diatonic modes instead by starting note, and enumerate them by their relative sharps and flats:

| Accidentals relative to Ionian | Name |
| ------------- | ------------- |
| #4 | Lydian |
| none | Ionian (major) |
| b7 | Mixolydian |
| b3, b7 | Dorian  |
| b3, b7, b6 | Aeolian (natural minor) |
| b3, b7, b6, b2 | Phrygian |
| b3, b7, b6, b2, b5 | Locrian |

It is easy to believe, and [studies have shown](https://www.researchgate.net/publication/259731533_Emotional_Connotations_of_Diatonic_Modes), that the number of flats correlates with the brightness or happiness of the scale. Perhaps you can judge for yourself:

<div id="scale1"></div>
<div id="scale2"></div>
<div id="scale3"></div>
<div id="scale4"></div>
<div id="scale5"></div>
<div id="scale6"></div>
<div id="scale7"></div>
<script>
makeInteractive("scale1", `
X:1
R:Lydian
K:C
L: 1/4
Q:1/2=60
CDE^FGABC'
`);
makeInteractive("scale2", `
X:1
R:Ionian (major)
K:C
L: 1/4
Q:1/2=60
CDEFGABC'
`);
makeInteractive("scale3", `
X:1
R:Mixolydian
K:C
L: 1/4
Q:1/2=60
CDEFGA_BC'
`);
makeInteractive("scale4", `
X:1
R:Dorian
K:C
L: 1/4
Q:1/2=60
CD_EFGA_BC'
`);
makeInteractive("scale5", `
X:1
R:Aeolian (natural minor)
K:C
L: 1/4
Q:1/2=60
CD_EFG_A_BC'
`);
makeInteractive("scale6", `
X:1
R:Phrygian
K:C
L: 1/4
Q:1/2=60
C_D_EFG_A_BC'
`);
makeInteractive("scale7", `
X:1
R:Locrian
K:C
L: 1/4
Q:1/2=60
C_D_EF_G_A_BC'
`);
</script>
