# AND, OR and NOT Logic Gates

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [AND, OR and NOT logic-gates video](https://www.youtube.com/watch?v=Hm5eN4HZ_IM).

Three independent circuits demonstrate the basic Boolean operations:

- **AND:** `Q = A·B`. The output is 1 only when both inputs are 1.
- **OR:** `Q = A+B`. The output is 1 when at least one input is 1, including when both inputs are 1.
- **NOT:** `Q = A̅`. The output is the inverse of the single input A.

Each circuit has its own input controls. The repeated A and B labels do not mean that all three circuits share the same electrical input nets.

## Files

- [`Logic_Gates_AND_OR_NOT.pdsprj`](Logic_Gates_AND_OR_NOT.pdsprj) — the author's original Proteus project, copied without changing its bytes.
- [`truth-table.csv`](truth-table.csv) — expected outputs, stable observations from the video and separate fields for future native test results.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the project and truth-table CSV.

The `.pdsprj` file contains the project design and its embedded project resources. No separate workspace, backup, simulator installer or third-party library bundle is supplied.

## Open and run

1. Download and extract the repository ZIP, or clone the repository.
2. Open **Proteus Professional** and use its **Open Project** command to select `Logic_Gates_AND_OR_NOT.pdsprj` in this folder. Use a working copy if you intend to save changes.
3. Open the schematic in ISIS. Check that the AND, OR and NOT circuits, input controls and output indicators load correctly.
4. Start the simulation and inspect any messages reported by Proteus. If the project fails to load or a model is unavailable, resolve that issue before comparing the logic states.
5. Change the controls for one circuit at a time. Allow the displayed states to settle and compare Q with the corresponding rows in `truth-table.csv`.
6. Stop the simulation when finished. Save changes only to your working copy.

The recording shows the **Proteus 8 family**. The exact minimum compatible release and compatibility with other releases have not been established. This repository does not claim that the project has been reopened or simulated in the current publication environment.

## Truth tables and verification

The CSV contains ten unique cases: four for AND, four for OR and two for NOT. Its `video_observed_Q` values were confirmed from stable states in the video. The blank `native_observed_Q` cells and `not_tested` status mean that a new simulator test has **not yet been performed**; blank cells are not zero outputs.

The CSV lists AND and OR inputs in the conventional order `00, 01, 10, 11`. The video's on-screen tables use `00, 10, 01, 11`; both orders express the same logic.

Static checks can establish file integrity and the presence of embedded project entries. They cannot establish that the simulator opens the design, that all required models are available or that every state produces the expected result.

For a future native verification, record the actual software version, open an unchanged-source working copy, run all ten cases, inspect diagnostics, and save and reopen the tested copy. Populate the CSV's native result fields only with observed test results.

This example demonstrates Boolean behavior in simulation. It does not establish a physical IC part number, pinout, supply voltage or measured propagation delay. Use both the displayed 0/1 values and the settled signal indicators when comparing states; a brief display mismatch during a transition is not a measurement of physical gate delay.

## Related material

- [Video](https://www.youtube.com/watch?v=Hm5eN4HZ_IM)
- [Electricity & Electronics playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
