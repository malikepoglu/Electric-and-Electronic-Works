# 7447 vs 7448 BCD to 7-Segment Decoders | Proteus ISIS

A Proteus ISIS example by **Mehmet Ali Kepoglu**, accompanying the [7447 vs 7448 BCD to 7-Segment Decoders | Proteus ISIS](https://www.youtube.com/watch?v=Mk2JOF9l-y0).

The same four input controls drive two decoder/display combinations:

- **7447 → common-anode display:** active-low segment outputs; the display common connects to +5 V.
- **7448 → common-cathode display:** active-high segment outputs; the display common connects to GND.

A=1, B=2, C=4 and D=8. Four-bit codes in the table are written **DCBA**, from the most significant bit to the least significant bit. The recording uses manual input controls, rather than an automatic counter.

## Files

- [`7447_And_7448_BCD_To_7_Segment_Display_Decoder.pdsprj`](7447_And_7448_BCD_To_7_Segment_Display_Decoder.pdsprj) — the author's original project, copied without changing its bytes.
- [`truth-table.csv`](truth-table.csv) — all 16 expected input patterns, stable observations from the video, and separate fields for future native test results.
- [`validation.json`](validation.json) — static archive integrity checks; native simulator tests remain `NOT_TESTED`.
- [`SHA256SUMS`](SHA256SUMS) — checksums for the project, table and this README.

The project archive contains `PROJECT.XML`, `ROOT.CDB`, `ROOT.DSN` and `SCRIPTS/PWRRAILS.DAT`. Separate personal workspace files, backups, simulator installers and third-party library bundles are excluded.

## Open and run

1. Download and extract the repository ZIP, or clone the repository.
2. In **Proteus Professional**, choose **Open Project** and select the `.pdsprj` file in this folder. Use a working copy if you intend to save changes.
3. Open the schematic in ISIS. Confirm that the two decoders, common-anode/common-cathode displays, four input controls and fourteen 220 Ω resistors appear.
4. Start the simulation and inspect its diagnostics. Resolve unavailable model or supply problems before comparing states.
5. Set each DCBA input combination, let the display settle, and compare both displays with `truth-table.csv`. A closed input button connects its line to GND; in the recorded model an open button is interpreted as HIGH.
6. Stop the simulation when finished. Save changes only to your working copy.

The recording and project belong to the **Proteus 8 family**. The project metadata records raw release/file-version identifiers `804` and `805`; a minimum compatible Proteus release has not been established. This package has received static file checks, but has **not** been opened or simulated in the current publication environment.

The design references the Proteus models `74XX47.MDF`, `74XX48.MDF`, `7SEGCOMA.MDF`, `7SEGCOMK.MDF` and `ITFMOD.MDF`. Use a licensed Proteus installation providing the required standard models. Their availability and compatibility in a particular installation remain to be checked.

## Reading the table

- Decimal inputs **0–9** are valid single-digit BCD and display decimal digits.
- Inputs **10–15** are outside valid BCD. This decoder family defines additional segment patterns; they are **not hexadecimal A–F characters**. Input 15 produces a blank display under the normal control conditions.
- The open shapes of **6** and **9** are intentional for this decoder family: segment a is off for 6, and segment d is off for 9.
- Segment names are a=top, b=upper right, c=lower right, d=bottom, e=lower left, f=upper left and g=middle.
- `expected_7447_abcdefg` and `expected_7448_abcdefg` contain seven logic levels in that exact segment order. A lit segment corresponds to LOW for 7447 and HIGH for 7448. For 7447, a 1 represents the HIGH/open-collector-off condition of the segment node, not an actively driven HIGH source.
- `none` means all segments are off. Empty native-observation fields with `not_tested` mean no new native simulator test has been performed; they are not zero values or passed results.

Stable states in the video show matching lit segments on both displays for all 16 input codes. Those observations are distinct from a new simulator run. The expected patterns follow the relevant TI decoder-family function tables; they do not assign an unverified physical manufacturer or device suffix to the generic Proteus symbols.

## Simulation scope

The schematic uses fourteen 220 Ω segment resistors. The display models record `VF=1.5V` and `ION=10mA`; these are model parameters, not measured segment currents. The source contains VCC/GND pin definitions for both decoders, while the compiled hidden supply bindings have not been independently validated by a fresh run.

The recording demonstrates normal code decoding. LT, RBI and BI/RBO are held in their normal HIGH conditions; lamp test, blanking and ripple-blanking operation are not demonstrated. The 7447 and 7448 output circuits have different current-driving characteristics. A physical build requires defined input levels, the exact device/display ratings, appropriate supply connections and an independently checked current-limiting design. An open simulated TTL input should not be treated as a universal physical HIGH source.

For a future native verification, record the actual Proteus version, open an unchanged-source working copy, inspect diagnostics and supply networks, run all 16 table rows, then save and reopen the tested copy. Populate native results only from observed simulator states. Static archive/model checks cannot establish these runtime results.

## Related material

- [Video](https://www.youtube.com/watch?v=Mk2JOF9l-y0)
- [TI 7447 and 7448 BCD-to-Seven-Segment Decoders/Drivers, SDLS111](https://www.ti.com/lit/ds/symlink/sn7447a.pdf), covering both decoder types; particularly the character and function tables on pages 3–4
- [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc)
- [Project index](../README.md)

## Display reference examples

The video and original project use generic Proteus common-anode and common-cathode display models, rather than an identified physical display part. These manufacturer datasheets illustrate the two connection types; they do not identify the simulated devices or establish hardware compatibility with this circuit.

- [Kingbright SA56-11EWA — common-anode seven-segment display](https://www.kingbrightusa.com/images/catalog/SPEC/sa56-11ewa.pdf)
- [Kingbright SC56-11EWA — common-cathode seven-segment display](https://www.kingbrightusa.com/images/catalog/spec/sc56-11ewa.pdf)

For the simulated common-anode arrangement, the display common connects to +5 V; for the common-cathode arrangement, it connects to GND. Refer to the exact physical part's pinout and ratings when moving beyond the simulation.
