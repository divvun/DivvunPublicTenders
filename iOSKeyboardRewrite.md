# iOS Keyboard rewrite

The present iOS Keyboard code is based on [Tasty Imitation Keyboard](https://github.com/divvun/tasty-imitation-keyboard). It served as a good starting point, but the code has turned out to be hard to maintain and develop further. This sub-project aims to replace that codebase with a complete rewrite.

This sub-project should be run after the [mobile keyboard speller](MobileSpell.md) sub-project. It is important to get the mobile keyboard spellers out as soon as possible using the present codebase, thus the rewrite must happen thereafter.

# Deliverables

## Targeted features

* functionally the same as the code at the end of the [mobile keyboard speller](MobileSpell.md) subproject:
    * basic typing functionality supporting all languages and writing systems already supported
    * basic speller functionality
* the top banner (aka the «suggestion field») should be a plug-in banner, where additional functionality can be provided by different keyboard plugins, such as word completion and next-word prediction
* the keyboard drawing code should be clean and easy to maintain and enhance
* the new codebase should be written so that it is easy to add new functionality and new properties to the keyboard app
* it should include a first-time startup guide
* it should use the Páhkat package management to install and update additional functionality for languages selected by the user
* functionally and graphically it should as closely as possible resemble Apple’s keyboards for everything that is not our own additional functionality or a plugin functionality
* keyboard layout should adapt to portrait or landscape orientation of iPads, similar to what Apple keyboards do

## Compatibility requirements

* iOS 10+

## Acceptance requirements

Before delivery of final version:

* technical documentation
* passing all defined tests
* all code in Github
