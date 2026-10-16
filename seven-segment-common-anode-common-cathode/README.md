# 7-Segment Displays: Common Anode vs Common Cathode | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [7-Segment Displays: Common Anode vs Common Cathode | Proteus ISIS](https://www.youtube.com/watch?v=60n690-pR4w).

Compare common-anode and common-cathode 7-segment displays in Proteus ISIS. Individual switches control the seven LED segments, showing how each display is powered and how the current paths differ.

The common-anode display has its common connection at +5 V. Closing a segment switch completes that segment's return path to ground. The common-cathode display has its common connection at ground. Closing a segment switch supplies that segment from +5 V.

Each segment has its own 220-ohm series resistor in this 5 V simulation. The switches build up visible segment combinations, including all seven segments lit. This demonstration uses direct segment control; it does not use a BCD decoder, counter or multiplexing.

Physical display pinouts and suitable current-limiting values depend on the selected component and its datasheet.

## Files

- [`Understanding_seven_segment_displays.pdsprj`](Understanding_seven_segment_displays.pdsprj) — the author's original native project, copied without changing its bytes.
- [`segment-observations.csv`](segment-observations.csv) — expected behavior and observations from the reviewed video, with separate fields for future native tests.
- [`validation.json`](validation.json) — static archive checks and the exact source checksum.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the native project, README, CSV and validation record.

Personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download the repository using **Code → Download ZIP** and extract it, or clone it. Keep this folder's files together.
2. In a licensed **Proteus Professional** installation, choose **Open Project** and select `Understanding_seven_segment_displays.pdsprj`. Use a working copy for any changes.
3. Open the schematic in ISIS and inspect the components, power configuration and model availability before running.
4. Start the simulation and read its diagnostic messages. Resolve missing models or configuration errors before comparing results.
5. Operate the individual switches for each display. Compare the cumulative lit-segment sets with `segment-observations.csv`, then test each segment separately in your working copy if needed.
6. Stop the simulation. If you modify the working copy, save it and reopen it before recording a verification result.

## Verification scope

The CSV records fourteen cumulative segment sets: seven for each display. It does not claim fourteen isolated-segment tests, every possible segment combination or decimal decoding. The timestamps locate settled video examples. The two physical display references below illustrate connection types; they do not identify the generic Proteus devices.

The project ZIP CRC and `PROJECT.XML` syntax passed static checks. The archive contains the design entries listed in `validation.json`. Embedded model-file identifiers: `74XX47.MDF`, `74XX48.MDF`, `7SEGCOMA.MDF`, `7SEGCOMK.MDF`.

The recording belongs to the Proteus 8 family. Exact minimum-release compatibility has not been established. **This publication has not opened, run, saved or reopened the project in Proteus.** The CSV's empty native observation fields and `NOT_TESTED` values are deliberate; they do not mean a simulator test passed. Static identifiers cannot verify every connection, available model, hidden supply or runtime diagnostic.

For a new native test, record the actual Proteus version, work from an unchanged-source copy, read the diagnostics, perform the listed cases, and fill the native observation columns only with observed results. These simulation examples do not establish a physical hardware build or measured propagation delay. Physical use requires the exact selected component's pinout, supply and current ratings to be checked separately.

## References and related material

- [Kingbright SA56-11EWA — common-anode display example](https://www.kingbrightusa.com/images/catalog/SPEC/sa56-11ewa.pdf)
- [Kingbright SC56-11EWA — common-cathode display example](https://www.kingbrightusa.com/images/catalog/spec/sc56-11ewa.pdf)

Manufacturer documents are function or component-family references. They do not identify an unverified manufacturer, exact device suffix or physical display in the simulation.

- [Related lesson — 7447 vs 7448 BCD decoders](https://www.youtube.com/watch?v=Mk2JOF9l-y0)
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
