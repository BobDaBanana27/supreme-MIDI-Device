# Controls and status behavior

Revision A has three physical buttons:

- OCT− shifts the playable range down one octave.
- OCT+ shifts the playable range up one octave.
- MODE/FN cycles the planned performance modes. A short press changes the selected mode; a held press while pressing OCT− or OCT+ is reserved for choosing scale root or chord voicing.

The first firmware target is plain chromatic playing plus octave shift. Scale lock and chord mode are planned behaviors, not working features until firmware implements and tests them. The onboard RGB LED can show the selected mode and MIDI connection state.

The original capacitive strip is omitted from Revision A. A future touch-strip revision should map its modes to pitch bend, modulation CC 1, or filter cutoff CC 74 and should measure interference from the USB cable, key matrix, and hand position before choosing a sensor.
