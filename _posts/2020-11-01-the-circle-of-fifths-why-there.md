---
title: "The circle of fifths: Why there are twelve notes in Western music"
---

The short answer: Because

$$3^{12} = 531441 \approx 524288 = 2^{19}.$$

The wise(?) answer: Because musical semantics arises from carefully chosen _intervals_, not pitches.

The long answer:

### Consonance, or small integer ratios

The experience of sound is the detection of air waves, and different pitches correspond to different wavelengths - high pitches correspond to short wavelengths. The traditional physical explanation for consonance between two notes is that the ratio of their wavelengths is a ratio of small integers. For later reference, I list the best such ratios here:

$$\frac{1}{2}, \frac{1}{3}, \frac{1}{5}, \frac{1}{7}, \frac{3}{5}, \frac{3}{7}, \frac{5}{7}.$$

Here I have chosen fractions involving 1 and primes from 3 through 7. The lower the integers, the greater the consonance. I have also included 1/2 but omitted other pairings involving 2, due to _octave equivalence_, We discuss this next.

### Octave equivalence

The most consonant wavelength ratio of 1 to 2 corresponds to an octave interval; the notes sound "the same." The question of why such octave-separated pitches sound similar is an empirical question for neuroscientists and doesn't have a clean answer. For instance, studies have found that chimpanzees also experience octave equivalence. On the other hand, [other studies](https://www.quantamagazine.org/perceptions-of-musical-octaves-are-learned-not-wired-in-the-brain-20191030/) have discovered isolated human cultures which do not:

<div class="media">
<p>Computer analyses that compared the Tsimané participants with those in the United States found that both groups generally preserved the pitch intervals between the notes played to them — for example, maintaining the difference between a middle C and middle A...</p>

<p>A curious difference emerged, however, in how they sang the notes back. When the notes played were very high or low, U.S. participants accurately shifted the notes into an octave within their vocal range. The Tsimané didn’t. To them, it seemingly wasn’t clear what notes in their range best corresponded to the ones they heard. Their responses didn’t seem to reflect a perception of octave structure at all.</p>
</div>

### The circle of fifths

The next most consonant wavelength ratio of 1 to 3 essentially corresponds to a perfect fifth. As written, this interval is larger than an octave; an actual perfect fifth corresponds to lowering the higher note of the interval by an octave, for a 2 to 3 ratio. 

Perfect fifths are desirable as they are not equivalent to existing notes, and yet are very consonant. They are the most natural, deliberate way to select new musical pitches. As a result, we extend another perfect fifth down from our note of wavelength 3, resulting in a new note of wavelength 9/2. Repeating this process and allowing octave equivalences, we find ourselves having all notes with wavelengths of length

$$\frac{2^n}{3^m}.$$

We should restrict this process to wavelengths that are not too short or too long (too high pitched or low pitched, respectively). This corresponds to keeping the ratio $$n/m$$ bounded. However, without further restriction, we still have infinitely many notes, by choosing $$m$$ arbitrarily large but $$n$$ appropriately larger (we obtain arbitrarily many distinct wavelengths close to 1). We thus return to the short answer at the beginning of today's discussion: Every time we see $$3^{12}$$, we exchange it with $$2^{19}$$, which in turn is octave equivalent to 1. This ensures that we have exactly 12 notes corresponding, up to octave equivalence, to each $$3^{m}$$ with $$m$$ ranging from 0 to 11 - precisely the 12 notes of Western music.
