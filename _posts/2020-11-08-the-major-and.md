---
title: "The major and pentatonic scales: An objective construction"
---

To what extent does the major scale of classical Western music, and the pentatonic scale of Eastern music, have mathematical origins? To what extent are they merely ingrained through habituation? I did a lot of research trying to find a definitive answer to these questions. I found a lot of partial answers, but which always seemed to fall short. Below is what I have decided is the most objective construction, pieced together from various sources.

### Tritone removal

I will copy here the table of intervals from our discussion of the [consonant intervals]({{ "" | relative_url }}{% post_url 2020-11-03-just-intonation-ordering %}):

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

First, I will insist that we preserve the unit wavelength note as the tonic of our scale. Many resources point out that the notes of the major scale are contiguous if we begin our generation at the perfect forth and cycle through to the major seventh, but this fails to explain why the major scale seems to be the [most consonant mode]({{ "" | relative_url }}{% post_url 2020-11-09-diatonic-modes-from %}).

There are many disonances contained within these twelve notes. Given our tonic note, what is the most dissonant note? The most natural answer is the diminished fifth, which forms the most dissonant interval, also known as a _tritone_.

Suppose we remove the diminished fifth from our collection of notes. Then, the next most dissonant note would seem to be the minor second, as it forms a dissonance with the tonic, but also a tritone relative to the perfect fifth.

Having removed the minor second, the minor sixth should be removed: It forms a tritone with the major second, but also a minor second with the perfect fifth.

We proceed similarly to remove the minor seventh, which forms a tritone with the major third and a minor second with the major sixth.

Finally, we remove the minor third, which forms a tritone with the major sixth and a minor second with the major third. 

We have finished removing all tritones, and are left with the following chart, which consists precisely of the notes of the major scale, _with the tonic preserved_:

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 8/15 | major seventh (inversion of minor second) |
| 3/4 | perfect fourth (inversion of perfect fifth) |
| 1/2 | octave |

### Half step removal

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

The mathematical origins seem to be motivated in a way similar to our discussion for the major scale. If we continued removing the most dissonant notes, we would first remove the major seventh, as it forms a minor second with our tonic. Then, we would remove the perfect fourth, as it forms a minor second with our perfect fifth (which we certainly are not going to remove):

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 1/2 | octave |
