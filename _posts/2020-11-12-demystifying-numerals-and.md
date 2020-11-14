---
title: "Demystifying numerals and lead sheet notation"
---

Today we will try to resolve something that has always been a mystery to me: Sheet music for jazz and popular music. In particular, what is the meaning behind those numerals, spontaneously capitalized, peppered with superscripted 7's?

### Introduction

First, the basics: Numerals and lead sheet notation both refer to chords and triads. [Open music theory](https://viva.pressbooks.pub/openmusictheory/chapter/lead-sheet-symbols/) comments on the philosophical difference:

<div class="media">
<p>Roman numerals are more theoretical and abstract, because they tell you the location of a chord relative to the key of the song. Lead sheet symbols, on the other hand, tell you exactly (absolutely) which notes are being played in this given chord, without reference to any outside system...</p>
  
<p>In other words, the purpose of lead sheet symbols is to get performers’ fingers to the right notes at the right time.</p>
</div>

On the other hand, the absense of a theoretical connotation is sometimes useful when none is intended.

Note that there are notational variations in the literature, particularly among lead sheet symbols.

### Lead sheet notation

Lead sheets are commons for jazz and popular music. The notation appears above a staff which carries the melody. The symbols represent accompanying chords, which the performer is to play at his or her own discretion, referred to as "voicing," guided by the following instructions:

1. Key/root: The main letter of the symbol. Straightforward.
2. Quality: Major unless indicated otherwise: Lowercase m for minor, + for augmented, o for diminished.
3. Inversion: The lowest note is indicated after a slash. Cm/Eb is a first inversion C minor triad. The lowest note needn't be part of the triad.
4. Sevenths: A superscripted 7. Defaults to dominant seventh. Otherwise, the quality will be indicated.
5. Sustained: A modifer common in jazz and popular music which replaces the middle third of a triad by a fourth.

<div id="score"><div>
<script>
makeInteractive("score", `
X:1
L:1/4
K:C
Q:1/4=60
"Dm"[DFA]|"D7"[D^FAc]| "D7/F#"[d^FAc]| "Dsus7"[DGAc]|
`);
</script>
