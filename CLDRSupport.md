# Extensions to the keyboard infra & improved CLDR support

Our present keyboard development infrastructure needs further improvements, especially in the area of CLDR support and support for locale data. This project is intended to provide that.

# Deliverables

## Locale support
* support for specifying locale data in a simple (yaml) format
* export locale data in CLDR format
* yaml support for Windows specific locale data
* support for building Windows locale installers
* Windows locale installer must be integrated with Windows keyboard installer so that both are installed together

### Compatibility requirements

* Windows 8.1+
* CLDR xml format

## Keyboard support
* export keyboard defs in CLDR xml
* macOS XML import
* improved X11 support
    * read and include existing keyboard defs
    * X11 keyboard def should use include statement + overrides
* support for Chromebooks / ChromeOS
* support for m17n/ibus
* improved templating based on CLDR data online
* possibly a web-based, graphical editor for the yaml flies
    * needs to display both the yaml content and the layout editor, and data should be two-way synced so that one can edit both

### Compatibility requirements

* Windows 7+
* macOS 10.8+
* Linux (X11 & m17n/ibus)
* iOS 10+
* Android 5+
* ChromeOS

A degraded experience is acceptable where older operating systems pose difficulties for implementation.

## General keyboard infra improvements

* Consolidate all automatically downloaded dependencies (excluding git dependencies) in kbdgen to use a Páhkat repository, including the Windows targets

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
