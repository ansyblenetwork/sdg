---
title: "The major, minor, and pentatonic scales: An objective construction"
---

To what extent do the major and minor scales of classical Western music, and the pentatonic scale of Eastern music, have mathematical origins? To what extent are they merely ingrained through habituation? I did a lot of research trying to find a definitive answer to these questions. I found a lot of partial answers, but which always seemed to fall short. Below is what I have decided is the most objective construction, pieced together from various sources.

### Tritone removal

I will copy here the table of intervals from our discussion of the [consonant intervals]({{ "" | relative_url }}{% post_url 2020-11-03-just-intonation-and %}):

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 8/15 | major seventh (inversion of minor second) |
| 32/45 | diminished fifth (inversion of itself) |
| 15/16 | minor second (inversion of major seventh) |
| 5/8 | minor sixth (inversion of major third) |
| 5/6 | minor third (inversion of major sixth) |
| 9/16 | minor seventh (inversion of major second) |
| 3/4 | perfect fourth (inversion of perfect fifth) |
| 1/2 | octave |

First, I will insist that we preserve the unit wavelength note as the tonic of our scale. Many resources mention that the notes of the major scale are contiguous if we begin our generation at the perfect forth and cycle through to the major seventh, essentially reassigning the tonic note. However, this fails to explain why the major and minor scales are the [most commonly used modes]({{ "" | relative_url }}{% post_url 2020-11-09-diatonic-modes-a %}). Given the strikingly different moods a scale can evoke simply by shifting the tonic note, we should seek a contruction that preserves the tonic throughout.

There are many disonances contained within these twelve notes. Given our tonic note, what is the most dissonant note? The most natural answer is the diminished fifth, which forms the most dissonant interval, also known as a _tritone_.

In fact, the tritone is so dissonant that we should consider removing all the tritone intervals that appear within our notes. In the following chart, we pair the 12 notes by tritone formation:

| Note | Tritone pair |
| ------------- | ------------- |
| tonic | diminished fifth |
| perfect fifth | minor second |
| perfect fourth | major seventh |
| major third | minor seventh |
| major sixth | minor third |
| major second | minor sixth |

For the moment, pretend that the major scale lacks the major seventh, and that the minor scale lacks the majors second. Then the construction of each scale would use the following reasoning:

Within the chart, the tonic, perfect fourth, and perfect fifth are our primary consonances and non-negotiable; we must keep them, and summarily dispose of the diminished fifth, minor second, and major second. 

Then we have a degree of freedom. If we remove the minor seventh, this means we keep the major third. This makes it tempting to keep the major sixth as we have just removed a (dissonant) half step neighbor, and to remove the minor third, as we have just fixed a half-step neighbor. We accordingly remove the minor third and keep the major sixth. In turn, it is natural to remove finally the minor sixth. We obtain the pre-major scale.

If we chose instead to remove the major third and keep the minor seventh, we end with the pre-minor scale.

However, the major second at the end and beginning of the major and minor scales respectively, is odd and should be repaired. The re-insertion of the major seventh, also known as the _leading tone_, completes the major scale. This is particularly appropriate as the seventh tone resolves to the tonic very strongly. On the other hand, the minor scale should not begin with a half step, as this would want to resolve back downward; the major second is a better bet.

In conclusion, there seem to be three principles that the major and minor scales satisfy:

1. Use as few tritones and half-steps as possible, without introducing major second gaps.
2. Leading tones occur at the end of the scale, not the beginning.
3. Perfect fourths and fifths should not be tampered with.

All the [diatonic modes]({{ "" | relative_url }}{% post_url 2020-11-09-diatonic-modes-a %}) satisfy (1), but only the major and minor scales satisfy both (2) and (3).


### The pentatonic scale: Half step removal

The pentatonic scale is less well known to classical pianists (as far as I am aware). I only discovered it recently. See [this video](https://www.youtube.com/watch?v=MGpUscFY9RA) by David Bennett for a nice overview of its use in popular and Asian music. In a nutshell, it is the scale consisting of the black keys on a piano:

<div id="scale"></div>
<script>
makeInteractive("scale", `
X:1
K:C
L: 1/4
Q:1/4=60
^F^G^A^C'^D'
`);
</script>

The mathematical origins are simpler than those of the diatonic scale. If we continued removing the most dissonant notes from the major scale, we would first remove the major seventh, as it forms a minor second with our tonic. Then, we would remove the perfect fourth, as it forms a minor second with our perfect fifth (which we certainly are not going to remove):

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 1/2 | octave |
