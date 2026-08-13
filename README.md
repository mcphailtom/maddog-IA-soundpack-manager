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

The installer completes and validates a hidden candidate before touching an older versioned package. It deletes an old package only when its exact name and marker identify same-target Maddog Sound Fix output. Generated package directories are wholly tool-owned; links, junctions, foreign markers, and another target stop deletion.

There is no rollback. If deletion or publication fails, keep the simulator closed and rerun the installer. Neither paid source package is deleted or modified.

If you used an earlier unversioned release, first move the old generated folder—usually `maddog-sound-compat-native-2024` or `maddog-sound-compat-msfs2020`—out of Community.

Do not download or share a generated sound package. Every user must own both add-ons and build locally from their own installations.

## Supported versions

Maddog Sound Fix follows the latest validated Leonardo package for each supported simulator:

| Simulator | Leonardo | Immersive Audio |
| --- | --- | --- |
| Native MSFS 2024 | **2.1.283** | **1.0.0** |
| MSFS 2020 | **2.0.283** | **1.0.0** |

Older Leonardo builds are not supported. Update Leonardo and restore both paid packages to stock before running the tool. Modified sound, bank, model, or package files remain unsupported.

MSFS 2020 remains simulator-runtime-unverified by the maintainer and may require the generated package to load after Leonardo.

## What it does

- Detects known Store and Steam Community locations and the exact Leonardo and IA package folders.
- Starts from Leonardo's complete setup and applies one maintained IA-first sound configuration.
- Preserves Leonardo-selected crew, PNF callouts, the complete mechanic call, and aircraft-specific behavior.
- Relocates selected Wwise Events into a separate removable Community package.
- Replaces earlier versioned Maddog Sound Fix output through exact name and same-target marker authority.

The tool exposes only the `install` command. It has no uploader and does not modify either paid package.

## Sound coverage

The maintained mix uses IA for compatible machinery, engine, wind, warning, and control families. Two isolated compatibility gaps remain Leonardo-owned:

- **Cockpit-door motion**, because IA's routes become audible too late for the native animation.
- **Fast approach-minimums warning**, because the released IA Event targets a Wwise object absent from its bank.

See [Finnisher's script and Maddog Sound Fix](COMPARISON.md) for the practical differences. Thanks to @finnisher and @DrPredrag for the community work that made this project possible.

## License

Maddog Sound Fix is distributed under the MIT License. The packaged README contains the complete project license and pinned third-party notices.
