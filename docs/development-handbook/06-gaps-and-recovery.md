# Known gaps and recovery

| Symptom | Inspect first | Safe next action |
|---|---|---|
| Checksum mismatch | Asset and checksum from the same release; exact filename | Redownload matching files; do not launch a mismatched archive |
| Missing files after extraction | Complete extracted directory and available disk space | Extract a verified archive into a fresh directory; preserve personal data |
| Existing Linux launcher reports missing file | Actual command and NixOS compatibility wrapper | Retry the documented `steam-run` path, then collect the error |
| Graphics window never opens | Desktop availability and terminal startup error | Diagnose graphics/runtime boundary in a local test; do not reset statistics |
| macOS security rejection | Exact release and operating-system message | Escalate package/signing investigation to publisher; retain verification evidence |
| Statistics appear reset | Actual platform data path and prior backup | Stop further writes and compare preserved copies; do not repeatedly reinstall |
| Latest link gives an unexpected build | Actual tag and downloaded digest | Pin the report to the named release rather than the moving link |

## Prioritized improvements

First, document actual Windows and Linux personal-data paths, save filenames and safe recovery behavior with source-backed verification. Acceptance is a disposable account test showing an upgrade and restore retain expected settings and statistics. Second, publish a platform validation record for each release, including NixOS launch, controls, sound, normal close and repeat launch. Acceptance is concrete recorded local results rather than a general Linux claim.

Third, make checksums and immutable version references consistent across all platform downloads. The root README supplies checksums for Linux and macOS but no Windows checksum link. Confirm the real release assets before adding one. Fourth, add a public controls/usage guide and an issue template focused on version, platform, archive integrity and reproducible behavior. These improve support without exposing private implementation.

## Backup and rollback boundaries

Keep an untouched known-working archive and the associated digest. Back up personal data separately after the program has exited. On macOS, the path is explicitly documented; on other systems, establish it before a destructive cleanup. A rollback replaces complete program files with a known version and restores only data that version understands. Because schema compatibility is not documented here, do not promise that an older release can read data last written by a newer one.

There is no server or container to stop, no database volume in this repository, and no production configuration to restore from Git. The public documentation is recovered through ordinary Git history; binaries are recovered from verified release artifacts. If a release asset disappears, the public checkout alone cannot reconstruct it. Maintaining an authorized release archive belongs to the publisher's preservation process.
