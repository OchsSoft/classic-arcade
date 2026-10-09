# OchsSoft Classic Arcade Downloads

This repository hosts public release downloads for OchsSoft Classic Arcade.

The game is free to download and play. This repository contains release assets
and installation documentation; game and website source are maintained privately.

Download packages from the [latest release](https://github.com/OchsSoft/classic-arcade/releases/latest).

## Windows

Download [ClassicArcade-windows.zip](https://github.com/OchsSoft/classic-arcade/releases/latest/download/ClassicArcade-windows.zip),
extract it, and launch `ClassicArcade.exe`. Keep the program folder together.

## Linux (x86_64)

Download [ClassicArcade-linux-x86_64.tar.gz](https://github.com/OchsSoft/classic-arcade/releases/latest/download/ClassicArcade-linux-x86_64.tar.gz)
and its [SHA-256 checksum](https://github.com/OchsSoft/classic-arcade/releases/latest/download/ClassicArcade-linux-x86_64.tar.gz.sha256).
Verify with `sha256sum -c ClassicArcade-linux-x86_64.tar.gz.sha256`, extract the
archive, and run `./ClassicArcade/ClassicArcade`.

A graphical desktop with glibc 2.35 or newer is required. On NixOS, use
`steam-run ./ClassicArcade/ClassicArcade`.

## macOS (Apple Silicon and Intel)

The universal2 macOS package is awaiting Apple's notarization approval and is
not yet available for download. The release asset will be named
`ClassicArcade-macos.zip`. Once published:

1. Download and extract `ClassicArcade-macos.zip`.
2. Drag `ClassicArcade.app` into your Applications folder.
3. Open Applications and double-click ClassicArcade.

The release app will be Developer ID signed, notarized by Apple, and carry a
stapled notarization ticket. It includes Python and the game dependencies, with
native code for Apple Silicon and Intel; Python and Rosetta installation are
not required.

Intel startup/shutdown and settings/statistics persistence have been tested.
Both architecture slices are verified in every native binary. Apple Silicon
execution and interactive audio/controller acceptance remain to be tested.

Settings and statistics are stored in
`~/Library/Application Support/OchsSoftClassicArcade`, outside the app bundle.

OchsSoft name, logo, and brand assets are owned by OchsSoft LLC.
