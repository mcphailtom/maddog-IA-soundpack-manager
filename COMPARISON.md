# Finnisher’s script and Maddog Sound Fix

Finnisher’s community script is the starting point for this project and remains valuable evidence about IA placement, model corrections, missing Anniversary bindings, and in-simulator behavior. Maddog Sound Fix automates a different installation approach rather than claiming that work was wrong.

## Key differences

| | Finnisher’s community script | Maddog Sound Fix |
| --- | --- | --- |
| Starting point | Starts from the wholesale IA sound setup and adapts it to the Maddog | Starts from Leonardo’s complete setup and moves complete compatible behaviors to IA |
| Installation | Produces files that are copied into or replace files under the aircraft package | Builds a separate removable Community package |
| Original add-ons | Requires careful backup/restoration when files have been replaced | Treats both paid packages as read-only and refuses changed supported inputs |
| Sound ownership | Uses the IA-oriented converted document | Gives each complete coupled sound sequence to one provider, avoiding mixed start/run/stop behavior |
| Leonardo-only behavior | Adds selected Anniversary behavior and recreates some calls using external WAV files | Keeps Leonardo PNF, Manager-selected crew, and proven unique behavior from their original banks |
| IA warning gaps | Uses IA XML wholesale; definitions with broken/missing IA bank routes remain silent | Can retain a Leonardo fallback or use a validated recovered IA route for an individual missing warning |
| Anniversary controls | Grafts newer controls onto generic IA switch Events | Uses the same evidence, but validates each trigger and keeps the decision in the maintained behavior catalog |
| Guard sounds | Includes optional directional guard choreography in later operations | Initial baseline keeps exact generic IA guard clicks; richer choreography remains optional pending testing |
| APU, hydraulics, rack fan | IA running media naturally includes startup before its steady loop | Treats each as one complete provider-owned sequence; never layers Leonardo startup over the IA intro |
| Cockpit door | Adds IA open/close recordings and adjusted motion timing plus optional latch behavior | Uses the purchased IA open/close recordings with IA’s original trigger timing and no synthetic latch layer |
| Model changes | Uses a prepared exhaust-locator model patch | Adds only the two approved locators when selected sounds actually require them |
| Validation | Relies on the user applying scripted operations and regenerating package metadata correctly | Checks exact supported installs, XML selectors, Event collisions, bank differences, model nodes, metadata, hashes, and deterministic output automatically |
| Removal | Restore the modified aircraft files or reinstall the package | Delete the single generated `maddog-sound-compat-...` Community folder |
| Custom choices | Edit or reapply conversion operations | Uses a tested baseline by default; advanced users can list, override, and export complete sound-family choices |
| Download contents | Script/instructions; some optional behavior requires user-provided audio | CLI and README only; no paid or generated audio is distributed |

## Important prerequisite: restore stock first

Maddog Sound Fix validates the paid packages before it builds anything. It must start from supported stock Leonardo and Immersive Audio installations.

If you previously used Finnisher’s script—or any other conversion that replaced Maddog sound XML, banks, model files, or package metadata—restore the current stock packages first. The safest route is to use the official installers/updaters or reinstall the affected package. Do not try to make validation pass by editing hashes or copying individual files until the warning disappears.

A changed GSX/Manager layout can be supported when every file the tool actually uses remains correct, but converted sound/model payloads are intentionally rejected.

## Which should I use?

Finnisher’s script remains useful for understanding and manually experimenting with the conversion. Maddog Sound Fix is intended for users who want an automated, validated, removable result while retaining Leonardo-only behavior and keeping the purchased installations untouched.

The initial release is still completing native MSFS 2024 validation. MSFS 2020 remains runtime-unverified and may require package ordering after Leonardo.
