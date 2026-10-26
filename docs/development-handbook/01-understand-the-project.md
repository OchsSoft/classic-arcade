# Understand the project

## The product and this repository

This is the public download and installation repository for OchsSoft Classic Arcade. The root README explicitly says that game and website source are maintained privately. This checkout therefore cannot be used to change game logic, rebuild executables, inspect save code or run source tests. Its development work is release presentation, installation documentation and the integrity of published assets.

A release asset is a packaged file attached to a GitHub release rather than a normal source file. The repository links the latest release and named platform archives. The links using `releases/latest` move when a newer release becomes latest; they are convenient entry points, not immutable version evidence. For a reproducible support report, record the actual downloaded release tag, asset name, checksum and platform.

The reader has two roles. As a player, download the appropriate archive, verify it where a checksum is supplied, extract the whole program folder and launch the platform entry point. As a maintainer, check that documentation matches the actual release, investigate reports without exposing private source, and coordinate any executable change in the separate source repository's own workflow.

## Platform promises in the committed README

Windows uses `ClassicArcade-windows.zip` and `ClassicArcade.exe`. Linux x86_64 uses `ClassicArcade-linux-x86_64.tar.gz`, a SHA-256 checksum companion, and `./ClassicArcade/ClassicArcade`. The stated Linux requirement is a graphical desktop with glibc 2.35 or newer; NixOS uses `steam-run` around the launcher. macOS uses `ClassicArcade-macos.zip`, a checksum, and `ClassicArcade.app` copied into Applications.

The README says the macOS app is Developer ID signed, notarized and stapled, includes Python and dependencies, supports Apple Silicon and Intel, and does not require installing Python or Rosetta. These are the release documentation's assertions. This handbook did not download or inspect a current binary and does not claim a fresh signing, architecture or NixOS runtime verification.

## What is intentionally unknown here

There is no committed API, game-loop source, settings schema, Linux data-path contract, build workflow or automated test harness. A maintainer should ask the source/release owner for those facts when needed rather than fill the public guide with guesses. The public documentation must remain useful on its own while accurately marking that evidence boundary.
