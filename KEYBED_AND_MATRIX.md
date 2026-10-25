# Keybed and scan matrix

## Note range

The keybed has 25 chromatic notes, MIDI 48–72 inclusive. The physical sequence begins at C3 and ends at C5. The complete assignment of note and switch contacts to matrix positions is in [hardware/key_matrix_map.csv](hardware/key_matrix_map.csv).

## Two-contact velocity concept

Each key closes contact A first and contact B later in its downstroke. Firmware records both timestamps and maps their interval to an initial velocity. A short interval should result in a higher velocity; a long interval should result in a lower velocity. The transfer curve and thresholds are intentionally left for calibration after a physical key exists.

Use the first contact as the start marker. If the second contact is not detected before the key is released, treat that press as an incomplete press and do not leave a stuck note. Key release should send Note Off exactly once. These are firmware requirements, not implemented behavior.

## 5 × 10 matrix

There are 50 individual contacts: two for every note. Five row outputs and ten column inputs create 50 crosspoints. Each contact gets its own isolation diode to prevent multi-key ghost paths. The column inputs use pull-ups; a selected row is driven low. With this scan polarity, put each diode's anode on the column side and its banded cathode toward the row side.

Notes are packed in blocks of five per row. Each note uses adjacent columns for its A and B contacts. The mapping file is the source of truth for the next schematic and firmware revision.

## Scan and debounce targets

- Scan all five rows often enough to observe a press interval at approximately 1 ms frame resolution.
- Measure and document switch bounce before choosing a debounce rule.
- Support any number of simultaneous notes without ghosting.
- Preserve each contact transition timestamp; do not debounce by adding a large latency to every press.
- Record velocity repeatability across keys and repeated presses before selecting the final response curve.

## Prototype risk

Two cheap tactile switches under one lever are a low-cost experiment, not a piano-grade mechanism. Their travel, actuation force, sound, bounce, and unit variation could make the velocity estimate inconsistent. Replace the switch mechanism if the repeatability checks fail.
