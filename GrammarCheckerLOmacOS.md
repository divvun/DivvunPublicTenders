# Grammar Checker integration with LibreOffice and macOS

## Introduction

This subproject contains two, possibly three parts:

1. LibreOffice integration
1. macOS integration
1. Windows integration

### LibreOffice integration

There is already working code for grammar checkers in LibreOffice, using [libdivvun](https://github.com/divvun/libdivvun) at its core, using [code](https://github.com/divvun/libreoffice-divvun) forked from [libvoikko](https://github.com/voikko/corevoikko) as a wrapper around it. However, this code assumes that the library and the linguistic components are all built into one big [oxt file](https://wiki.openoffice.org/wiki/Documentation/DevGuide/Extensions/File_Format), which means more work and heavier downloads for updates, and a lot of duplicate binaries when installing multiple languages.

The aim of this part of the subproject is to make the language independent code and the linguistic components into separate packages, and make them both installable and update-able through a Páhkat repository. At the same time this will make the grammar checker library code be installed only once, and used by all grammar checker languages.

This should come in addition to the present solution with one monolithic package for each language.

### macOS integration

MacOS has a [grammar checker API](https://developer.apple.com/documentation/foundation/nsspellserverdelegate) as part of the spelling api. This part of the subproject should integrate the grammar checker with the macOS API for grammar checking.

There is no default graphical user interface in macOS for configuring the grammar checker. Instead a grammar checker configuration tool has to be built, either as part of the Páhkat GUI client, or as a separate tool. The configuration is stored in a file that is read and used by the grammar checker library, and it should be re-read whenever the grammar checker library detects that it has been changed.

### Windows integration

Windows does not have a grammar checker API. But it might be possible to deliver a limited grammar checker functionality disguised as a speller, as long as enough context is available via the speller API. If so, also Windows support is part of this project within the limits given by the speller API on Windows.

### Common features for all

Only the general grammar checker library is specific to each host environment (aka API). The linguistic support files are the same, and should be shared. All three components should be installed and automatically updated through a Páhkat repository:

* macOS version of the grammar checker library
* LibreOffice version of the grammar checker library
* linguistic support files for each language the user wants

# Deliverables

## Targeted features

* grammar checking for LibreOffice (macOS and Windows)
* grammar checking for macOS systemwide
* possibly grammar checking for Windows systemwide
* all binary files and linguistic support files downloaded, installed and updated using the Páhkat package manager
* linguistic support files installed in a shared location (on macOS & Windows)
* configuration tool for the macOS (and Windows) system-wide grammar checker

## Supported languages

Any language that can be identified with a [BCP47](https://tools.ietf.org/html/bcp47) code.

## Compatibility requirements

* macOS 10.10+
* Windows 7+ (LibreOffice integration only)
* Windows 8.1+ (system wide grammar checker only)

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
