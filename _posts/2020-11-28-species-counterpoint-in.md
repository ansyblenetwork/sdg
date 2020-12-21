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
C: Pachelbel
Q:1/2=100       % tempo
M:C|            % time signature
L:1/8           % default note length
K:D major       % key signature
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%staves {(R1 R2) (L1 L2)}
V:R1 clef=treble
V:L1 clef=bass
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
[V:R1] x8      |x8      |x8       |x8          |x8           |x8          |x8         | x8 | 
[V:R2] d8      |c8      |b,8       |a,8          |g,8          |f,8         |g,8      |e,8    |
[V:L1] x8      |x8      |x8       |x8          |x8           |x8         |x8           | x8 |
[V:L2] d,,8    |a,,,8   |b,,,8    |f,,,8       |g,,,8       |d,,,8       |g,,,8   |a,,,8 |
%
[V:R1] x8      |x8      |x8          |x8          |x8           |x8           |x8        | x8 | x8 |]
[V:R2] f8      |e8      |d8          |c8          |b,8           |a,8         | b,8 |    c8 | d8 |]
[V:L1] x8      |x8      |x8          |x8          |x8           |x8           |x8         | x8 | x8 |]
[V:L2] d,,8      |a,,,8      |b,,,8    |f,,,8       |g,,,8       |d,,,8       |g,,,8   |e,,8 |d,,8 |]
%	
`, 73);
</script>

Does this deviate at all from first species counterpoint? Other than the last f of the ostinato into an e, not really. There is a large number of octaves, but they are always separated by imperfect consonances (thirds or sixths) except at the last two measures of the first 8 bar phrase, where an octave is followed by a perfect fifth.


### Second species

Next, we have the second variation:


<div id="score2"></div>
<script>
makeInteractive("score2", `

T: Second Species Canon
C: Pachelbel
Q:1/2=100       % tempo
M:C|            % time signature
L:1/8           % default note length
K:D major       % key signature
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%staves {(R1 R2) (L1 L2)}
V:R1 clef=treble
V:L1 clef=bass
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
[V:R1] x8      |x8      |x8       |x8          |x8           |x8         | x8     | x8    |
[V:R2] d,4 f,4 |a,4 g,4 |f,4 d,4  |f,4  e,4    |d,4 b,,4    |d,4 a,4     |g,4 b,4 |a,4 g,4 |
[V:L1] x8      |x8      |x8       |x8          |x8           |x8         | x8     | x8    |  
[V:L2] d,,8    |a,,,8   |b,,,8    |f,,,8       |g,,,8       |d,,,8       |g,,,8   |a,,,8   |
%
[V:R1] x8      |x8      |x8          |x8          |x8          |x8         | x8     | x8     | x8  |]
[V:R2] f,4 d,4 |e,4 c4  |d4 f4       |a4 a,4      |b,4  g,4    |a,4 f,4    | d,4 d4 | d6 c2  | d8  |]
[V:L1] x8      |x8      |x8          |x8          |x8          |x8         | x8     | x8     |x8   |]
[V:L2] d,,8    |a,,,8   |b,,,8       |f,,,8       |g,,,8       |d,,,8      |g,,,8   |e,,8    |d,,8 |]
%	
`, 73);
</script>

The second variation breaks from second species a bit more, with the triple of octaives in measures 6, 7, and 8. Otherwise, it is a pretty good second species counterpoint as well.
