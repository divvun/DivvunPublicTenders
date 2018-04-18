# Grammar Checker integration with MS Office and Google apps

This subproject should take our grammar checker library and turn it into a functional grammar checker tool for MS Office and Google apps users, resembling the standard MS Office grammar checker as much as possible.

## Architecture

The following is a schematic view of the main components of the grammar checker:

![Schematic view of the main components of the grammar checker](bilete/GramCheckArch.png "Schematic view of the main components of the grammar checker")

## Front-end / grammar checker plugin

The front-end code should be based on the
[GrammarSoft frontend code](https://github.com/GrammarSoft/proofing-gasmso), but reworked so that it can also run offline, primarily when used with MS Office. More specifically, it needs to:

* download all required libraries and components from the server and store them locally in a cache, and use them locally
* when there is a network connection, the front-end should check with the back-end server for new versions, and if found, download and install the newer version
* it should also be possible to run the grammar checker completely server-based, in cases where it is not possible to store files locally, or running the grammar checker locally turns out to be too heavy on the platform according to some test
    * running completely server-based is the default (and possibly only) mode when used with Google apps, as the Google apps are only usable when there is a network connection; it still may be useful to run the grammar checker offline along the same line as for the MS Office integration, as that could possibly speed up the grammar checker - the exact behavior needs to be determined at a later point, when speed and other considerations can be tested properly
* the front-end must query the central server back-end while downloading support files, so that end users don't have to wait for the download to finish before starting the grammar checker

Functional requirements:

* send and receive a paragraph of text to the locally cached back-end (or over the net to the server, when required as described above), and receive a list of errors such that they can be marked in the source text or highlighted in the grammar checker user interface
* present correction suggestions containing the following:
    * short error title
    * one or more correction suggestions
    * a short description of the error(s)
    * based on user action, also a long description of the error
* it must be possible to turn on or off checking of specific grammar errors (the list of available errors is given by the backend)
    * it should be possible to define one's own collection of grammar errors to detect
    * cf. also the [Swedish grammar checker in MS Word](Spesifikasjon.md)
* if at all possible:
    * green/blue underlining
    * right-click on errors should give a context menu with correction suggestions and short error title
* the User Interface must still contain a clear and visible graphic element that unambiguously identifies the tool as comming from the Divvun group, not MS
* to the extent possible by MS and Google's API's, the grammar checker should work in all office applications
* it must be easy to identify the language of the text
* it should be possible to set the language of the text to the grammar checker language, even in cases where the language is not previously known to the host app (using BCP-47 locale codes)
* the grammar checker should only check text in the language(s) of the grammar checker
* it should be possible to run grammar checkers for several languages at the same time - the library and the code is the same, only the linguistic files differ
* the front-end must query the back-end for supported languages
* on supported platforms, the grammar checker should detect language switches to and from supported languages, e.g. when the user switches keyboard language
* all code must be Unicode safe, with support for all of it, not only the BMP

See a separate document with screen shots and [UI examples](Spesifikasjon.md) for what a possible implementation could look like.

### Targeted platforms/Office versions

* MS Office for Mac
* MS Office for Windows
* MS Office on iPad
* MS Office Online
* Google Apps

## Server back-end

The server backend should be based on existing backends, and the communication between server and front-end should be similar to already working solutions, based on the existing GrammarSoft code, but with an eye on the implementations already in use by the Divvun group.

The server backend must be a wrapper around [libdivvun](https://github.com/divvun/libdivvun) compiled as a grammar checker library. The server must:

* support uploading of libraries and support files so that the plugin can run off-line
* support version checking of libraries and support files, to facilitate uploading of new versions compared to what is already on the client

The interface should also follow whatever the REST/GraphQL subproject settles on.

## Requirements

* solid C++ programming experience
* solid JavaScript and NodeJS or similar experience
* solid macOS programming experience
* solid Windows programming experience

**solid** = reference to at least five independent projects involving the programming language or platform in question.

## Subproject selection criteria

* experience with similar work — XXX
* experience with language technology projects
* realistic and sound project plan — XXX

## Acceptance requirements

Before delivery of final version:

* user documentation
* passing all defined tests, on both Windows and macOS
* all code in Github
* code must be language independent
* MS Office integration must work with all language codes, including such codes that are not known to MS Office
* all functionality of libdivvun compiled as a grammar checker must be available via a user friendly and functional User Interface
* the code must follow established styles and linters for the programming language in question
* the code must pass code review by the Divvun group
* the grammar checker must function according to specifications
