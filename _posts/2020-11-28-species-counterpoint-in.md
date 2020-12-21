---
title: "Species counterpoint in Pachelbel's Canon"
---

[Open music theory](http://openmusictheory.com/firstSpecies.html) is already an excellent resource on species counterpoint, so I thought that instead of reproducing a post on it, I would analyze Pachelbel's Canon from the point of view of species counterpoint.

### First species

The first variation of the Canon is essentially already in species counterpoint. Swapping the two four-measure phrases, we have:

<div id="score"></div>
<script>
makeInteractive("score", `
T: First Species Canon
C: J. S. Bach
Q:1/2=100       % tempo
M:C|            % time signature
L:1/8           % default note length
K:D major       % key signature
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%staves {(R1 R2) (L1 L2)}
V:R1 clef=treble
V:L1 clef=bass
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
[V:R1] x8      |x8      |x8       |x8          |x8           |x8                   | x8 | 
[V:R2] d8      |c8      |b,8       |a,8          |g,8          |f,8         |g,8      |e,8    |
[V:L1] x8      |x8      |x8       |x8          |x8           |x8                    | x8 |
[V:L2] d,,8    |a,,,8   |b,,,8    |f,,,8       |g,,,8       |d,,,8       |g,,,8   |a,,,8 |
%
[V:R1] x8      |x8      |x8          |x8          |x8           |x8                    | x8 | x8 |]
[V:R2] f8      |e8      |d8          |c8          |b,8           |a,8         | b,8 |    c8 | d8 |]
[V:L1] x8      |x8      |x8          |x8          |x8           |x8                    | x8 | x8 |]
[V:L2] d,,8      |a,,,8      |b,,,8    |f,,,8       |g,,,8       |d,,,8       |g,,,8   |e,,8 |d,,8 |]
%	
`, 73);
</script>

Does this deviate at all from first species counterpoint? Other than the last f of the ostinato into an e, not really.
