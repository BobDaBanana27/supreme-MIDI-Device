# MetroKey 25

MetroKey 25 is a compact two-octave USB MIDI keyboard designed around a clear constraint: a physical 25-key controller that can connect to a computer and play MIDI instruments in a DAW, with a parts-only DIY build target below US$30. The first revision uses a USB-C RP2040 module, a 25-key dual-contact switch bed for velocity, octave controls, and a mode button. Wireless, battery, and touch-strip features are documented as later options so the first build stays buildable and budget-aware.

## Start here

- [Estimated parts list](BOM.csv)
- [Mechanical design](MECHANICAL_DESIGN.md)
- [Electrical design and schematic](ELECTRICAL_DESIGN.md)
- [Keybed and velocity](KEYBED_AND_MATRIX.md)
- [USB MIDI and DAW target](USB_MIDI.md)
- [Controls and status behavior](CONTROLS.md)
- [Power and later wireless options](POWER_AND_BUDGET.md)
- [Verification plan](TEST_PLAN.md)
- [10 substantial hardware-design packages with CAD files and previews](chunks/INDEX.md)
- [KiCad and FreeCAD project entrypoints](hardware/PROJECT_INDEX.md)
- [FreeCAD assembly and exports](hardware/CAD/MetroKey25/README.md)
- [Work log and artifact index](WORK_LOG.md)

## What is included

- 25 note keys, mapped from MIDI note 48 through 72 (C3 to C5).
- Two sequential switch contacts per key; the interval between contacts is the proposed velocity input.
- A five-row by ten-column scan matrix with one isolation diode per contact.
- An RP2040-Zero module with USB-C and native USB device support.
- Three controls: octave down, octave up, and mode/function.
- USB bus power and a parts-only build estimate of US$28.79.

<img width="1150" height="364" alt="Screenshot 2026-10-25 170304" src="https://github.com/user-attachments/assets/33f0234c-794e-465e-81bb-76220681faca" />
<img width="1077" height="582" alt="Screenshot 2026-10-25 171423" src="https://github.com/user-attachments/assets/e964c717-4eb9-4ae9-8a60-5fa336db220b" />


The USB-MIDI device behavior still needs firmware, and the tactile-switch velocity mechanism needs a physical calibration prototype. This repository contains the hardware design pack, not firmware or a finished device. The current cost target excludes labor, tools, taxes, shipping, and commercial margin; it is not a US$30 retail-price claim.

## Schematic and visual design

- [Editable KiCad project and native schematic](hardware/KiCad/MetroKey25/README.md)
- [Logisim key-scan demonstration](hardware/MetroKey25_Keyscan_Demo.circ)
- [Key-to-matrix assignment](hardware/key_matrix_map.csv)



