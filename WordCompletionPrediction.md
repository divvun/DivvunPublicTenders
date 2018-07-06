
# Word completion and prediction for the Giella mobile keyboards

* target platforms: iOS and Android
* possibly in cooperation with the Hfst team at Helsinki University and/or a development team in Canada, organised through AltLab at the University of Alberta

# Deliverables

## Word completion

* some sort of lemma, morphology and word form frequency weighting
* fst-based, essentially adding a star to the end of the string typed so far, and suggesting the best match in the fst
* possibly combined with a trigram model looking at the two previous words (can only be done on iOS as long as we cache the input — there is no way to access the text buffer beyond the present word)

Alternatively, one can train a neural network on existing corpus data (word forms), where each word is split in individual letters, and the neural network then predicts the most likely continuation given the input so far.

Whatever technology is chosen, the task is to integrate that technology with the existing mobile speller code, to make sure that everything works on the technical side. The linguistic side of things is fully the responsibility of the Divvun group.

## Word prediction

Probably something along the following lines:

* trigram model of word forms
* trigram model of lemma / POS / inflections

Or a neural network, using e.g. [OpenNMT](http://opennmt.net/), trained on relevant material. See also the text above regarding word completion.

## Trigger

The word completion should be automatically applied when the user taps the space key.

## Compatibility requirements

* iOS 9+
* Android 5+

## Acceptance requirements

Before delivery of final version:

* user documentation
* passing all defined tests
* all code in Github
