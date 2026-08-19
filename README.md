# Maddog Sound Fix

Maddog Sound Fix is a portable Windows application that builds a separate compatibility package from Leonardo Fly the Maddog X and sound packages you already own.

It includes neither paid add-on, never edits either source package, and keeps the generated package owner-local on your PC.

## Download and run

This repository is the public download and release-notes home. Download the current Windows ZIP under **Releases**, compare its SHA-256 with the release notes, and extract both files into one private local folder:

- `maddog-sound-fix.exe`
- `README.md`

Close Microsoft Flight Simulator and Leonardo Manager, then run `maddog-sound-fix.exe`. The portable application uses the Microsoft Edge WebView2 runtime already installed on Windows; no browser runtime or installer is bundled.

The Deployment Receipt shows the detected Community folder, Leonardo package, selected and installed sound sources, generated-fix state, and the exact available action. IA 1.0 is selected by default. Native MSFS 2024 users may optionally choose their owner-local Anniversary beta folder for the current session.

If automatic detection is wrong or ambiguous, choose the exact physical Community folder. A link or junction is reported but cannot become mutation-ready; choose its physical target instead. Community and beta choices are never persisted.

Before Install, Update, Reinstall, source switching, or Uninstall, acknowledge that MSFS and Leonardo Manager are closed. Source switching uses the clearly labelled primary action and does not add a second confirmation. Uninstall uses a separate Windows confirmation dialog and works even if the paid packages are absent or no longer supported.

## Supported versions

| Simulator | Leonardo | Sound source |
| --- | --- | --- |
| MSFS 2024 | Native version **2.1.283** | Immersive Audio **1.0.0**, or optional owner-local Anniversary beta |
| MSFS 2020 | version **2.0.283** | Immersive Audio **1.0.0** |

Restore paid packages to stock before installing. Versions not listed above are unsupported. The Anniversary beta is unavailable for MSFS 2020.

This release makes no new real-source or simulator-runtime acceptance claim for either simulator target. MSFS 2020 may additionally require the generated package to load after Leonardo.

## Safety model

The application completes and validates one hidden candidate before removing prior generated output. It publishes one canonical package:

```text
maddog-ia-sound-fix
```

The reserved namespace also includes historical numeric/development names and the two earlier compatibility names. Matching entries are wholly tool-owned regardless of marker, target, entry type, or contents. Links and junctions are removed as entries without following or modifying their targets. Differently named entries and both paid source packages are ignored.

There is no rollback after deletion begins. Success and Failure retain selectable, copyable details, including definitely completed removals and recovery guidance. Keep the application, simulator, and Leonardo Manager closed until the operation finishes.

Do not download or share a generated sound package. Every user must own the required add-ons and build locally from their own installations. Never share paid or generated XML, PCK, BNK, WEM, WAV, glTF, `.bin`, manifest, layout, package, or extracted-bank files.

## Privacy and Windows behavior

Maddog Sound Fix has no telemetry, network client, updater, settings store, or persisted Community/beta path preference. It is single-instance and prevents ordinary window closure while installation or removal is active.

The executable is unsigned and may show a SmartScreen warning. The published SHA-256 confirms that your download matches the published release; it does not independently authenticate the publisher. Do not disable Windows security features.

## Sound coverage

The maintained mix uses IA for compatible machinery, engine, wind, warning, and control families while retaining selected Leonardo behavior where required. See [Finnisher's script and Maddog Sound Fix](COMPARISON.md) for the practical differences. Thanks to @finnisher and @DrPredrag for the community work that made this project possible.

## License

Maddog Sound Fix is distributed under the MIT License. The packaged README contains the complete project license and all required pinned third-party notices.
