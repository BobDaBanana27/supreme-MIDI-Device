# Verification plan

No physical prototype or firmware is included yet. Use these checks when those parts exist.

## Mechanical

- Measure the assembled enclosure and confirm it fits the stated 320 × 120 × 18 mm target or update the target.
- Check every key for free return, neighboring-key clearance, switch overtravel, and reliable contact order.
- Weigh the finished device and record the actual printed-part and hardware cost.
- Open and close the case repeatedly; inspect hinge rails, standoffs, and cable strain relief.

## Electrical

- Confirm no short between 5 V, 3.3 V, and ground before plugging into a host.
- Check diode orientation and continuity for all 50 contact positions.
- Verify that each row scan reads the expected columns and that multi-key combinations do not ghost.
- Measure USB current at idle, during key activity, and at each status LED brightness.
- Confirm USB-C data works with both a USB-A-to-C and a C-to-C data cable.

## Key and velocity

- Exercise every note, first and second contact, repeated soft and hard presses, and simultaneous notes.
- Verify each of the 25 keys maps to the intended MIDI note number 48–72.
- Capture contact timing and report per-key repeatability before selecting velocity thresholds.
- Check switch bounce, missed contacts, double triggers, stuck notes, and release behavior.

## USB MIDI and DAW

- Confirm the device enumerates as a USB MIDI input after firmware is added.
- In a MIDI monitor or DAW, verify Note On, note number, velocity, and Note Off for all keys.
- Test octave buttons and mode behavior after firmware is added.
- Test reconnect, reset, suspend/resume, and unplug while a note is held.
- Record host operating system, DAW version, cable, and results.

## Budget

- Replace every planning estimate in BOM.csv with a dated cart or fabrication quote.
- Include shipping, taxes, failed prints, replacement parts, and labor separately from the parts-only target.
- Recalculate the cost before claiming the device meets the US$30 parts budget.
