# System wide spelling checkers

The Divvun group has earlier had a solution for a system-wide speller on macOS. Due to changes in macOS related to security, the old solution is not working. We have also tried to build a similar solution for Windows in cooperation with Tino Didriksen, after system-wide spelling was provided there as part of Windows 8. That code is almost done, but some show-stopper bugs have hindered us from releasing such a tool.

This project should modernise the macOS speller, finalise the Windows speller, and update both to support updates via Páhkat repositories.

# Deliverables

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

## Compatibility requirements

* Windows 8.1+
* macOS 10.10+

## Acceptance requirements

Before delivery of the final version, the code should meet [the standard requirements](GeneralInfo.md), plus the following:

* installable & working spellers, both as independent installers and through a Páhkat repository
