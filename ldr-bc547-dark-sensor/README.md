# LDR Dark Sensor with BC547 | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [LDR Dark Sensor with BC547 | Proteus ISIS](https://www.youtube.com/watch?v=sDMib8qdAAg).

See how an LDR and a BC547 NPN transistor control an LED in a Proteus ISIS simulation.

The 100 kΩ resistor and LDR form the transistor's base-bias network. As illumination increases, the LDR resistance decreases and the base drive falls, so the green LED dims and turns off. Reducing the illumination turns the LED on again.

Circuit shown:
- 9 V DC supply
- BC547 NPN transistor
- LDR (light-dependent resistor / photoresistor)
- 100 kΩ bias resistor
- Green LED with a 470 Ω series resistor

The simulated light source is adjusted to demonstrate the LED response to changing illumination. This is a dark-sensing circuit example, not a calibrated light meter or a verified hardware build.

## Files

- [`Torch_LDR_Led.pdsprj`](Torch_LDR_Led.pdsprj) — the author's original native project, copied without changing its bytes.
- [`light-response-observations.csv`](light-response-observations.csv) — expected behavior and observations from the reviewed video, with separate fields for future native tests.
- [`validation.json`](validation.json) — static archive checks and the exact source checksum.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the native project, README, CSV and validation record.

Personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download the repository using **Code → Download ZIP** and extract it, or clone it. Keep this folder's files together.
2. In a licensed **Proteus Professional** installation, choose **Open Project** and select `Torch_LDR_Led.pdsprj`. Use a working copy for any changes.
3. Open the schematic in ISIS and inspect the components, power configuration and model availability before running.
4. Start the simulation and read its diagnostic messages. Resolve missing models or configuration errors before comparing results.
5. Increase and decrease the simulated illumination and compare the LED response with the CSV. For quantitative verification, separately record the LDR settings, base voltage/current, collector-emitter voltage and LED current.
6. Stop the simulation. If you modify the working copy, save it and reopen it before recording a verification result.

## Verification scope

The CSV records qualitative LED responses and the expected direction of resistance/base-drive change. The video does not provide calibrated illuminance, LDR resistance, transistor currents or saturation measurements. The virtual torch is a simulation control, not a physical lux or distance measurement.

The project ZIP CRC and `PROJECT.XML` syntax passed static checks. The archive contains the design entries listed in `validation.json`. Embedded model-file identifiers: `BIPOLAR.MDF`, `LEDA.MDF`.

The recording belongs to the Proteus 8 family. Exact minimum-release compatibility has not been established. **This publication has not opened, run, saved or reopened the project in Proteus.** The CSV's empty native observation fields and `NOT_TESTED` values are deliberate; they do not mean a simulator test passed. Static identifiers cannot verify every connection, available model, hidden supply or runtime diagnostic.

For a new native test, record the actual Proteus version, work from an unchanged-source copy, read the diagnostics, perform the listed cases, and fill the native observation columns only with observed results. These simulation examples do not establish a physical hardware build or measured propagation delay. Physical use requires the exact selected component's pinout, supply and current ratings to be checked separately.

## References and related material

- [onsemi BC546/BC547/BC548/BC549/BC550 NPN transistor family](https://www.onsemi.com/pdf/datasheet/bc550-d.pdf)

Manufacturer documents are function or component-family references. They do not identify an unverified manufacturer, exact device suffix or physical display in the simulation.

- [Related lesson — BC547 voltage, current and LED dimming](https://www.youtube.com/watch?v=c5b6sTHSjEc)
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
