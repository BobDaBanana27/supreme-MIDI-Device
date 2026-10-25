# USB MIDI and DAW target

## Host connection

The RP2040-Zero module has a USB-C connector and uses the RP2040 USB device peripheral. Revision A is USB-powered and connects directly to a computer with a data-capable USB-C cable. A charge-only cable will not carry MIDI data.

The finished firmware must enumerate a USB MIDI 1.0 interface and send standard Note On and Note Off messages. The hardware module does not arrive as a MIDI keyboard just because it has a USB port. Firmware and host checks are still required.

## Note map

The default physical range is MIDI note 48 through 72 inclusive, C3 through C5. Each key sends its assigned note number on a configurable MIDI channel. On key-down, send Note On with an estimated velocity from 1 to 127. On release, send Note Off. A future panic action should send All Notes Off if a USB disconnect leaves a note sounding.

DAWs differ in how they label octave numbers. The note number, rather than the displayed octave label, is the acceptance reference.

## FL Studio and other DAWs

The compatibility target is a class-compliant USB MIDI input that appears in a computer's MIDI device list and can be selected as an input in a DAW. The first host check should use FL Studio or another MIDI monitor: connect the controller, select its MIDI input, play a note, confirm the expected note number and velocity, and verify that the note ends on release.

No special DAW plugin or proprietary driver is intended. Exact setup steps and compatibility must be confirmed on the actual operating system and DAW version after firmware exists.

## MIDI references

- [MIDI 1.0 message summary](https://midi.org/summary-of-midi-1-0-messages)
- [USB MIDI 1.0 specification](https://midi.org/usb-midi-1-0)
