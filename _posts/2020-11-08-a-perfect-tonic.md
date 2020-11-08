---
title: "A perfect tonic: Naming the intervals"
---

I have an admission to make: It takes me too long - perhaps a second or two - to recall the names of notes written on the staff (I do a better job of it if I'm sitting at a piano). I discovered this when trying to copy sheet music into Musescore the other day. However, I'm not ashamed of this. There is essentially no meaning to the lettered names of the notes; they are merely a semanticless anthropogenic convention.

This brings me to today's question: What are the principles guiding the longform names of the intervals?

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
C[D_B,][EA,][FG,]
w: tonic supertonic/subtonic mediant/submediant dominant/subdominant
`);
D('scale2').style.display = "none";
</script>


1. The _tonic_ is obviously very important and probably has etymologically origins common with the word "tone."
2. _Mediant_ means "middle," and it lies halfway between the tonic and dominant.
3. _Dominant_
