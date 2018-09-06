# Dictionary apps for mobile phones and pads

The Divvun group wants to build a platform for delivering dictionary apps for mobile systems to our users. It is intended to replace our present solution, which requires users to install a third-party dictionary app, and then upload our dictionary content.

In addition to simplifying installation, we also want to build apps that better highlight our strengths both regarding content and linguistic functionality. The apps should be built for easy maintenance, and modularly so that one can easily add new functionality in the future. Also, the code should be written for easy portability (or should be platform independent), so that it will be easy to add support for new platforms if wanted, e.g. macOS, Windows, etc.

It is a primary requirement that the dictionary apps can work without a network connection for all of its basic functionality.

# Deliverables

## Targeted features

* must support iOS and Android
* should use majority language speech recognition (Siri, Google Assistant) to look up words and expressions to translate
* should use speech synthesis from Acapela (or later: us) to read out loud the translated input words (only SME for now, other languages when voices are available)
* should use open-source OCR libraries and built-in camera to recognise printed text and provide translations
  * Tesseract? Other open-source OCR libraries?
  * Tesseract needs to be trained on every font, not optimal
  * see [OCRopus](https://en.wikipedia.org/wiki/OCRopus) for an alternative
  * instead of an OCR library one can use OS services, if available, e.g. [https://developers.google.com/vision/android/text-overview](https://developers.google.com/vision/android/text-overview)
* look-up words in text (using morphological analysis (+ disambiguation using [libdivvun](https://github.com/divvun/libdivvun) if context is available) of input string)
    * preferably using OS services if available
* look-up single words / lemmas in the dictionary (standard search)
* dictionary content updated via a Páhkat repository
    * default: stable channel, check every week
* the details of the user interface should be worked out in cooperation between Divvun&Giellatekno and the winning tenderer
* fuzzy match, possibly based on our speller technology, frequency ranked
* [Korp](http://gtweb.uit.no/korp/) lookup if corpus for the language is available, and Internet connection is available
* paradigm/word form generation (off-line, fst-based)
    * key forms
    * full paradigm
    * which one to generate should be a user preference, or possibly a two-step process: always generate the key forms, then if the user taps on an expansion triangle or somesuch the full paradigm should be displayed
* speedy, fast lookup of dictionary entries
* clear and easy-to-read typography
* easy to use
* should use the same XML format (see [here](https://gtsvn.uit.no/langtech/trunk/words/dicts/scripts/gt_dictionary.dtd) and [here](https://gtsvn.uit.no/langtech/trunk/giella-core/schemas)) as the other dictionary platforms as input (but the app-internal representation of the dictionary can of course be different)
* support for audio, video, images as part of dictionary entries
* search history
* when looking up compound words in text that are not found in the dictionary, the app should analyse the compound word using the fst analyser, and present the articles for the compound constituents. The same goes for derivations.
* dictionary cross reference lookup should be supported, so that one can go from one article to another, using cross references
* hiding / showing different parts of dictionary articles (e.g. etymology, examples, homonyms, synonyms, etc.)

Whether to build one app for each language (containing dictionaries to and from that language), or build one language with all dictionaries installed is presently left unspecified. In any case it must be possible to turn off dictionaries and language pairs the user is not interested in.

See also [Mothertoungues.org](http://mothertongues.org/), and the [dictionary app](https://www.sametinget.se/appar/ordbocker) released by Språkcentrum in Östersund.

## Compatibility requirements

* iOS 9+
* Android 5+

## Acceptance requirements

[Standard requirements](GeneralInfo.md).

<!--
Andre merknader
===============

Vi vil at bygginga skal gjerast automatisk, inklusive signering og anna teknisk
byråkrati. Tanken er at vi skal kunna levera automatiske oppdateringar til faste
intervall (t.d. ein gong i månaden) med dei siste oppdateringane frå termwikien
og andre ordbokskjelder.

Eg meiner vi bør få alle ordbøkene over på ein open redigeringsplattform der
alle kan registrera seg (manuelt - vi vil ikkje ha søppel) og vera med å
redigera. I lag med det førre avsnittet betyr det at folk kan sjå sine eigne ord
etter neste (automatiske) oppdatering. Samtidig bør ordbokskjeldene vera knytte
til fst-ane våre på ein eller annan måte, slik at vi får melding om ord som bør
leggjast til i fst-leksikonet, og omvendt: ord vi har i fst-en som ikkje finst i
ordboka skal finnast som eit tentativt oppslag (men bli ekskludert frå bygginga)
slik at folk ev. kan leggja til omsetjingar, døme, m.m.


Notatar frå eit tidlegare møte, med nokre ref som det kan vera nyttig å ha med seg seinare:

!!! Møte om utlysning av programmeringsjobber, 21.03.2018


Waldayu
 - Ionic Framework - web app framework
 - same code-base for Android and iOS
 - responsive design
 - mobile limitation
    - screen size
    - speed

- weighted Levenshtein search
 Schulz & Mihov 2002 FSA

- Levenshtein automaton on comparison forms

http://waldayu.org/

-->
