# BC547 Circuit: Voltage, Current & LED Dimming | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [BC547 Circuit: Voltage, Current & LED Dimming | Proteus ISIS](https://www.youtube.com/watch?v=c5b6sTHSjEc).

Observe voltage, current and LED brightness in a simple BC547 NPN transistor circuit with resistors and a capacitor, simulated in Proteus ISIS.

The upper button charges the 1000 µF capacitor directly from the 9 V supply. After the button is released, the capacitor supplies the transistor's base through a 10 kΩ resistor. The base current falls; the LED branch current initially stays nearly level, then decreases and the red LED dims as the base drive declines. A 470 Ω resistor limits the LED branch current. The lower button resets the capacitor.

Follow the base-path current, base-emitter voltage, LED voltage and source return current on the virtual meters. The video illustrates how these quantities change over time; it is not a precision timer or a calibrated transistor-characterization test.

The 10 kΩ resistor is in the base/discharge path, not in series with the capacitor's direct charging switch. Displayed 0.00 mA values are rounded meter readings, not proof of an exactly zero current.

## Files

- [`electrolytic_capacitor_transistor_led.pdsprj`](electrolytic_capacitor_transistor_led.pdsprj) — the author's original native project, copied without changing its bytes.
- [`voltage-current-observations.csv`](voltage-current-observations.csv) — expected behavior and observations from the reviewed video, with separate fields for future native tests.
- [`validation.json`](validation.json) — static archive checks and the exact source checksum.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the native project, README, CSV and validation record.

Personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download the repository using **Code → Download ZIP** and extract it, or clone it. Keep this folder's files together.
2. In a licensed **Proteus Professional** installation, choose **Open Project** and select `electrolytic_capacitor_transistor_led.pdsprj`. Use a working copy for any changes.
3. Open the schematic in ISIS and inspect the components, power configuration and model availability before running.
4. Start the simulation and read its diagnostic messages. Resolve missing models or configuration errors before comparing results.
5. Reset with the lower button, charge with the upper button, release it, and observe base-path current, VBE, LED voltage and source return current. Compare phases rather than assuming the media time is simulation time. Do not treat the 10 kΩ × 1000 µF product as a measured LED timeout.
6. Stop the simulation. If you modify the working copy, save it and reopen it before recording a verification result.

## Verification scope

The CSV transcribes selected rounded virtual-meter readings from the reviewed recording. Empty observation cells mean no value was transcribed; they are not zero. A displayed 0.00 mA does not prove an exactly zero current. The lower meter is labelled source return current because the capacitor/base discharge loop does not always pass through it. Media timestamps are not calibrated circuit elapsed times.

The project ZIP CRC and `PROJECT.XML` syntax passed static checks. The archive contains the design entries listed in `validation.json`. Embedded model-file identifiers: `BIPOLAR.MDF`, `DCIMETER.MDF`, `DCVMETER.MDF`, `LEDA.MDF`.

The recording belongs to the Proteus 8 family. Exact minimum-release compatibility has not been established. **This publication has not opened, run, saved or reopened the project in Proteus.** The CSV's empty native observation fields and `NOT_TESTED` values are deliberate; they do not mean a simulator test passed. Static identifiers cannot verify every connection, available model, hidden supply or runtime diagnostic.

For a new native test, record the actual Proteus version, work from an unchanged-source copy, read the diagnostics, perform the listed cases, and fill the native observation columns only with observed results. These simulation examples do not establish a physical hardware build or measured propagation delay. Physical use requires the exact selected component's pinout, supply and current ratings to be checked separately.

## References and related material

- [onsemi BC546/BC547/BC548/BC549/BC550 NPN transistor family](https://www.onsemi.com/pdf/datasheet/bc550-d.pdf)

Manufacturer documents are function or component-family references. They do not identify an unverified manufacturer, exact device suffix or physical display in the simulation.

- [Related lesson — LDR dark sensor with BC547](https://www.youtube.com/watch?v=sDMib8qdAAg)
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)
