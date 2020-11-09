---
title: "A perfect tonic: Naming the intervals"
---

I have an admission to make: It takes me too long - perhaps a second or two - to recall the names of notes written on the staff (I do a better job of it if I'm sitting at a piano). I discovered this when trying to copy sheet music into Musescore the other day. However, I'm not ashamed of this. There is essentially no meaning to the lettered names of the notes; they are merely a semantic-less anthropogenic convention.

This brings me to today's question: What are the principles guiding the _longform_ names of the intervals?

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

It turns out this chart is anachronistic. The more revealing chart:

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

In particular, note that the major scale has a leading tone, instead of a subtonic which appears in natural and melodic minor scales. Also note that these names are preserved between major and minor scales, so this is not about [interval consonance]({{ "" | relative_url }}{% post_url 2020-11-03-just-intonation-ordering %}), as I suspected on first glance.
