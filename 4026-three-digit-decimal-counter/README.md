# 4026 Decimal Counter: 000–999 | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [4026 Decimal Counter: 000–999 | Proteus ISIS](https://www.youtube.com/watch?v=LptkMoCDSbk).

A three-digit decimal counter simulated in Proteus ISIS using three 4026 counter/display-driver ICs and common-cathode 7-segment displays.

The units stage receives the clock signal. Its carry output clocks the tens stage, and the tens stage clocks the hundreds stage. A shared active-HIGH reset returns all three digits to 000 and holds them there while reset remains HIGH.

The three-digit circuit has a range of 000-999. This recording demonstrates counting, carry transitions and reset; it does not show a complete 000-999 cycle or the 999-to-000 rollover.

This is a simulation example. A physical build needs verified supply and clock settings, display specifications, and suitable segment-current limiting and drive.

## Files

- [`0_999_Decimal_Counter_with_4026_and_7_Segment_Display.pdsprj`](0_999_Decimal_Counter_with_4026_and_7_Segment_Display.pdsprj) — the author's original native project, copied without changing its bytes.
- [`verification-cases.csv`](verification-cases.csv) — expected behavior and observations from the reviewed video, with separate fields for future native tests.
- [`validation.json`](validation.json) — static archive checks and the exact source checksum.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the native project, README, CSV and validation record.

Personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download the repository using **Code → Download ZIP** and extract it, or clone it. Keep this folder's files together.
2. In a licensed **Proteus Professional** installation, choose **Open Project** and select `0_999_Decimal_Counter_with_4026_and_7_Segment_Display.pdsprj`. Use a working copy for any changes.
3. Open the schematic in ISIS and inspect the components, power configuration and model availability before running.
4. Start the simulation and read its diagnostic messages. Resolve missing models or configuration errors before comparing results.
5. Observe units-to-tens and tens-to-hundreds carry. Set reset HIGH and hold it, then release it. Separately test 998 → 999 → 000 in a working copy; that rollover is not shown in the recording.
6. Stop the simulation. If you modify the working copy, save it and reopen it before recording a verification result.

## Verification scope

The CSV distinguishes observed carry/reset events from the unobserved full-range and rollover cases. Its time windows are approximate video media positions. They do not establish clock frequency or calibrated simulation time. The source schematic omits explicit segment-current-limiting resistors; it is not a complete physical LED-driving design.

The project ZIP CRC and `PROJECT.XML` syntax passed static checks. The archive contains the design entries listed in `validation.json`. Embedded model-file identifiers: `4026.MDF`, `7SEGCOMK.MDF`, `ITFMOD.MDF`.

The recording belongs to the Proteus 8 family. Exact minimum-release compatibility has not been established. **This publication has not opened, run, saved or reopened the project in Proteus.** The CSV's empty native observation fields and `NOT_TESTED` values are deliberate; they do not mean a simulator test passed. Static identifiers cannot verify every connection, available model, hidden supply or runtime diagnostic.

For a new native test, record the actual Proteus version, work from an unchanged-source copy, read the diagnostics, perform the listed cases, and fill the native observation columns only with observed results. These simulation examples do not establish a physical hardware build or measured propagation delay. Physical use requires the exact selected component's pinout, supply and current ratings to be checked separately.

## References and related material

- [TI CD4026B/CD4033B — function reference](https://www.ti.com/lit/ds/symlink/cd4026b.pdf)

Manufacturer documents are function or component-family references. They do not identify an unverified manufacturer, exact device suffix or physical display in the simulation.

- [Display basics — common anode vs common cathode](https://www.youtube.com/watch?v=60n690-pR4w)
- [7447 vs 7448 BCD decoders](https://www.youtube.com/watch?v=Mk2JOF9l-y0)
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
