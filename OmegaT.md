# OmegaT integration

OmegaT is a translator's workbench, with support for a lot of tools to improve translation speed and quality. But most supported tools are not according to our technologies or needs. We thus want our tools to be integrated smoothly and in such a way that we can deliver a package with everything installed.

# Deliverables

We want the following integrated:

* spellers (hfst-ospell + zhfst files, or any other lib that can read zhfst files)
* grammar checkers (as an alternative or complement to spellers)
* dictionaries
* terminology lists
* (disambiguated) lemmatisation of words in text
* lemmatised indexes of dictionaries and word lists/terminologies
* corpus search (online, but with results presented in a pane in OmegaT)
* MT is already supported [via Apertium](http://wiki.apertium.org/wiki/Apertium_OmegaT_Native "Apertium OmegaT Native article on the Apertium wiki")
* most, if not all, should be installable and automatically updated via a Páhkat repo

## Compatibility requirements

* Windows 7+
* macOS 10.8+
* Linux

## Acceptance requirements

Before delivery of the final version, the code should meet [the standard requirements](GeneralInfo.md), plus the following:

* a working setup with a Páhkat repository
* working installation packages for all components
