---
title: "An objective construction of the major, minor, and pentatonic scales"
---

To what extent do the major and minor scales of classical Western music, and the pentatonic scale of Eastern music, have mathematical origins? To what extent are they merely ingrained through habituation? It isn't so easy to find a definitive answer to these questions. I encountered a lot of partial answers, but which always seemed to fall short. Below is what I have decided is the most objective construction, pieced together from various sources.

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

First, I will insist that we preserve the unit wavelength note as the tonic of our scale. Many resources observe that the notes of the major scale are contiguous if we begin our generation at the perfect forth and cycle through to the major seventh, essentially reassigning the tonic note. However, this fails to explain why the major and minor scales are the [most commonly used modes]({{ "" | relative_url }}{% post_url 2020-11-09-diatonic-modes-a %}). Given the strikingly different moods a scale can evoke simply by shifting the tonic note, we should seek a contruction that preserves the tonic throughout.

There are many disonances contained within the twelve notes. In particular, the diminished fifth forms the most dissonant interval with the tonic, also known as a _tritone_. The tritone is so dissonant that we should consider removing all the tritone intervals that appear within our notes. In the following chart, we pair the 12 notes by tritone formation:

| Note | Tritone pair |
| ------------- | ------------- |
| tonic | diminished fifth |
| perfect fifth | minor second |
| perfect fourth&nbsp;&nbsp;&nbsp;&nbsp; | major seventh |
| major third | minor seventh |
| major sixth | minor third |
| major second | minor sixth |

But which of each pair do we remove? For the moment, pretend that the major scale lacks the major seventh, and that the minor scale lacks the major second. Then the construction of each scale would use the following reasoning:

Within the chart, the tonic, perfect fourth, and perfect fifth are our primary consonances and non-negotiable; we must keep them, and summarily dispose of the diminished fifth, minor second, and major seventh. 

Then we have a degree of freedom. If we remove the minor seventh, this means we keep the major third. In turn, it becomes convenient to keep the major sixth as we have just removed one of its (dissonant) half step neighbors, and to remove its tritone pair, the minor third, as we have just inked one of its half step neighbors. If we proceed as such, it in turn is natural to remove finally the minor sixth. We obtain the pre-major scale.

If we chose instead to remove the major third and keep the minor seventh, we end with the pre-minor scale.

However, the minor third gap at the end and beginning of the major and minor scales respectively, is awkward and should be repaired. The re-insertion of the major seventh, also known as the _leading tone_, completes the major scale. This is particularly appropriate as the seventh tone resolves to the tonic very strongly, ending the scale. On the other hand, the minor scale should not begin with a half step, as this would want to resolve back downward; the major second is a better bet.

In conclusion, there seem to be four principles that the major and minor scales satisfy:

1. No major second gaps.
2. Remove tritones and half-steps, as long as (1) is satisfied.
3. The perfect fourth and fifth are not to be tampered with.
4. Leading tones occur at the end of the scale, not the beginning.

All of the [diatonic modes]({{ "" | relative_url }}{% post_url 2020-11-09-diatonic-modes-a %}) satisfy (1) and (2), but only the major and minor scales satisfy (3) and (4).


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

The mathematical description of the pentatonic scale is simple: It is the unique largest scale with no tritones or half steps. It can be constructed from the pre-major scale by removing the last remaining half step, the perfect fourth:

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 1/2 | octave |
