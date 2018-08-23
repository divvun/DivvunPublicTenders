# Advanced Spell checking for mobile keyboards

This subproject builds on the work done for [basic speller support](MobileSpell.md) in mobile keyboards, but depends on the [iOS keyboard rewrite](iOSKeyboardRewrite.md). The goal is to deliver a more advanced speller, with universal language support, and automatic download and updates of speller dictionaries.

# Deliverables

## Targeted features

* speller files updated via a Páhkat repository; no speller files are included at build time
* automatically maintained user dictionary:
    * unknowns not corrected into a candidate list
    * unknowns left uncorrected a second time stored in user dictionary, and suggested prior to anything else for similar input
    * user dictionary should be visible and editable in dictionary app, including option to upload to Divvun for inclusion of new words (that would also require storing one word before and after, or the two preceding words, to give a minimum of context for the use of the word - this can also help us build a trigram of word usage for word prediction)

## Supported languages

Any language that can be identified with a [BCP47](https://tools.ietf.org/html/bcp47) code.

## Compatibility requirements

* iOS 9+
* Android 5+

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
