# General info

It is possible to submit offers for a single subproject, or some subprojects, but see the note below.

The Divvun group can — at its own sole discretion — decide to not purchase a given subproject from any tenderer. The final set of subprojects to actually go forward with is decided single-handedly by the Divvun group.

**Note:** Everything else being equal, offers covering everything will be preferred over offers for parts of the tender, and offers covering more subprojects will be preferred over offers covering fewer subprojects. Also, more experience in the relevant programming languages or topic at hand is preferred over less experience. This can be documented e.g. as a list of past projects, with a reference person with contact information for each such project. Minimum number of reference projects is specified below.

## Tender requirements

* solid experience in the programming languages and other relevant skills needed (see detailed requirements list below)
* audited financial reports and tax reports for the last fiscal year
* additional requirements may be specified for some subprojects

**solid** = reference to at least five (project lead)/three (team members) independent projects involving the language or platform in question.

| Sub-project                | C/C++ |  Rust | Python |(Node)JS|  GUI  | iOS   | Android | macOS | Windows | Other |
| -------------------------- |:-----:|:-----:|:------:|:------:|:-----:|:-----:|:-------:|:-----:|:-------:|:-----:|
| Support work               |   x   |   x   |   x    |   -    |   -   |   x   |   x     |   x   |   x     |   -   |
| CI / CD                    |   x   |   -   |   -    |   -    |   -   |   x   |   x     |   x   |   x     | CI/CD |
| REST/GraphQL API           |   -   |   -   |   -    |   -    |   -   |   -   |   -     |   -   |   -     |API/RST|
|____________________________|_______|_______|________|________|_______|_______|_________|_______|_________|_______|
| Grammar Check MS & Google  |   x   |   -   |   -    |   x    |   x   |   x   |   x     |   x   |   x     |   -   | 
| Basic M Spell checking     |   -   |   x   |   -    |   -    |   -   |   x   |   x     |   -   |   -     |   -   |
| System wide spelling       |   x   |   -   |   -    |   -    |   -   |   -   |   -     |   x   |   x     |   -   |
|____________________________|_______|_______|________|________|_______|_______|_________|_______|_________|_______|
| Grammar Check LO and mac   |   x   |   -   |   x    |   -    |   -   |   -   |   -     |   x   |   x     |   -   |
| Keyboard infra extensions  |   -   |   -   |   x    |   -    |   -   |   -   |   -     |   x   |   x     |   -   |
| Dictionary app for phones  |   x   |   -   |   -    |   -    |   x   |   x   |   x     |   -   |   -     | Java  |
| OmegaT integration         |   -   |   -   |   -    |   -    |   -   |   -   |   -     |   x   |   x     | Java  |
| Web dictionary app         |   -   |   -   |   -    |   x    |   x   |   -   |   -     |   -   |   -     |XQR,wbp|
| Páhkat Setup Wizards       |   x   |   -   |   -    |   -    |   -   |   -   |   -     |   x   |   x     | Inno  |
| Rewrite of iOS keyboard    |   -   |   -   |   -    |   -    |   x   |   x   |   -     |   -   |   -     | Swift |
| Advanced M Spell checking  |   x   |   x   |   -    |   -    |   x   |   x   |   x     |   -   |   -     | Swift |
| Graphical analysis app     |   x   |   -   |   -    |   -    |   x   |   -   |   -     |   x   |   x     | Linux |
| Word compl. and prediction |   x   |   x   |   -    |   -    |   -   |   x   |   x     |   -   |   -     | Java  |
| Open-source text-to-speech |   x   |   -   |   -    |   -    |   -   |   -   |   -     |   x   |   x     |   -   |
|____________________________|_______|_______|________|________|_______|_______|_________|_______|_________|_______|
| Together, each skill       |  11   |   4   |   3    |   2    |   6   |   8   |   7     |  10   |   10    |   -   |

Other must-have requirements:

* building mobile keyboards and keyboard apps
* building desktop keyboards

For the "immediate start" group, the following should also be submitted:

* realistic and sound project plan, containing at least:
    * timetable with milestones and planned final delivery date
    * clearly identified tasks for both the tenderer and the Divvun group
    * a layout of how to test the deliverables, both functionality and GUI design

### Summary of the requirements table and other requirements

#### Must-have requirements (A-krav)

* solid C/C++ programming experience
* solid Windows, Android, macOS and iOS programming experience
* solid GUI design experience
* experience with natural language technology and finite state machines and transducers
* experience with working with minority languages and/or multiple natural languages

#### Should-have requirements (B-krav)

The more the better - this will influence the tender decision:

* solid mobile keyboards and keyboard apps programming experience
* solid desktop keyboards programming experience
* solid Objective C/Swift programming experience
* solid Rust programming experience
* solid Python programming experience
* solid Java programming experience

#### Preferable requirements (C-krav)

Also the more the better, and will influence the tender decision, but to a
lesser degree than the previous section.

* solid NodeJS and JavaScript programming experience
* solid Inno installer programming experience
* solid Linux programming experience
* solid API & REST design experience
* solid XQuery programming experience
* solid webapp programming experience

## Acceptance requirements

Before delivery of the final version of each subproject:

* the code must be in [Github.com/divvun](https://github.com/divvun), with all tests passing
* the code must build on all platforms specified for each subproject
* the code must have been built with all tests passing on at least one of the computers of the Divvun group
* the code, possible API's and all functionality must be documented
* the code must meet specifications
* the code must follow linting standards agreed upon at contract signing time, or a specified time short thereafter
* further acceptance requirements may be specified in each subproject

## Copyright and license

* All code should have an open licence selected by Divvun
* the delivered code must be © UiT
