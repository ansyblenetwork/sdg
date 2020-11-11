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

In particular, recall that the major scale has a [leading tone]({{ "" | relative_url }}{% post_url 2020-11-10-an-objective-construction %}) instead of a subtonic. Also note that these names are preserved between modes, so that other than the dominant and subdominant, this is not about intervals, but scales.
