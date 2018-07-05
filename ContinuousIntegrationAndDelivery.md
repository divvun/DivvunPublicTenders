# Continuous Integration And Delivery

To improve our delivery frequency and code quality, the Divvun group wants to improve the workflow from source code to delivered products and services by adding Continuous Integration (CI) and Continuous Delivery (CD) to it.

* open source if possible
* all platforms
* list of products
* training of Divvun members to run it by themselves

A semi-CI (nightly) service for the analysers and spell checkers already exists, with output at [https://apertium.projectjj.com/](https://apertium.projectjj.com/), and operated by [Tino Didriksen](https://stackoverflow.com/cv/tinodidriksen). This subproject should be a complement to that existing service, with an option of replacing it in the future, if need be.

## Products and services

The following is a list of products and services for which CI and CD should be delivered, in no particular order.

### Continuous integration

Programs and libraries:

* iOS keyboard apps
* Android keyboard apps
* desktop keyboard packages/installers
* grammar checker engines/libs
* speller engines/libs
* linguistic analysis program

Possibly linguistic resources (this is presently handled by Tino Didriksen, cf above):

* morphological analysis, generation, tokenisation
* syntactic analysis
* spellers
* hyphenators
* grammar checkers

Continuous integration of the linguistic resources and tools should include automatic regression and coverage testing (not presently done), so that one can automatically decide whether to do a release.

### Continuous delivery

This is mainly done through Páhkat repository updates of the following (the list may be extended):

* spellers
* grammar checkers
* morphological analysers & generators
* desktop keyboard packages
* grammar checker engines
* speller engines for LO, MS Office
* linguistic analysis app

The following should be delivered through their respective, official channels:

* mobile keyboard apps

## Deliverables

* working CI and CD services
* documentation
* training for select Divvun team members

## Compatibility requirements

* CI and CD must work for all listed products and services

## Acceptance requirements

* complete documentation
* working CI and CD services
* all relevant code in the Divvun group's Github or Subversion repositories
* training given to relevant persons

## Requirements

* solid CI experience
* solid CD experience
