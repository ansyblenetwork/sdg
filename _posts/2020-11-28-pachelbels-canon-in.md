---
title: "Pachelbel's Canon in species counterpoint"
---


<div id="score"></div>
<script>
makeInteractive("score", `
%%staves{1 2 3 4}
Q:1/4=60
M:4/4
L:1/8
K:D
V:1
GG' F'F EB EE'|F'F EE' D'D CC' | BB' A'A G3/2E'/2 AA | A2 z2z4|]
V:2 
D'3 D' D'2 C'2 | D'D CC' BB, A,A| GG' F'F EB EE'|A2 z2z4 |]
V:3
B'2 D''A'B'2 A'2 | A'2 A>G F2 F'>E'|D'3 D' D'2 C'2|D'2 z2 z4|]
V:4 clef=bass
G,,2 D,,2 G,,2 A,,2 | D,2 A,,2 B,,2 F,,2 |G,,2 D,,2 G,,2 A,,2 | D,2 z2 z4 |]
`);
</script>
