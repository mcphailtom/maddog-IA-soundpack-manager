# Maddog Sound Fix

Maddog Sound Fix is a Windows tool that builds and installs a separate Maddog sound add-on from Leonardo Fly the Maddog X and Immersive Audio packages you already own.

It includes neither paid add-on, never edits either source package, and keeps the generated package on your PC.

## Download and install

This repository is the public download and release-notes home. Download the current Windows ZIP under **Releases**, verify its published SHA-256, and extract all three files into one private local folder.

Each ZIP contains exactly:

- `maddog-sound-fix.exe`
- `README.md`
- `Install Maddog Sound Fix.bat`

Close Microsoft Flight Simulator and Leonardo Manager, then double-click **`Install Maddog Sound Fix.bat`**. One process detects the supported Store or Steam Community folder, validates both paid packages, builds the fixed sound package, and installs it as:

```text
maddog-ia-sound-fix-<version>
```

A new package is completed and validated before an older version-stamped Maddog Sound Fix package is removed. The installer never deletes a folder from its name alone.

If you used an earlier release, first move the old unversioned generated folder—usually `maddog-sound-compat-native-2024` or `maddog-sound-compat-msfs2020`—out of Community. Never delete either paid source package.

Do not download or share a generated sound package. Every user must own both add-ons and build locally from their own installations.

## Supported versions

| Simulator | Leonardo | Immersive Audio |
| --- | --- | --- |
| Native MSFS 2024 | **2.1.282** or **2.1.283** | **1.0.0** |
| MSFS 2020 | **2.0.281** | **1.0.0** |

MSFS 2020 remains runtime-unverified by the maintainer.

Restore both paid packages to stock before running the tool. If another conversion replaced sound XML, banks, model files, or package metadata, use the official installer/updater or reinstall the affected add-on. Validation is designed to stop rather than build from modified purchased files.

## What it does

- Detects known Store and Steam Community locations and the exact Leonardo and IA package folders.
- Validates supported versions, source identities, sound routing, model attachment points, generated package metadata, and repeatable output.
- Starts from Leonardo's complete setup and applies one maintained IA-first sound configuration.
- Preserves Leonardo Manager crew voices, PNF callouts, the complete mechanic call, and genuinely unique aircraft behavior.
- Builds a separate removable Community package instead of changing either paid add-on.
- Safely replaces earlier version-stamped Maddog Sound Fix packages only after proving their marker, payload hash, metadata, exact tree, and physical identity.

The old `overlay` and `choices` commands, public family customization, and saved ownership files are no longer used. Future sound-policy changes ship in the catalog with a new release.

## Sound coverage

The maintained mix uses IA for compatible machinery, engine, wind, warning, and control families. Two isolated compatibility gaps remain Leonardo-owned:

- **Cockpit-door motion**, because IA's routes become audible too late for the native animation.
- **Fast approach-minimums warning**, because the released IA Event targets a Wwise object absent from its bank.

Native 2024 also retains Leonardo-selected crew, pilot-not-flying callouts, the three-perspective mechanic call, and aircraft-specific behavior.

See [Finnisher's script and Maddog Sound Fix](COMPARISON.md) for the practical differences. Thanks to @finnisher and @DrPredrag for the community work that made this project possible.

## Project boundary

The development source remains private. This public repository is an artifact and release-notes portal, never a source mirror. The executable is unsigned and may trigger a SmartScreen warning; verify the release checksum before running it.

## License

Maddog Sound Fix is distributed under the MIT License. The packaged README contains the complete project license and pinned third-party notices.
