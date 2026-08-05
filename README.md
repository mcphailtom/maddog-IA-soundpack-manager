# Maddog IA Soundpack Manager

A small Windows tool for building a separate Maddog sound add-on from Leonardo Fly the Maddog X and Immersive Audio packages you already own.

It does not include either paid add-on and does not edit them. The generated package stays on your PC and can be removed by deleting its one Community folder.

## Restore stock packages first

The tool must start from supported stock Leonardo and Immersive Audio installations. If you previously used @finnisher's script or another conversion that replaced Maddog sound XML, banks, model files, or package metadata, restore the current stock packages before running this tool. The safest route is the official installer/updater or reinstalling the affected add-on. Validation is designed to fail rather than build from modified paid files.

## Download

This repository is only the public download and release-notes home. When the first release is ready, get the ZIP from **Releases** and follow the included `README.md`.

The ZIP will contain only:

- `maddog-sound-fix.exe`
- `README.md`

Do not download or share generated sound packages. Every user must own both add-ons and build locally from their own installations.

## What it does

- Checks that your installed Leonardo and Immersive Audio packages match supported public releases.
- Uses a baseline based on @finnisher’s community script.
- Starts with Leonardo’s complete setup, preserving Leonardo-only and selected crew-pack sounds.
- Builds a separate removable Community package instead of changing either original add-on.
- Uses Immersive Audio for the supported replacement sounds by default, with optional command-line overrides.

See [Finnisher's script and Maddog Sound Fix](COMPARISON.md) for the practical differences, what remains Leonardo-owned, and why stock packages are required.

## Current status

The first release is still being validated in native MSFS 2024. MSFS 2020 output can be built, but the maintainer does not own that simulator, so it remains runtime-unverified and may need its package ordered after Leonardo.

The development source remains private while validation is moving quickly. That may be revisited after the initial release has settled. This public repository is not a source mirror.

Thanks to @finnisher and @DrPredrag for the community work that made this possible.

## License

Maddog Sound Fix is distributed under the MIT License. The release README contains the full project and third-party notices.
