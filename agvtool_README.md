# agvtool

## [Reference](https://developer.apple.com/library/content/qa/qa1827/_index.html)

## Intro
- agvtool is a command-line tool that allows you to automatically increment these numbers to the next highest number or to a specific number. This document provides step-by-step instructions for updating your build and version numbers using agvtool. The "Xcode" and "Command Line" sections indicate the steps to be respectively performed in Xcode and the command line.

## Naming convention
- [major].[minor].[patch]
- [version-number].[build-number]

***

## Usage

1. Enable agvtool & Setup your version and build numbers

    + In Build Settings, set Current Project Version to a value of your choosing: Your Xcode project data file, project.pbxproj, includes a CURRENT_PROJECT_VERSION (Current Project Version) build setting, which specifies the current version of your project. agvtool searches project.pbxproj for CURRENT_PROJECT_VERSION. It continues running if CURRENT_PROJECT_VERSION exists and stops running, otherwise. Its value is used to update the build number.

    + Set Versioning System to Apple Generic: By default, Xcode does not use any versioning system. Setting Versioning System to Apple Generic ensures that Xcode will include all agvtool-generated version information in your project.

2. Updating the Version Number and Build Number

    + Update Version Number to a specific version:
        - agvtool new-marketing-version [your_specific_version]

    + Auto-increment Build Number to the next highest integer:
        - agvtool next-version -all

    + Manual build number setup:
        - agvtool new-version -all [your_specific_version]

3. Viewing Version Numbers & Build Number

    + View the current Version Number:
        - (xcrun) agvtool what-marketing-version

    + View Build Number:
        - (xcrun) agvtool what-version
