# XNOR Logic Gate: Truth Table & Equivalent Circuits | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [XNOR Logic Gate: Truth Table & Equivalent Circuits | Proteus ISIS](https://www.youtube.com/watch?v=8SSDGAATYSk).

Compare three equivalent XNOR circuits in Proteus ISIS: a 4077 XNOR gate, XOR followed by NOT, and an AND/NOT/OR implementation. The same A and B inputs drive all three circuits, and their outputs agree for all four input combinations shown.

The XNOR output is HIGH when the inputs are equal:

```text
A B -> Q
0 0 -> 1
0 1 -> 0
1 0 -> 0
1 1 -> 1
```

Boolean expressions:

```text
Q = NOT(A XOR B)
Q = (A AND B) OR ((NOT A) AND (NOT B))
```

Follow the three outputs as the inputs change. This demonstration compares steady-state logic; it does not measure physical propagation delay or verify a hardware build.

## Files

- [`Logic_Gate_XNOR.pdsprj`](Logic_Gate_XNOR.pdsprj) — the author's original native project, copied without changing its bytes.
- [`truth-table.csv`](truth-table.csv) — expected behavior and observations from the reviewed video, with separate fields for future native tests.
- [`validation.json`](validation.json) — static archive checks and the exact source checksum.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the native project, README, CSV and validation record.

Personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download the repository using **Code → Download ZIP** and extract it, or clone it. Keep this folder's files together.
2. In a licensed **Proteus Professional** installation, choose **Open Project** and select `Logic_Gate_XNOR.pdsprj`. Use a working copy for any changes.
3. Open the schematic in ISIS and inspect the components, power configuration and model availability before running.
4. Start the simulation and read its diagnostic messages. Resolve missing models or configuration errors before comparing results.
5. Change A and B through all four combinations. Let all output indicators settle, and compare every circuit with `truth-table.csv`.
6. Stop the simulation. If you modify the working copy, save it and reopen it before recording a verification result.

## Verification scope

The table contains all four unique A/B combinations. Video result columns record settled output states from the reviewed recording; they are distinct from expected mathematical values and from a new simulator test. The source video uses 00, 10, 01, 11 order; the CSV uses 00, 01, 10, 11. Neither ordering changes the function. Sample timestamps are approximate media evidence positions, not physical gate-delay measurements.

The project ZIP CRC and `PROJECT.XML` syntax passed static checks. The archive contains the design entries listed in `validation.json`. Embedded model-file identifiers: `40XOR2.MDF`, `ITFMOD.MDF`.

The recording belongs to the Proteus 8 family. Exact minimum-release compatibility has not been established. **This publication has not opened, run, saved or reopened the project in Proteus.** The CSV's empty native observation fields and `NOT_TESTED` values are deliberate; they do not mean a simulator test passed. Static identifiers cannot verify every connection, available model, hidden supply or runtime diagnostic.

For a new native test, record the actual Proteus version, work from an unchanged-source copy, read the diagnostics, perform the listed cases, and fill the native observation columns only with observed results. These simulation examples do not establish a physical hardware build or measured propagation delay. Physical use requires the exact selected component's pinout, supply and current ratings to be checked separately.

## References and related material

- [TI CD4070B/CD4077B — XOR/XNOR function reference](https://www.ti.com/lit/ds/symlink/cd4077b.pdf)

Manufacturer documents are function or component-family references. They do not identify an unverified manufacturer, exact device suffix or physical display in the simulation.

- [Compare XOR — HIGH when the inputs are different](https://www.youtube.com/watch?v=wpsi6ThjZQI)
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
