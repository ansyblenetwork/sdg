---
title: "Just intonation: Understanding and ordering the intervals by consonance"
---

Previously, we discussed why there are at least [twelve notes]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of-fifths-why-there %}) in Western music, and why they [suffice]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}). In a nutshell, the selection of twelve notes prioritizes the ability to play perfect fifths, and the choice of temperament compromises this with the ability to play other consonant intervals.

In today's post we look for such consonances approximated by these 12 notes. It is clear that not all 12 intervals are consonant: This corresponds with the fact that slamming a piano with random notes does not sound good, and why despite all of the combinatorial possibilities, simultaneous notes in classical music almost always stem from canonical chords and triads.

### Justifying the intervals

Recall that we have 12 notes corresponding to the following wavelengths, derived from successive extension by perfect fifths:

$$\frac{2}{3}, \frac{2^3}{3^2}, \frac{2^4}{3^3}, \frac{2^6}{3^4}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{2^{12}}{3^8}, \frac{2^{14}}{3^9}, \frac{2^{15}}{3^{10}}, \frac{2^{17}}{3^{11}}, \frac{2^{19}}{3^{12}}.$$

Here, by choosing the numerators to be appropriate powers of 2, we have used the octave equivalents with wavelength between 1/2 and 1, lying within an octave above the root note. We perform successive approximations which justify the intervals (pun intended...?):

1) Recall the approximations for the major third and closing the circle of fifths, respectively:

$$\frac{4}{5} \approx \frac{2^6}{3^4}, \qquad 1 \approx \frac{2^{19}}{3^{12}}.$$

We implement these approximations in our list of notes, keeping in mind this also provides approximations for inversions:

$$\frac{2}{3}, \frac{8}{9}, \frac{2^4}{3^3}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{5}{8}, \frac{3^3}{2^5}, \frac{9}{16}, \frac{3}{4}, 1.$$

2) Recall the last element of our list of [small integer ratios]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of-fifths-why-there %}), 3/5. This corresponds to a major sixth and has the approximation

$$\frac{3}{5} \approx \frac{2^4}{3^3}.$$

We implement this and its inversion:

$$\frac{2}{3}, \frac{8}{9}, \frac{3}{5}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{5}{8}, \frac{5}{6}, \frac{9}{16}, \frac{3}{4}, 1.$$

3) The remaining intervals may be viewed as dissonant, since they do not come naturally from our list of small integer ratios. Still, we may mildly temper them with the approximations

$$\frac{8}{15} \approx \frac{2^7}{3^5},$$

where the ratio 8/15 corresponds to a major seventh. Implementing this and its inversion, we have

$$\frac{2}{3}, \frac{8}{9}, \frac{3}{5}, \frac{4}{5}, \frac{8}{15}, \frac{32}{45}, \frac{15}{16}, \frac{5}{8}, \frac{5}{6}, \frac{9}{16}, \frac{3}{4}, 1.$$

### Ordering by consonance

We list our final set of wavelengths, which are the wavelengths used in _just intonation_:

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
| 1/1 | octave |

In modern music, these wavelengths are only approximate due to [equal temperament]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}), but this analysis explains why and how we can order the intervals by consonance:

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 4/5 | major third (inversion of minor sixth) |
| 3/5 | major sixth (inversion of minor third) |
| 8/9 | major second (inversion of minor seventh) |
| 8/15 | major seventh (inversion of minor second) |
| 32/45 | diminished fifth (inversion of itself) |

The first row consists of the perfect consonances, the next three consist of imperfect consonances, and the last two consist of dissonances. 

<div id="paper" class="sheetmusic"></div>
<div id="controller" style="position:relative; width:calc(100% + 360px + 35px); left:calc(-180px - 17.5px); padding-left:calc(360px + 35px);"></div>

					
<script>
// NOTE: If you want just the sound without showing the music, use "*" instead of "paper" in the renderAbc call.
	var test = "X:1\nK:C\nQ:1/4=60\nCG[CG]2|CE[CE]2|CA[CA]2|CD[CD]2|CB[CB]2|C_G[C_G]2|\n";
	
var visualObj = ABCJS.renderAbc("paper", test, { add_classes: true, clickListener: self.clickListener })[0];

	var synthControl = new ABCJS.synth.SynthController();
	synthControl.load("#controller", cursorControl, 
		{
		    displayLoop: true, 
		    displayRestart: true, 
		    displayPlay: true, 
		    displayProgress: true, 
		    displayWarp: true
		}
	);

    if (ABCJS.synth.supportsAudio()) {    
	var midiBuffer = new ABCJS.synth.CreateSynth();
        window.AudioContext = window.AudioContext || window.webkitAudioContext || navigator.mozAudioContext || navigator.msAudioContext;
        var audioContext = new window.AudioContext();
        audioContext.resume().then(function () {
            // In theory the AC shouldn't start suspended because it is being initialized in a click handler, but iOS seems to anyway.

            // midiBuffer.init preloads and caches all the notes needed. There may be significant network traffic here.
            return midiBuffer.init({
                visualObj: visualObj,
                audioContext: audioContext,
                millisecondsPerMeasure: visualObj.millisecondsPerMeasure(),
                options: {
			soundFontUrl: '',
                    onEnded: function() {console.log("hi");}
                }
            }).then(function (response) {
	    
                synthControl.setTune(visualObj, false, { options:{ qpm: 2*visualObj.getBpm()} }).then(function () {
                    console.log("Audio successfully loaded.")
		    
			let tempos = document.querySelectorAll(".abcjs-midi-tempo");
			for (let i = 0; i < tempos.length; i++) {
				tempos[i].value = 99;
				tempos[i].value = 100;
			}

                }).catch(function (error) {  console.warn("Audio problem:", error);  });

                // midiBuffer.prime actually builds the output buffer.
                return midiBuffer.prime();
            }).then(function () {
                // At this point, everything slow has happened. midiBuffer.start will return very quickly and will start playing very quickly without lag.
                return Promise.resolve();
            }).catch(function (error) { console.warn("synth error", error);  });
        });
    }

</script>

<style>
    svg .abcjs-tempo {
	display:none;
    }
<style>
