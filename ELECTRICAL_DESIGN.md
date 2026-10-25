# Electrical design

## Revision A blocks

The USB-C RP2040-Zero module provides the controller, USB device interface, flash, 3.3 V regulation, and a built-in RGB status LED. The carrier PCB holds the key matrix, per-contact diodes, three control buttons, and the module's connection pads. The keyboard runs from USB bus power; there is no LiPo charger or battery in this revision.

## Signal plan

- GP0–GP4: active-low matrix row outputs.
- GP5–GP14: ten matrix column inputs with pull-ups.
- GP17–GP19: octave down, octave up, and mode/function buttons.
- GP16: onboard WS2812 RGB LED on the controller module; reserve it for status.
- USB D+ and D−: handled by the RP2040 USB peripheral and module routing.

The assignment reserves GP16 because the RP2040-Zero board connects its RGB LED to that pin. Confirm the exact module revision and breakout pads against its schematic before routing the carrier PCB.

## Matrix electrical behavior

Scan one row low at a time and leave the other rows high-impedance or inactive. Read the ten columns through pull-ups. Each key contact sits in series with one diode. For the stated scan polarity, the diode anode faces the column input and the banded cathode faces the row driver.

The drawing [hardware/MetroKey25_Electrical_Schematic.svg](hardware/MetroKey25_Electrical_Schematic.svg) shows the full 5 × 10 matrix and module connection. [hardware/MetroKey25_Keyscan_Demo.circ](hardware/MetroKey25_Keyscan_Demo.circ) is a small Logisim logic demonstration for the row-gating principle; it is not a complete PCB netlist.

An editable native KiCad project is available at [hardware/KiCad/MetroKey25/](hardware/KiCad/MetroKey25/). It includes the switch/diode matrix schematic, module pin map, BOM, matrix CSV, project files, and a starter board outline. The board has no footprints or routing and is not ready for fabrication; see its README for scope and opening instructions.

## USB and ESD

Use a data-capable USB-C port provided by the module. Keep the host data connection on the module's native USB path and add appropriate ESD protection to exposed USB data lines on the carrier if the module layout does not already protect the connector. Follow the module vendor's design and keep the cable entry mechanically supported. Do not connect a battery in Revision A.

## Before PCB release

Confirm module pad pitch and edge access, GP pin assignments, matrix diode polarity, USB connector keep-out, mounting holes, and return-current path. These are release gates; this document is not a routed PCB layout.
