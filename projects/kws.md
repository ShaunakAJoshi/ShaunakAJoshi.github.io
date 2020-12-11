---
layout: post
title: Keyword Spotting
permalink: /projects/kws/
---

Keyword Spotting (KWS) refers to the task of detecting a pre-defind keyword/phrase in an audio file or a stream of audio.

Say you have an audio lecture file and you'd like to jump right to the part where the professor discusses a particular topic. You could use KWS by recording an utterance of the word you'd like to search for and that's it! You'll get a list of all the time instances where the word was uttered! (an empty list if it didn't find any)

But KWS is more-widely used for trigger word detection. All Android users can trigger the Google Assistant by uttering the phrase 'Hey Google' while iPhone users can wake up Siri by simply saying 'Hey Siri'. In such cases, KWS should be computationally and power efficient since the microphone of our phone is always on and listening! KWS should be robust enough to ignore a variety of background noises, non-keyword speech, etc. while also remaining vigilant enough to detect our pre-defined keyword!

I implemented a sliding DTW approach and tested it on the Google Speech Commands dataset. Two different approaches have been used for feature extraction:

* MFCC features
* Neural Network feature extractor, trained for predicting phones on the TIMIT dataset

You can go through the [presentation]({{site.url}}/assets/pdf/kws.pdf) for a complete explanation while the code can be found [here](https://github.com/methi1999/KWS).
