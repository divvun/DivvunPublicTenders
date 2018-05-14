# System wide spelling checkers

## Targets

* macOS, based on
  [MacDivvun.service](https://github.com/divvun/macdivvun-service)
* Windows 8+, in cooperation with Tino Didriksen ([source code](http://svn.tinodidriksen.com/tdc/oss/spellers))
* speller engine and speller lexicon updates delivered via a Páhkat repository & the Páhkat clients
* both spellers should be language independent, work for any defined locale (new locales should be defined as needed through the installation of keyboards for those locales)
* both spellers should be distributed in two ways
    * through a Páhkat repository
    * as independent installers
* both spellers must support user dictionaries and all other functionality supported by the respective API's (see below).

## Other notes

Both the Windows and macOS API's for system-wide speller integration are public. They can be found here:

* [Windows](https://msdn.microsoft.com/en-us/library/windows/desktop/hh869748.aspx)
* [macOS](https://developer.apple.com/documentation/appkit/nsspellchecker)

This subproject may possibly be extended to cover grammar checking, by integrating already existing grammar checker code with the spelling checker API (and on macoS: the grammar checker API).

## Compatibility requirements

* Windows 8.1+
* macOS 10.10+

## Tender requirements

* solid macOS programming experience
* solid Windows programming experience

**solid** = reference to at least five independent projects involving the language or platform in question.

## Subproject selection criteria

* experience with similar work

## Acceptance requirements

Before delivery of final version:

* user documentation
* passing all defined tests
* all code in Github
* installable & working spellers, both as independent installers and through a Páhkat repository
