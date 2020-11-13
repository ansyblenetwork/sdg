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
C|[D_B,]|[EA,]|[GF,]|
w: tonic supertonic/subtonic mediant/submediant dominant/subdominant
`);
D('scale2').style.display = "none";
</script>


1. The _tonic_ is obviously very important and probably has etymological origins common with the word "tone."
2. The _dominant_ is a perfect fifth above the tonic, also quite important. The _subdominant_ is a perfect fifth below the tonic.
3. _Mediant_ means "middle," and it lies approximately halfway between the tonic and dominant. Likewise, _submediant_ lies halfway between tonic and subdominant.
4. Supertonic and subtonic are whole steps above and below the tonic, respectively.

In particular, observe that the major scale has a [leading tone]({{ "" | relative_url }}{% post_url 2020-11-10-an-objective-construction %}) instead of a subtonic. Also note that these names are preserved between modes, so that this is not about intervals, but scales.

### Intervals

Earlier, we discovered and named the [12 intervals]({{ "" | relative_url }}{% post_url 2020-11-03-just-intonation-and %}). Here we formalize the system:

Intervals are one of the rare musical objects that are named based on notation, rather than intrinsic pitch. The number assigned to the interval is determined by the interval on the staff. Then,

1. Intervals are _major_ if they appear in the major scale.
1. However, the fourth and fifth alone receive the _perfect_ modifier, as they are the primary consonances.
3. If none of the above, the interval is _minor_ if they appear in the minor scale.
4. If still none of the above: Any perfect interval may have the _augmented_ or _diminished_ modifier, which means the interval is a half step larger or smaller, respectively. Major intervals may also receive the augmented modifier, while minor intervals may receive the diminished modifier.

### Triads

A triad consists of two stacked thirds (three notes). There are three variables: Key, quality, and inversion. 

The key is given by the root note, which in turn is given by the bottom note when the triad is explicitly stacked.

There are four qualities:

<div id="scale3"></div>
<script>
makeInteractive("scale3", `
X:1
K:C
L: 1/4
Q:1/4=60
  [CEG}|[CE^G]|[C_EG]|[C_E_G]|
w: major augmented minor diminished~
`);
</script>

1. Major: A major third and perfect fifth.
2. Augmented: Major but with augmented fifth.
3. Minor: A minor third and perfect fifth.
4. Diminished: Minor but with diminished fifth.

Triads may be inverted, enumerated by the bass (lowest) note:
<div id="scale4"></div>
<script>
makeInteractive("scale4", `
X:1
K:C
L: 1/4
Q:1/4=60
  [CEG}|[C'EG]|[CEG,]|
w: root~position first~inversion second~inversion
`);
</script>

In summary, the root note determines the key (C, in all of the examples above); the bass note determines the inversion.

### Seventh chords

A seventh chord adds a seventh to a triad. There are five:

1. Major: Adds a major seventh to a major triad.
2. Dominant: Adds a minor seventh to a major triad.
3. Minor: Adds a minor seventh to a minor triad.
4. Half-diminished: Adds a minor seventh to a diminished triad.
5. Diminished: Adds a diminished seventh to a diminished triad.

Seventh chords may also be inverted with the natural naming scheme (up to a third inversion).

