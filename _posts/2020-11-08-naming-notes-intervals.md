---
title: "Naming notes, intervals, chords, and triads"
---

I essentially didn't study music theory growing up; I crammed for ABRSM grade 5 theory over a few weeks, which if I recall, was a prerequisite to take the grade 8 performance exam.

This post is a crash course on musical terminology.

### Scale degree names

<div id="scale"></div>
<script>
makeInteractive("scale", `
X:1
K:C
L: 1/4
Q:1/4=60
CDEFGAB
w: tonic supertonic mediant subdominant dominant submediant leading~tone
`);
D('scale').style.display = "none";
</script>

It turns out this chart is anachronistic. Below is the more revealing chart:

<div id="scale2"></div>
<script>
makeInteractive("scale2", `
X:1
K:C
L: 1/4
Q:1/4=60
C[D_B,][EA,][GF,]
w: tonic supertonic/subtonic mediant/submediant dominant/subdominant
`);
D('scale2').style.display = "none";
</script>


1. The _tonic_ is obviously very important and probably has etymological origins common with the word "tone."
2. The _dominant_ is a perfect fifth above the tonic, also quite important. The _subdominant_ is a perfect fifth below the tonic.
3. _Mediant_ means "middle," and it lies approximately halfway between the tonic and dominant. Likewise, _submediant_ lies halfway between tonic and subdominant.
4. Supertonic and subtonic are whole steps above and below the tonic, respectively.

In particular, recall that the major scale has a [leading tone]({{ "" | relative_url }}{% post_url 2020-11-10-an-objective-construction %}) instead of a subtonic. Also note that these names are preserved between modes, so that this is not about intervals, but scales.

### Intervals

Earlier, we discovered and named the [12 intervals]({{ "" | relative_url }}{% post_url 2020-11-03-just-intonation-and %}). Here we formalize the system:

1. The fourth and fifth alone receive the "perfect" modifier, as they are the primary consonances.
2. Other intervals are major if they come from the major scale.
3. Next, if they are from the minor scale, they are minor.
4. Lastly, any interval may have the augmented or diminished modifier, which means the interval is a half step larger or smaller, respectively.

### Chords and triads

As I understand it, "chord" is the more general term. A triad must refer to a collection of three notes. There are four triads:

1. Major: A major third and perfect fifth.
2. Augmented: Raises the perfect fifth of a major triad by a half step.
3. Minor: A minor third and perfect fifth.
4. Diminished: Lowers the perfect fifth of a minor triad by a half step.

<div id="scale3"></div>
<script>
makeInteractive("scale3", `
X:1
K:C
L: 1/4
Q:1/4=60
  [CEG}[CE^G][C_EG][C_E_G]
w: major~ augmented~ minor~ diminished~
`);
</script>


