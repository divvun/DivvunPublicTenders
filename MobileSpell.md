# Mobile keyboard spell checker enhancements

# Deliverables

## Targeted features

* spell checking for the mobile keyboards (iOS and Android) using the [Rust hfst-ospell library](https://github.com/bbqsrc/hfst-ospell-rs)
* speller files updated via a Páhkat repository
* generate speller error model for nearby key hits based on keyboard layout
* automatically maintained user dictionary:
    * unknowns not corrected into a candidate list
    * unknowns left uncorrected a second time stored in user dictionary, and suggested prior to anything else for similar input
    * user dictionary should be visible and editable in dictionary app, including option to upload to Divvun for inclusion of new words (that would also require storing one word before and after, or the two preceding words, to give a minimum of context for the use of the word - this can also help us build a trigram of word usage for word prediction)

## Compatibility requirements

* iOS 8+
* Android 5+

## Acceptance requirements

Before delivery of final version:

* user documentation
* passing all defined tests
* all code in Github

# Tender

## Tender requirements

* solid Rust programming experience
* solid iOS programming experience
* solid Android programming experience

**solid** = reference to at least five independent projects involving the language or platform in question.

## Subproject selection criteria

* experience with similar work
