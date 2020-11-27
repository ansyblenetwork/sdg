---
title: "A discussion regarding counterpoint"
---

I was fully intending to make this post about cadences, as an entry into harmony. But then I started reading about cadences, and lost interest, perhaps due to past familiarity but also due to a lack of motive. Further, my current favorite resource, [Integrated Music Theory](https://intmus.github.io/inttheory20-21/05-counterpoint-embell-shapes/1-introcounterpoint.html), discusses counterpoint briefly before proceeding to harmony. I realized then that this is a sensible thing to do: From the perspective of understanding sound and consonance, counterpoint is more direct, pure, and honest, than harmony. It is only my perception about the appropriate order of music curriculum that suggests that harmony should be taught first.

So next I started reading several resources including Integrated Music Theory covering species counterpoint, the classical pedagogical approach recorded by Fux. But this became very dry as well.

I started googling about counterpoint, and I realize that a softer discussion about counterpoint and its value was warranted.


### A brief introduction

We introduce the following terminology:

Parallel motion:

<div id="score"></div>
<script>
makeInteractive("score", `
X:1
L:1/4
K:C
Q:1/2=60
V:1
C|D|E|F
V:2 clef=bass
C,|D,|E,|F,
`);
</script>

Contrary motion:
<div id="score2"></div>
<script>
makeInteractive("score2", `
X:1
L:1/4
K:C
Q:1/2=60
V:1
C|D|E|F
V:2 clef=bass
C,|B,,|A,,|G,,
`);
</script>

Oblique motion:
<div id="score3"></div>
<script>
makeInteractive("score3", `
X:1
L:1/4
K:C
Q:1/2=60
V:1
C|C|C|C
V:2 clef=bass
C,|B,,|A,,|G,,
`);
</script>


Similar motion:
<div id="score4"></div>
<script>
makeInteractive("score4", `
X:1
L:1/4
K:C
Q:1/2=60
V:1
C|E|G|B
V:2 clef=bass
C,|D,|E,|F,
`);
</script>

Counterpoint is taught in incremental steps, known as species. For instance, first species counterpoint drops all nontrivial rhythm, and establishes a set of rules for permissible melodic intervals, harmonic intervals, and movement as enumerated above. A _cantus firmus_, or fixed melody, is provided in the bass, and the exercise is to write a counterpoint voice.

General principles:

1. Independence and integrity: The voices should be distinct, as the whole point is to have dual voices. For instance, octaves are discouraged.
2. Climax and resolution: There should be a unqiue climax and clear resolution.

Melodic intervals: 

1. Use steps (as opposed to larger intervals, or repeated notes).
2. If using large intervals, precede and follow with contrary steps.
3. The final two notes in particular should be related by a step.
2. Have a single climax, which may be emphasized by using a (rare) larger interval.

Harmonic intervals:

1. Start and end with tonic octaves.
2. Perfect intervals should be approached with contrary motion.
3. Allowed intervals: Major and minor thirds and sixths, and perfect fifths or octaves.

Motion:

1. Contrary motion is always acceptable.
2. No parallel octaves or fifths.
3. No similar motion into a perfect interval.

Evidently, this gets fairly dry fairly quickly. Accordingly, there have been some interesting coding projects which [automate the generation](https://luckytoilet.wordpress.com/2011/08/10/algorithmic-counterpoint-how-i-wrote-a-computer-program-to-generate-music-at-mathcamp-2011/) of species counterpoint.

### The discussion

The internet has thorough and reliable information about a lot of topics, but it is surprisingly difficult to find good resources about counterpoint. Here are some natural questions that came to mind, along with the fruits of my research attempting to find answers.

#### Did Bach study or use species counterpoint?

Bach's name hardly appears in the Wikipedia page for counterpoint. In the Wikipedia page for Fux,

<div class="media">
 <p>The Latin edition of Fux's Gradus ad Parnassum from the year 1725 is the only surviving book of J.S. Bach's personal library of theoretical works. As Mizler was a student of J.S. Bach, musicologist Christoph Wolff has suggested that Bach may have played some part in persuading Mizler to translate the treatise.</p>
</div>

Keep in mind that Bach lived from 1685 to 1750, so he was about 40 years old by 1725 when Fux's work was published, by which point Bach's career and style were already well established. One can ask the empirical question however, of whether Bach's music follows the rules of species counterpoint. I am not qualified to answer at this time, and was unable to find a reputable online resource answering this question. However, it seems that the answer is no.
