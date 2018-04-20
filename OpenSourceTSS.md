# Open Source TTS

## Platforms to support

* macOS
* Linux
* Windows (will most likely require an API license from MS)
* Android
* iOS

## Text processing, engine integration

Text processing is done using Hfst and VislCG3 through
[libdivvun](https://github.com/divvun/libdivvun).

After the text is processed and turned into synthesis symbols (IPA, SAMPA, or
something similar), it will be fed to the synthesis engine as the last step to
produce sound.

### Task

`libdivvun` needs to be extended with pipeline support for the synthesis engine,
so that the processed text can be fed to the synthesis engine. This is a major
part of the work for this section of the tender.

## Speech synthesis engine

* must be open source
* a possible candidate is the [festvox/festival system](http://festvox.org/)
* another candidate is [Idlak](https://github.com/idlak/idlak)
* a third candidate is [merlin](https://github.com/CSTR-Edinburgh/merlin)
    * merlin is only available as a Python version for now, and it is unclear
      how this could be used outside a research lab
    * on the other side it seems to be at the front of the research field,
      producing high quality voices
* a fourth candidate could be [Mimic](https://mycroft.ai/documentation/mimic/)
* other open-source engines may be suggested
* the selection of engine must be done in cooperation with Divvun and its
  partners, as the engine used for synthesis must be the same as or compatible
  with the one used for voice generation.

## Integration with operating systems

Closed-source integration will be accepted if required by the OS vendor.

## Updates

TTS engine and TTS voices should be updated via a Páhkat repository & the Páhkat clients

## Compatibility requirements

* Windows 7+
* macOS 10.8+
* Linux

## Tender requirements

* solid macOS programming experience
* solid Windows programming experience

**solid** = reference to at least five independent projects involving the language or platform in question.

## Subproject selection criteria

* none

## Acceptance requirements

Before delivery of final version:

* user documentation
* passing all defined tests
* all code in Github
