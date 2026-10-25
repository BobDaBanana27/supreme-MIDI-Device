# MetroKey 25

MetroKey 25 is a compact two-octave USB MIDI keyboard designed around a clear constraint: a physical 25-key controller that can connect to a computer and play MIDI instruments in a DAW, with a parts-only DIY build target below US$30. The first revision uses a USB-C RP2040 module, a 25-key dual-contact switch bed for velocity, octave controls, and a mode button. Wireless, battery, and touch-strip features are documented as later options so the first build stays buildable and budget-aware.

## Concept views

These original drawings show the proposed layout and assembly. They are design illustrations, not photographs of a fabricated prototype.

![MetroKey 25 top-view concept](assets/top_view_concept.svg)

![MetroKey 25 exploded concept](assets/exploded_concept.svg)

The current cumulative FreeCAD model is shown below; use the [CAD progress chunks](chunks/INDEX.md) to see the design evolve file by file.

![MetroKey 25 FreeCAD assembly drawing](hardware/CAD/MetroKey25/drawings/Assembly_Drawing.svg)
The corrected keybed detail and the shared KiCad/FreeCAD coordinate frame are shown below.

![Dimensioned keybed with black keys toward the rear controls](hardware/CAD/MetroKey25/drawings/Dimensioned_Keybed.svg)

![Shared KiCad and FreeCAD mechanical envelope](hardware/CAD/MetroKey25/drawings/KiCad_FreeCAD_Envelope.svg)

The black-key placement was checked against this real 25-key controller layout: [OMNITRONIC KEY-25 MIDI Controller](https://www.steinigke.de/en/mpn11045074-omnitronic-key-25-midi-controller.html).

## Start here

- [Design scope and decisions](DECISIONS.md)
- [Research and platform trade study](RESEARCH.md)
- [Estimated parts list](BOM.csv)
- [Mechanical design](MECHANICAL_DESIGN.md)
- [Electrical design and schematic](ELECTRICAL_DESIGN.md)
- [Keybed and velocity matrix](KEYBED_AND_MATRIX.md)
- [USB MIDI and DAW target](USB_MIDI.md)
- [Controls and status behavior](CONTROLS.md)
- [Power and later wireless options](POWER_AND_BUDGET.md)
- [Verification plan](TEST_PLAN.md)
- [10 substantial hardware-design packages with CAD files and previews](chunks/INDEX.md)
- [KiCad and FreeCAD project entrypoints](hardware/PROJECT_INDEX.md)
- [FreeCAD assembly and exports](hardware/CAD/MetroKey25/README.md)
- [Work log and artifact index](WORK_LOG.md)

## What the first revision includes

- 25 note keys, mapped from MIDI note 48 through 72 (C3 to C5).
- Two sequential switch contacts per key; the interval between contacts is the proposed velocity input.
- A five-row by ten-column scan matrix with one isolation diode per contact.
- An RP2040-Zero module with USB-C and native USB device support.
- Three controls: octave down, octave up, and mode/function.
- USB bus power and a parts-only build estimate of US$28.79.

The USB-MIDI device behavior still needs firmware, and the tactile-switch velocity mechanism needs a physical calibration prototype. This repository contains the hardware design pack, not firmware or a finished device. The current cost target excludes labor, tools, taxes, shipping, and commercial margin; it is not a US$30 retail-price claim.

## Schematic and visual design

- [Electrical schematic drawing](hardware/MetroKey25_Electrical_Schematic.svg)
- [Editable KiCad project and native schematic](hardware/KiCad/MetroKey25/README.md)
- [Logisim key-scan demonstration](hardware/MetroKey25_Keyscan_Demo.circ)
- [System architecture drawing](assets/system_architecture.svg)
- [Key-to-matrix assignment](hardware/key_matrix_map.csv)

## Progress evidence

The 10 larger work packages show cumulative FreeCAD work on the enclosure, 25-key mechanism, switch placement, controller module, manufacturing exports, and drawings. Read the [stage-by-stage progression](chunks/PROGRESSION.md) for the exact additions and files. They include editable CAD snapshots and distinct visual previews. No elapsed hours or physical build photos are claimed; photograph the actual PCB, keys, or assembly when a hardware prototype exists.


