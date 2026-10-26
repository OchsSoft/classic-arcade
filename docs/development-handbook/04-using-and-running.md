# Player journeys and normal close

## First launch

Choose the package for the computer's architecture and operating system, download it with any checksum companion, verify it, and extract it to a location where the whole application can remain together. On NixOS, open a terminal in the extraction parent and use the documented wrapper command. Keep the terminal available during the initial launch so an early failure remains visible.

After the application opens, use its own visible menus for game selection and settings. This repository does not document exact key bindings, game rules or an internal settings screen layout, so this handbook does not invent button names. A release should ideally ship accessible help for those tasks. If controls are unclear, preserve that as a concrete documentation gap with a screenshot and release version.

## Upgrade without losing history

Close the running application before replacing program files. Retain the old archive and record its version until the new release has been checked. On macOS, back up the documented settings/statistics directory separately, then replace the app bundle. Avoid copying arbitrary old executable files into the new bundle: that creates a mixed version that cannot be diagnosed reliably.

For Windows or Linux, determine the real personal-data location from the source project's documentation or the running application's diagnostics before attempting a settings reset. The public README does not currently establish it. Preserve candidate data rather than delete it based on a guess. A new application directory can help distinguish a damaged installation from personal settings, but it does not necessarily isolate user data because the application may use a shared platform directory.

## Normal close

Use the application's ordinary quit control or close its window. Wait for the process to exit before moving the bundle or restoring data. If launched in a terminal, confirm that the prompt returns. Do not assume an unresponsive window means it is safe to overwrite files while a process is still writing. This repository does not document the atomicity of settings/statistics writes, so conservative backup and complete process exit are appropriate.

## Troubleshooting information to collect

Distinguish “archive will not extract,” “launcher cannot start,” “window opens then closes,” “sound or controls fail,” and “personal progress changed.” Those are different boundaries. Report the first reproducible failure and exact command instead of the broad statement “Linux is broken.” A reproducible support case should identify the latest working release too, when known.
