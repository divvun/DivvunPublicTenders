# Divvun public tender 2018

The Divvun pubic tender in 2018 covers the following components, further
specified in the linked documents. The tender covers the following tasks:

* [Support work](SupportWork.md) for existing codebase in Github, 2 years
* Grammar Checker:
    * [Word integration](Word-integrering.md) (in Norwegian for now)
    * [Grammar checker UI and behavior](Spesifikasjon.md) (in Norwegian for now)
* Add support for CLDR export to the keyboard generation infra
    * support for specifying locale data in a simple (yaml) format
    * export locale data in CLDR format
    * export keyboard defs in CLDR xml
* [dictionaries for mobile phones](MobileDictionaries.md) (iOS, Android)
* add spell checking to the mobile keyboards (iOS and Android)
    * speller files updated via a Páhkat repository
* add word completion and word prediction to the mobile keyboards (iOS and Android)
    * possibly in cooperation with the Hfst team at Helsinki University and/or a
      development team in Canada, organised through AltLab at the University of Alberta
* system wide spelling checker for macOS
* system wide spelling checker for Windows 8+, in cooperation with Tino Didriksen
* **GT:** analyseprogram for lingvistar:
    * lim inn tekst, få analyse ut i eit anna vindauge:
        * trestruktur
        * Ulike alternativ for formattering av analysen
        * kopier analysen i passande format, slik at ein enkelt kan lima inn i andre program (som døme når ein skriv artiklar m.m.)
        * **GT** si rolle i dette prosjektet gjeld utforminga av grensesnittet, og testing og vurdering av programmet
    * automatisk oppdaterte språkpakker via Páhkat
    * bruker libdivvun + zcheck-filer
    * versjon både for mac, win og linux
    * jf [Apertium Simpleton](http://wiki.apertium.org/wiki/Apertium_Simpleton_UI)
        * det bør vera nok med [dette](https://apertium.projectjj.com/pkgs.php)
* Páhkat-klient for **iOS**?
* Páhkat-klient for **Android**?
* tekst-til-tale basert på open kjeldekode?
    * mac, linux, win
    * libdivvun som kjerne, med tilpassingar til TTS-behov

There is also a separate [tender admin page](TenderAdmin.md), which specifies
some general parts of the tender process.
