# Community script or Maddog Sound Fix?

Both options are based on the same excellent community work by @finnisher. Both require you to own Leonardo Fly the Maddog X and the Immersive Audio sound pack.

## The short version

**Finnisher’s script** is a set of instructions for manually converting the Maddog sound setup.

**Maddog Sound Fix** is a Windows tool that does the complicated work for you, checks that the files are supported, and creates a separate add-on that is easy to remove.

| | Finnisher’s script | Maddog Sound Fix |
| --- | --- | --- |
| Setup | Follow and apply conversion instructions | Download the tool and paste the commands from the guide |
| Your original add-ons | Converted files are copied into the aircraft package | Leonardo and IA are only read; they are never changed |
| Result | A converted aircraft sound setup | A separate `maddog-sound-compat-...` Community folder |
| Removing it | Restore backups or reinstall the changed package | Delete the one generated Community folder |
| Sound choices | Uses the script’s conversion choices | Uses a tested IA-first baseline; advanced users can change complete sound groups |
| Leonardo crew and callouts | Some are recreated with extra WAV files | Original Leonardo crew-pack and PNF systems remain in use |
| Leonardo-only features | Added back through selected script operations | Kept directly from Leonardo when IA has no complete replacement |
| Safety checks | The user must apply everything correctly | The tool checks versions, source files, sound links, generated files, and repeatable output |
| Paid audio in the download | No | No |

## Why use the tool?

### It does not change either paid add-on

The tool reads your Leonardo and IA packages and builds a new add-on somewhere else. If you do not like the result, close the simulator and remove that generated folder.

### It keeps the best parts of both packs

The baseline prefers IA sounds where a complete replacement exists and has been tested. Leonardo remains responsible for things IA does not fully replace, such as the selected crew pack, pilot-not-flying (PNF) callouts, and any missing warning or aircraft-specific sound.

### It avoids mixing one machinery sequence

Startup, running, and shutdown sounds for one system must come from the same sound pack. Testing showed that mixing Leonardo startup with IA running could replay or overlap sounds when changing camera views. The tool groups those sounds together so users cannot accidentally create that combination.

### It checks before building

The tool stops if the installed packages are unsupported or important source files have been changed. It also checks the generated sound package before making it available to install.

## Important: restore stock packages first

If you previously used Finnisher’s script—or another sound conversion—you must restore current stock Leonardo and Immersive Audio packages before using Maddog Sound Fix.

Use the official installer/updater or reinstall the affected add-on. Do not try to make validation pass by editing hashes or guessing which individual files need replacing. The tool is supposed to stop rather than build from an already converted installation.

Normal Leonardo Manager crew changes and supported GSX file-list updates are handled separately; replaced sound or model files are not.

## What will the first release sound like?

The planned baseline uses:

- IA for the major complete sound groups that pass final testing;
- Leonardo for Manager-selected crew voices and PNF callouts;
- Leonardo for genuinely unique aircraft sounds;
- Leonardo as a fallback where an IA sound is missing or does not work.

Native MSFS 2024 is being tested locally. MSFS 2020 can be built from supported files, but the maintainer does not own that simulator, so it remains unverified and may need the generated package ordered after Leonardo.

## Which option should I choose?

Use **Finnisher’s script** if you enjoy manual experimentation and want direct control over its individual conversion steps.

Use **Maddog Sound Fix** if you want an automated, checked, removable package that leaves the paid add-ons untouched.

Finnisher’s work is the foundation for this project and continues to provide important placement, behavior, and testing evidence. Maddog Sound Fix packages that knowledge into a safer repeatable process rather than replacing the community contribution.
