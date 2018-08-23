# Basic mobile keyboard spell checker enhancements

This subproject is a minimal update to the existing keyboards for the Sámi languages, to be able to minimally support spell checking as part of the typing experience. It uses the existing codebase, and work done in earlier projects, with minimal additional work to integrate the spell checking functionality.

The main objective is to deliver spell checking for the Sámi languages fast. Further speller enhancements and support for any language is part of the [Advanced Spell checking for mobile keyboards](MobileSpell2.md) project.

# Deliverables

## Targeted features

* spell checking for the mobile keyboards (iOS and Android) using the [Rust hfst-ospell library](https://github.com/bbqsrc/hfst-ospell-rs)
* generate speller error model for nearby key hits based on keyboard layout
* speller files are included in the keyboard app at build time
* user interface and interaction should be close to that of Apple's and Google's, on each respective platform - that is what people are used to from the majority language keyboards; other UI solutions are not by definition ruled out, but need a thorough discussion and evaluation before implementation

## Supported languages

* North Sámi (sme)
* Lule Sámi (smj)
* South Sámi (sma)
* Inari Sámi (smn)

## Compatibility requirements

* iOS 9+
* Android 5+

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
