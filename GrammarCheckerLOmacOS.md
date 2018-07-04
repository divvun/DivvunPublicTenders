# Grammar Checker integration with LibreOffice and macOS

## Introduction

This subproject contains two parts:

1. LibreOffice integration
2. macOS integration

### LibreOffice integration

There is already working code for grammar checkers in LibreOffice, using [libdivvun](https://github.com/divvun/libdivvun) at its core, using [code](https://github.com/divvun/libreoffice-divvun) forked from [libvoikko](https://github.com/voikko/corevoikko) as a wrapper around it. However, this code assumes that the library and the linguistic components are all built into one big [oxt file](https://wiki.openoffice.org/wiki/Documentation/DevGuide/Extensions/File_Format), which means more work and heavier downloads for updates, and a lot of duplicate binaries when installing multiple languages.

The aim of this part of the subproject is to make the language independent code and the linguistic components into separate packages, and make them both installable and update-able through a Páhkat repository. At the same time this will make the grammar checker library code be installed only once, and used by all grammar checker languages.

This should come in addition to the present solution with one monolithic package for each language.

### macOS integration

MacOS has a [grammar checker API](https://developer.apple.com/documentation/foundation/nsspellserverdelegate) as part of the spelling api. This part of the subproject should integrate the grammar checker with the macOS API for grammar checking.

There is no default graphical user interface in macOS for configuring the grammar checker. Instead a grammar checker configuration tool has to be built, either as part of the Páhkat GUI client, or as a separate tool. The configuration is stored in a file that is read and used by the grammar checker library, and it should be re-read whenever the grammar checker library detects that it has been changed.

### Common features for LibreOffice and macOS integration

Only the general grammar checker library is specific to each host environment (aka API). The linguistic support files are the same, and should be shared. All three components should be installed and automatically updated through a Páhkat repository:

* macOS version of the grammar checker library
* LibreOffice version of the grammar checker library
* linguistic support files for each language the user wants

# Deliverables

## Targeted features

* grammar checking for LibreOffice (macOS and Windows)
* grammar checking for macOS systemwide
* all binary files and linguistic support files downloaded, installed and updated using the Páhkat package manager
* linguistic support files installed in a shared location (on macOS)
* configuration tool for the macOS system-wide grammar checker

## Supported languages

Any language that can be identified with a [BCP47](https://tools.ietf.org/html/bcp47) code.

## Compatibility requirements

* macOS 10.8+
* Windows 7+ (LibreOffice integration only)

## Acceptance requirements

Before delivery of final version:

* user documentation
* technical documentation
* passing all defined tests
* all code in Github

# Tender

## Tender requirements

* solid C/C++ programming experience
* solid Python programming experience
* solid macOS programming experience
* solid Windows programming experience

**solid** = reference to at least five independent projects involving the language or platform in question.

## Subproject selection criteria

* experience with similar work
