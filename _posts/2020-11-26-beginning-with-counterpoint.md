---
title: "Beginning with counterpoint"
---

I was fully intending to make this post about cadences, as an entry into harmony. But then I started reading about cadences, and lost interest, perhaps due to past familiarity but also due to a lack of motive. Further, my current favorite resource, [Integrated Music Theory](https://intmus.github.io/inttheory20-21/05-counterpoint-embell-shapes/1-introcounterpoint.html), discusses counterpoint briefly before proceeding to harmony. I realized then that this is a sensible thing to do: From the perspective of understanding sound and consonance, counterpoint is more direct, pure, and honest, than harmony. It is only my perception about the appropriate order of music curriculum that suggests that harmony should be taught first.

The content here is standard in music theory, established by Fux. Still, I'm not familiar with it, so I reproduce it here.


### Contrapunctal motion

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


### First species counterpoint

Counterpoint is taught in incremental steps, known as species. First species counterpoint drops all nontrivial rhythm, and establishes a set of rules for permissible melodic intervals, harmonic intervals, and movement as enumerated above. A _cantus firmus_, or fixed melody, is provided in the bass, and the exercise is to write a counterpoint voice.

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
