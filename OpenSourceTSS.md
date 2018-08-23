# Open Source TTS

The Divvun group, in cooperation with the Norwegian Sámi Parliament and Acapela, has developed a North Sámi TTS system. While it is quite possible that we will build TTS systems for other languages using closed-source solutions in the future, we also want an open-source end-to-end solution for a number of reasons, the main reason being to avoid vendor lock-in. It is also likely that there won’t be financial resources to build TTS systems for many of the languages we work with using a commercial engine, and we also want to make our work on speech synthesis easily available to other researchers. Finally, it is also important that we keep building our own expertise and knowledge in this area.

# Deliverables

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
* possible candidates
    * [festvox/festival system](http://festvox.org/)
    * [Idlak](https://github.com/idlak/idlak)
    * [merlin](https://github.com/CSTR-Edinburgh/merlin)
        * merlin is only available as a Python version for now, and it is unclear
      how this could be used outside a research lab
        * on the other side it seems to be at the front of the research field,
      producing high quality voices
    * [Mimic](https://mycroft.ai/documentation/mimic/)
    * other open-source engines may be suggested
    * also: this field is in constant development, so when this sub-project is started, the options for speech synthesis engines must be re-evaluated
* the selection of engine must be done in cooperation with Divvun and its
  partners, as the engine used for synthesis must be the same as or compatible
  with the one used for voice generation.
* the engine should also be compatible with, buildable for and runnable on mobile systems

## Integration with operating systems

Closed-source integration will be accepted if required by the OS vendor.

## Updates

TTS engine and TTS voices should be updated via a Páhkat repository & the Páhkat clients

## Compatibility requirements

* Windows 7+
* macOS 10.8+
* Linux

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
