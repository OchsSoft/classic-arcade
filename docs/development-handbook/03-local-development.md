# Local setup on NixOS and other platforms

## Reviewing the repository

From the checkout, inspect `git status --short --branch`, `git ls-files`, and `README.md`. There is no `npm install`, Python environment or build command in this repository. Git and a text editor are enough to edit the public documentation. Keep release experiments and downloaded archives outside tracked source. A topic branch and a human-reviewed PR are the publication path for documentation changes.

## Linux and NixOS installation

Download the Linux x86_64 archive and its matching `.sha256` file from the same actual release. In the download directory:

```bash
sha256sum -c ClassicArcade-linux-x86_64.tar.gz.sha256
tar -xzf ClassicArcade-linux-x86_64.tar.gz
steam-run ./ClassicArcade/ClassicArcade
```

The first command is a verification gate: if it fails, stop and check filenames, exact bytes and release identity. The last command is the README's NixOS launch path. `steam-run` supplies a compatibility environment for conventional Linux binaries; the repository does not provide a pinned Nix shell or installation instructions for that host tool. Its presence and the graphical environment must be established locally. Do not change the host configuration or install packages merely to complete a documentation review.

A non-NixOS Linux desktop uses `./ClassicArcade/ClassicArcade` according to the README and must meet its glibc requirement. A terminal reporting “file not found” for an existing launcher can reflect a missing interpreter or loader, not a missing game file. On NixOS, first confirm that the documented wrapper was used before deleting or redownloading unrelated files.

## Windows and macOS

On Windows, extract the complete zip and launch `ClassicArcade.exe`. On macOS, extract the zip, move the app into Applications and open it normally. The documented checksum command on macOS is:

```bash
shasum -a 256 -c ClassicArcade-macos.zip.sha256
```

Do not recommend removing quarantine or bypassing operating-system security as routine installation instructions. If the app fails signature validation, collect the actual release and error and have the publisher investigate the package. This checkout contains no certificate, signing key or notarization log with which to repair it.

## Evidence limits

These are the committed installation paths, not a new test result. No binary was launched during this handbook's preparation. Before publishing a release change, the source/release maintainer must establish real local platform evidence, including NixOS for the Linux package. A README edit alone cannot prove a new bundle works.
