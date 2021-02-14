# streamdeck-applescript
A Stream Deck plugin for running arbitrary Applescript code

Run any Applescript from your Elgato Stream Deck - allows for either .scpt files or inline applescript code. Note that currently the UI isn't updated to show if a file is being used as the reference, not sure why... Otherwise it should work nicely!

Please note, this does seem to run fine in Streamdeck v4.3.0 (11246) but it is NOT using v2 of the SDK - which means you must use an older version of the DistributionTool if you want to package it up as a .sdPlugin file, or it'll act very weird!

The .sdPlugin in Releases should work fine, though.


## Building
Download and install Xcode on your mac from the App store
  - `open Sources//RunApplescript.xcodeproj/project.pbxproj`, install additional components as requested.
  - I believe this is what re-mapped the paths from `/Users/mushoo/...`
  - get the schema for the project
```
(cd Sources ;  xcodebuild -list -project RunApplescript.xcodeproj/)


```
  - build the project

```
(cd Sources ;  xcodebuild -scheme RunApplescript build)

```

