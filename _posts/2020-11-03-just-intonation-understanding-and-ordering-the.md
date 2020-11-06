---
title: "Just intonation: Understanding and ordering the intervals by consonance"
---

Previously, we discussed why there are at least [twelve notes]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of-fifths-why-there %}) in Western music, and why they [suffice]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}). In a nutshell, the selection of twelve notes prioritizes the ability to play perfect fifths, and the choice of temperament compromises this with the ability to play other consonant intervals.

In today's post we look for such consonances approximated by these 12 notes. It is clear that not all 12 intervals are consonant: This corresponds with the fact that slamming a piano with random notes does not sound good, and why despite all of the combinatorial possibilities, simultaneous notes in classical music almost always stem from canonical chords and triads.

### Justifying the intervals

Recall that we have 12 notes corresponding to the following wavelengths, derived from successive extension by perfect fifths:

$$\frac{2}{3}, \frac{2^3}{3^2}, \frac{2^4}{3^3}, \frac{2^6}{3^4}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{2^{12}}{3^8}, \frac{2^{14}}{3^9}, \frac{2^{15}}{3^{10}}, \frac{2^{17}}{3^{11}}, \frac{2^{19}}{3^{12}}.$$

Here, we have used the octave equivalents with wavelength between 1/2 and 1 - within an octave above the root note. We perform successive approximations which justify the intervals (pun intended...?):

1) Recall the approximations for the major third and closing the circle of fifths:

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

<div id="paper"></div>
<p id="suspend-explanation">Browsers require a button:</p>
<button id="activate-audio">Activate Audio Context And Play</button>
<button id="stop-audio" style="display:none;">Stop Audio</button>
<div id='audio-error' style="display:none;">Audio is not supported in this browser.</div>

<script>
    load();
function load() {
    // First draw the music - this supplies an object that has a lot of information about how to create the synth.
    // NOTE: If you want just the sound without showing the music, use "*" instead of "paper" in the renderAbc call.
    var visualObj = ABCJS.renderAbc("paper", "X:1\nK:D\nDDAA|BBA2|\n", {
        responsive: "resize" })[0];

    // This object is the class that will contain the buffer
    var midiBuffer;

    var startAudioButton = D("activate-audio");
    var stopAudioButton = D("stop-audio");
    var explanationDiv = D("suspend-explanation");
    var audioError = D("audio-error");

    startAudioButton.addEventListener("click", function() {
        startAudioButton.setAttribute("style", "display:none;");
        explanationDiv.setAttribute("style", "display:none;");
        if (ABCJS.synth.supportsAudio()) {
            stopAudioButton.setAttribute("style", "");

            // An audio context is needed - this can be passed in for two reasons:
            // 1) So that you can share this audio context with other elements on your page.
            // 2) So that you can create it during a user interaction so that the browser doesn't block the sound.
            // Setting this is optional - if you don't set an audioContext, then abcjs will create one.
            window.AudioContext = window.AudioContext ||
                window.webkitAudioContext ||
                navigator.mozAudioContext ||
                navigator.msAudioContext;
            var audioContext = new window.AudioContext();
            audioContext.resume().then(function () {
                // In theory the AC shouldn't start suspended because it is being initialized in a click handler, but iOS seems to anyway.

                // This does a bare minimum so this object could be created in advance, or whenever convenient.
                midiBuffer = new ABCJS.synth.CreateSynth();

                // midiBuffer.init preloads and caches all the notes needed. There may be significant network traffic here.
                return midiBuffer.init({
                    visualObj: visualObj,
                    audioContext: audioContext,
                    millisecondsPerMeasure: visualObj.millisecondsPerMeasure()
                }).then(function (response) {
                    // console.log(response); // this contains the list of notes that were loaded.
                    // midiBuffer.prime actually builds the output buffer.
                    return midiBuffer.prime();
                }).then(function () {
                    // At this point, everything slow has happened. midiBuffer.start will return very quickly and will start playing very quickly without lag.
                    midiBuffer.start();
                    return Promise.resolve();
                }).catch(function (error) {
                    if (error.status === "NotSupported") {
                        stopAudioButton.setAttribute("style", "display:none;");
                        audioError.setAttribute("style", "");
                    } else console.warn("synth error", error);
                });
            });
        } else {
            audioError.setAttribute("style", "");
        }
    });

    stopAudioButton.addEventListener("click", function() {
        startAudioButton.setAttribute("style", "");
        explanationDiv.setAttribute("style", "");
        stopAudioButton.setAttribute("style", "display:none;");
        if (midiBuffer) midiBuffer.stop();
    });
}
</script>
