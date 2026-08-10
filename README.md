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

The installer completes and validates a hidden candidate before touching an older versioned package. It deletes an old package only when its exact name and minimal marker identify same-target Maddog Sound Fix output. Generated package directories are wholly tool-owned; links, junctions, foreign markers, and another target stop deletion.

There is no rollback. If deletion or publication fails, keep the simulator closed and rerun the installer. Neither paid source package is deleted or modified.

If you used an earlier unversioned release, first move the old generated folder—usually `maddog-sound-compat-native-2024` or `maddog-sound-compat-msfs2020`—out of Community.

Do not download or share a generated sound package. Every user must own both add-ons and build locally from their own installations.

## Report an unsupported package version

The same executable can create one encrypted compatibility fingerprint:

```powershell
.\maddog-sound-fix.exe fingerprint --output ".\maddog-sound-fingerprint.zip"
```

The outer ZIP contains a public target/version/five-hash header plus `evidence.age`, which encrypts the approved XML, model, and offset-free Wwise evidence to the maintainer's public recipient. The command never uploads anything.

Check existing issues, then attach only the generated fingerprint ZIP. Never attach either paid package, decrypted evidence, a generated overlay, or diagnostics containing private paths. A fingerprint is evidence for maintainer review; it does not automatically add support.

## Supported versions

| Simulator | Leonardo | Immersive Audio |
| --- | --- | --- |
| Native MSFS 2024 | **2.1.282** or **2.1.283** | **1.0.0** |
| MSFS 2020 | **2.0.281** | **1.0.0** |

MSFS 2020 remains runtime-unverified by the maintainer.

Restore both paid packages to stock before running the tool. Source admission checks exact target and package versions plus five representative SHA-256 pins. PNF, current crew, and interior model files remain operational parser inputs; modified purchased packages are unsupported and user-owned.

## What it does

- Detects known Store and Steam Community locations and the exact Leonardo and IA package folders.
- Starts from Leonardo's complete setup and applies one maintained IA-first sound configuration.
- Preserves Leonardo-selected crew, PNF callouts, the complete mechanic call, and aircraft-specific behavior.
- Relocates selected Wwise Events and adds only the two approved model locators when needed.
- Builds a separate removable Community package instead of changing either paid add-on.
- Replaces earlier versioned Maddog Sound Fix output through exact name and minimal same-target marker authority.
- Creates encrypted, issue-shareable compatibility evidence for unknown versions without uploading it.

The old `overlay` and `choices` commands, public family customization, saved ownership files, and separate fingerprint collector are no longer used.

## Sound coverage

The maintained mix uses IA for compatible machinery, engine, wind, warning, and control families. Two isolated compatibility gaps remain Leonardo-owned:

- **Cockpit-door motion**, because IA's routes become audible too late for the native animation.
- **Fast approach-minimums warning**, because the released IA Event targets a Wwise object absent from its bank.

See [Finnisher's script and Maddog Sound Fix](COMPARISON.md) for the practical differences. Thanks to @finnisher and @DrPredrag for the community work that made this project possible.

## Project boundary

The development source remains private. This public repository is an artifact and release-notes portal, never a source mirror. The executable is unsigned and may trigger a SmartScreen warning; verify the release checksum before running it.

## License

Maddog Sound Fix is distributed under the MIT License. The packaged README contains the complete project license and pinned third-party notices.
