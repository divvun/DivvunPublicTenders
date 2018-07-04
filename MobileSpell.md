# Basic mobile keyboard spell checker enhancements

This subproject is a minimal update to the existing keyboards for the Sámi languages, to be able to minimally support spell checking as part of the typing experience. It uses the existing codebase, and work done in earlier projects, with minimal additional work to integrate the spell checking functionality.

The main objective is to deliver spell checking for the Sámi languages fast. Further speller enhancements and support for any language is part of a [separate project](MobileSpell2.md).

# Deliverables

## Targeted features

* spell checking for the mobile keyboards (iOS and Android) using the [Rust hfst-ospell library](https://github.com/bbqsrc/hfst-ospell-rs)
* generate speller error model for nearby key hits based on keyboard layout
* speller files are included in the keyboard app at build time
* automatically maintained user dictionary:
    * unknowns not corrected into a candidate list
    * unknowns left uncorrected a second time stored in user dictionary, and suggested prior to anything else for similar input


## Supported languages

* North Sámi (sme)
* Lule Sámi (smj)
* South Sámi (sma)
* Inari Sámi (smn)

## Compatibility requirements

* iOS 9+
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
