# Electrical & Electronic Systems Works

Electrical and electronic simulation projects and supporting notes by **Mehmet Ali Kepoglu**. Each video has its own directory directly in the repository root, containing the author's original Proteus project and its documentation.

Watch the [Electrical & Electronic Systems playlist](https://www.youtube.com/playlist?list=PLxVfiwCv5VsTB3PJYlwFLmNxNQshJskvc). The collection currently covers digital logic, display decoders and counters, and basic transistor circuits. Future topics may include electrical control panels, contactors, single-phase and three-phase circuits, motor control and start-stop circuits.

## Projects

| Playlist position | Video | Native project and documentation |
| --- | --- | --- |
| 1 | [4026 Decimal Counter: 000–999 \| Proteus ISIS](https://www.youtube.com/watch?v=LptkMoCDSbk) | [Project and notes](4026-three-digit-decimal-counter) |
| 2 | [7447 vs 7448 BCD to 7-Segment Decoders \| Proteus ISIS](https://www.youtube.com/watch?v=Mk2JOF9l-y0) | [Project and notes](7447-7448-bcd-to-seven-segment-decoders) |
| 3 | [7-Segment Displays: Common Anode vs Common Cathode \| Proteus ISIS](https://www.youtube.com/watch?v=60n690-pR4w) | [Project and notes](seven-segment-common-anode-common-cathode) |
| 4 | [XNOR Logic Gate: Truth Table & Equivalent Circuits \| Proteus ISIS](https://www.youtube.com/watch?v=8SSDGAATYSk) | [Project and notes](xnor-logic-gate) |
| 5 | [XOR Logic Gate: Truth Table & Equivalent Circuits \| Proteus ISIS](https://www.youtube.com/watch?v=wpsi6ThjZQI) | [Project and notes](xor-logic-gate) |
| 6 | [NOR Logic Gate: Truth Table & Equivalent Circuit \| Proteus ISIS](https://www.youtube.com/watch?v=U60KyiAkisU) | [Project and notes](nor-logic-gate) |
| 7 | [NAND Logic Gate: Truth Table & Equivalent Circuit \| Proteus ISIS](https://www.youtube.com/watch?v=J-uxkaq9AeI) | [Project and notes](nand-logic-gate) |
| 8 | [AND, OR & NOT Logic Gates and Truth Tables \| Proteus ISIS](https://www.youtube.com/watch?v=Hm5eN4HZ_IM) | [Project and notes](and-or-not-logic-gates) |
| 9 | [LDR Dark Sensor with BC547 \| Proteus ISIS](https://www.youtube.com/watch?v=sDMib8qdAAg) | [Project and notes](ldr-bc547-dark-sensor) |
| 10 | [BC547 Circuit: Voltage, Current & LED Dimming \| Proteus ISIS](https://www.youtube.com/watch?v=c5b6sTHSjEc) | [Project and notes](bc547-voltage-current-led-dimming) |

## Using the projects

Use **Code → Download ZIP**, extract the repository, and follow the README inside the video's folder. YouTube descriptions link directly to the corresponding directory. A licensed Proteus installation with the required standard models is needed; simulator installers, personal workspace files and third-party library bundles are not included.

The original native files are preserved without byte changes. Each folder contains a checksum manifest. The documentation separates mathematical expectations, reviewed video observations and static file checks from new native simulator tests. **No fresh Proteus open/run/save/reopen test is claimed for this publication.** Empty native-observation CSV fields and `NOT_TESTED` explicitly identify that limit.

## Known correction

The [XOR example](xor-logic-gate) includes an erratum for the equation below the middle circuit in the recording. Its correct expression is `Q = (A + B) · NOT(A · B)`. The original native source and existing video remain unchanged; a corrected recording is planned. See the example README before using that printed annotation.

## Titles and repository structure

Titles follow [the common title standard](TITLE_STANDARD.md): topic first, actual software name last. Each video keeps a stable directory, native filename and video ID. New videos receive a separate root directory; unrelated projects are not grouped into one download folder.

## Author

Mehmet Ali Kepoglu · [YouTube channel](https://www.youtube.com/@MehmetAliKepoglu)
