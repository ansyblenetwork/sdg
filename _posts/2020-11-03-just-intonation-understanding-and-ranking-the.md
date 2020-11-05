---
title: "Just intonation: Understanding and ranking the intervals by consonance"
---

Previously, we discussed why there are at least [twelve notes]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of-fifths-why-there %}) in Western music, and why they [suffice]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}). In a nutshell, the selection of twelve notes prioritizes the ability to play perfect fifths, and the choice of temperament compromises this with the ability to play other consonant intervals.

In today's post we look for such consonances approximated by these 12 notes. It is clear that not all 12 intervals are consonant: This corresponds with the fact that slamming a piano with random notes does not sound good, and why despite all of the combinatorial possibilities, simultaneous notes in classical music almost always stem from canonical chords and triads.

### Tempering the intervals

Recall that we have 12 notes corresponding to the following wavelengths, derived from successive extension by perfect fifths:

$$\frac{1}{3}, \frac{1}{3^2}, \frac{1}{3^3}, \frac{1}{3^4}, \frac{1}{3^5}, \frac{1}{3^6}, \frac{1}{3^7}, \frac{1}{3^8}, \frac{1}{3^9}, \frac{1}{3^{10}}, \frac{1}{3^{11}}, \frac{1}{3^{12}}$$

We perform successive simplifications:

1) These notes actually have extremely small wavelengths, far over an octave above the root note of wavelength 1. We can exchange them for their octave equivalents with wavelength between 1/2 and 1 - within an octave above the root note:

$$\frac{2}{3}, \frac{2^3}{3^2}, \frac{2^4}{3^3}, \frac{2^6}{3^4}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{2^{12}}{3^8}, \frac{2^{14}}{3^9}, \frac{2^{15}}{3^{10}}, \frac{2^{17}}{3^{11}}, \frac{2^{19}}{3^{12}}.$$

2) Recall the approximations for the major third and closing the circle of fifths:

$$\frac{4}{5} \approx \frac{2^6}{3^4}, \qquad 1 \approx \frac{2^{19}}{3^{12}}.$$

We implement these approximations in our list of notes:

$$\frac{2}{3}, \frac{8}{9}, \frac{2^4}{3^3}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{16}{25}, \frac{3^3}{2^5}, \frac{9}{16}, \frac{3}{4}, 1.$$

3) Recall our list of small integer ratios:

$$\frac{1}{2}; \frac{2}{3}, \frac{3}{4}; \frac{4}{5}; \frac{3}{5}.$$

The remaining ratio, 3/5, has the approximation

$$\frac{3}{5} \approx \frac{2^4}{3^3}.$$

We implement this and its inversion:

$$\frac{2}{3}, \frac{8}{9}, \frac{3}{5}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{16}{25}, \frac{5}{6}, \frac{9}{16}, \frac{3}{4}, 1.$$
