---
title: "Temperament: Compromising consonances"
---

Recall the list of small integer ratios from our [discussion of consonance]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of %}):

$$\frac{1}{2}; \frac{2}{3}, \frac{3}{4}; \frac{4}{5}; \frac{3}{5}.$$

There, we discussed the ratios 1/2 (octave equivalence) and 2/3 (the perfect fifth). The next most consonant ratio of 3/4 can be constructed from the perfect fifth by lowering the upper note by an octave to get a 4/3 wavelengh note (and then interchanging the roles of the notes to get 3/4). The procedure we just described is known as an _inversion_. The pianist will also recognize this as a perfect fourth.

The next most consonant wavelength ratio of 4/5 corresponds to a major third. This introduces the new prime 5, which cannot be constructed from factors of 2 and 3, so would be a natural candidate for a new note.

### Pythagorean tuning

However, it turns out that Western music does not introduce the wavelengths generated by major thirds as new notes, simply because there are already too many, with 12 notes generated by the perfect fifths alone. Instead, we approximate it using one of these existing notes:

$$\frac{4}{5} \approx \frac{2^6}{3^4}.$$

The note generation scheme outlined so far using the [circle of fifths]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of %}) is known as the _Pythagorean tuning_, with the hope that all other consonant intervals may be approximated by such ratios of 2 and 3. Unfortunately, these approximations, including the one above for the major third, cause noticeable distortions.

### Meantone temperament

_Temperament_ refers to any system which adjusts note wavelengths to compromise between consonant intervals. _Meantone temperament_, introduced in the 16th century, "redefines 3" into say, $$\tilde 3$$ so that

$$\frac{4}{5} = \frac{2^6}{\tilde 3^4}.$$

This means that major thirds sound exactly as they should. The perfect fifth is replaced by an approximation, but the error in $$\tilde 3$$ is essentially the fourth root of the error for the major third in Pythagorean tuning, which is acceptable.

Unfortunately, it turns out that the approximation 

$$1 \approx \frac{2^{19}}{\tilde 3^{12}}$$

closing the [circle of fifths]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of %}) is worse compared to Pythagorean tuning, and causes out-of-tune intervals known as _wolf intervals_.

### Equal temperament

Modern Western music uses _equal temperament_, a similar idea to meantone temperament except choosing to redefine 3 so that the circle of fifths closes:

$$1 = \frac{2^{19}}{\tilde 3^{12}}.$$

The error on $$\tilde 3$$ is essentially the twelvth root of the wolf interval error and is almost imperceptible. It turns out that the major third approximation is also improved.

A happy byproduct of using equal temperament is that it is harmless to change the root note, allowing for lossless modulation. The legend goes that Bach intended the WTC to be played on a keyboard tuned with equal temperament. Historians have since [invented a lot of other ideas](https://en.wikipedia.org/wiki/The_Well-Tempered_Clavier#Well-Tempered_tuning).
