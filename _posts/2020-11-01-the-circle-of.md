---
title: "The circle of fifths: Why there are twelve notes in Western music"
---

The short answer: Because

$$3^{12} = 531441 \approx 524288 = 2^{19}.$$

The wise(?) answer: Because musical semantics arises from carefully chosen _intervals_, not pitches.

The long answer:

### Consonance, or small integer ratios

The experience of sound is the detection of air waves, and different pitches correspond to different wavelengths - high pitches correspond to short wavelengths. The traditional physical explanation for consonance between two notes is that the ratio of their wavelengths is a ratio of small integers. For later reference, I list the best such ratios here:

$$\frac{1}{2}; \frac{1}{3}, \frac{2}{3}, \frac{3}{4}; \frac{1}{5}, \frac{2}{5}, \frac{4}{5}; \frac{3}{5}.$$

How did I choose these ratios? I have grouped the ratios involving the prime 2 alone; the primes 2 and 3; the primes 2 and 5; and the primes 3 and 5. I have considered only ratios under 1 by taking reciprocals as necessary. I have sometimes allowed 4 in the groups where I have included 2, but this allowance is at some level redundant, due to _octave equivalence_, which we discuss next.

### Octave equivalence

The most consonant wavelength ratio of 1 to 2 corresponds to an octave interval; the notes in fact sound "the same." Due to octave equivalence, we may remove from our list the ratios less than 1/2. For instance, 1/3 is equivalent to 2/3; we are simply lowering the note by an octave:

$$\frac{1}{2}; \frac{2}{3}, \frac{3}{4}; \frac{4}{5}; \frac{3}{5}.$$

The question of why such octave-separated pitches sound similar is an empirical question for neuroscientists and doesn't have a clean answer. For instance, studies have found that chimpanzees also experience octave equivalence. On the other hand, [other studies](https://www.quantamagazine.org/perceptions-of-musical-octaves-are-learned-not-wired-in-the-brain-20191030/) have discovered isolated human cultures which do not:

<div class="media">
<p>Computer analyses that compared the Tsimané participants with those in the United States found that both groups generally preserved the pitch intervals between the notes played to them — for example, maintaining the difference between a middle C and middle A...</p>

<p>A curious difference emerged, however, in how they sang the notes back. When the notes played were very high or low, U.S. participants accurately shifted the notes into an octave within their vocal range. The Tsimané didn’t. To them, it seemingly wasn’t clear what notes in their range best corresponded to the ones they heard. Their responses didn’t seem to reflect a perception of octave structure at all.</p>
</div>


### The circle of fifths

The next most consonant wavelength ratio of 2/3 corresponds to a perfect fifth. Perfect fifths are desirable as they are not equivalent to existing notes, and yet are very consonant. They are the most natural, deliberate way to select new musical notes. As a result, we extend another perfect fifth up from our note of wavelength 2/3, resulting in a new note of wavelength 4/9. Repeating this process and lowering by octave equivalences as necessary, we find ourselves having all notes with wavelengths of length

$$\frac{2^n}{3^m}.$$

We should restrict this process to wavelengths that are not too short or too long (too high pitched or low pitched, respectively). This corresponds to keeping the ratio $$n/m$$ bounded. However, without further restriction, we still have infinitely many notes, by choosing $$m$$ arbitrarily large but $$n$$ appropriately larger (we obtain arbitrarily many distinct wavelengths close to 1). 

We thus return to the short answer at the beginning of today's discussion: Every time we see $$3^{12}$$, we exchange it with $$2^{19}$$, which in turn is octave equivalent to 1. This ensures that we have exactly 12 notes corresponding, up to octave equivalence, to each $$3^{m}$$ with $$m$$ ranging from 0 to 11 - precisely the 12 notes of Western music.
