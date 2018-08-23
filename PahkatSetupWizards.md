# Setup Wizards for the Páhkat clients

This subproject should add a new feature to the Páhkat clients for [Windows](https://github.com/divvun/pahkat-client-windows) and [macOS](https://github.com/divvun/pahkat-client-macos). The new feature should guide users through a first-time configuration and installation of their wanted languages and tools.

# Deliverables

The new feature is a first-time setup wizard that:

* runs first time (or on request)
* asks for languages of interest
* asks for tools of interest
* downloads and installs the selected tools/components (and all dependencies)
* make the clients only show the selected language(s) in the main window (ie hide the languages not relevant to the user)
    * (or show them under some sort of *other* category)
    * language set can be changed later in settings window
    * notify user of new tools for the selected language(s)

## Compatibility requirements

* Windows 7+
* macOS 10.8+

## Acceptance requirements

[Standard requirements](GeneralInfo.md).
