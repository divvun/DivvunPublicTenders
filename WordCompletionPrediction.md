# Word completion and prediction for the Giella mobile keyboards

The Divvun group wants to develop further our mobile keyboards, adding word completion and word prediction on top of other functionality. This project should possibly be done in cooperation with the Hfst team at Helsinki University and/or a development team in Canada, organised through AltLab at the University of Alberta. The project depends on [Advanced Spell checking for mobile keyboards](MobileSpell2.md) being completed and delivered.

# Deliverables

## Word completion

* some sort of lemma, morphology and word form frequency weighting
* fst-based, essentially adding a star to the end of the string typed so far, and suggesting the best match in the fst
* possibly combined with a trigram model looking at the two previous words (can only be done on iOS as long as we cache the input — there is no way to access the text buffer beyond the present word)

Alternatively, one can train a neural network on existing corpus data (word forms), where each word is split in individual letters, and the neural network then predicts the most likely continuation given the input so far.

Whatever technology is chosen, the task is to integrate that technology with the existing mobile speller code, to make sure that everything works on the technical side. The linguistic side of things is fully the responsibility of the Divvun group.

Appearance and behaviour should be as close to the standard OS keyboard for majority languages as possible.

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

[Standard requirements](GeneralInfo.md).
