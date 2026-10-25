# Research notes

Research checked on 2026-10-25. The first revision favors native USB MIDI and a low-cost controller module. The wireless feature set from the initial brief is retained as a later design path, not part of the under-US$30 core.

## Controller trade study

The Waveshare RP2040-Zero is listed at US$3.99–4.99 and includes a USB-C connector, an RP2040, flash, a 3.3 V regulator, and a board RGB LED. Raspberry Pi documents USB 1.1 host and device support on the RP2040. That makes this module a better first-revision fit than adding a wireless radio and battery to the budget.

The RP2040 does not provide Bluetooth. The USB connector and USB device peripheral alone also do not create a MIDI controller: firmware must expose a USB MIDI device interface before a DAW can enumerate it as a MIDI source.

## MIDI behavior

The MIDI Association describes Note On as a note number plus velocity, followed by Note Off when the key is released. Its USB MIDI and BLE MIDI pages describe the transport specifications. Revision A targets USB MIDI 1.0 class behavior. BLE MIDI is a later option only.

## Why ESP32-S3 is deferred

Espressif documents USB full-speed OTG, BLE support, and 14 capacitive-sensing GPIOs on the ESP32-S3 family. The same hardware guidance warns that the S3 touch sensor has not passed the conducted-susceptibility test and has limited application scenarios. That is a reason to prototype and measure a touch strip before making it a product claim.

The ESP32-S3 is a credible future wireless controller, but the current v1 budget is already tight. A LiPo, charger/protection, radio module, capacitive sensor layout, and battery test would displace the keybed budget. Battery life cannot be inferred from the 500 mAh label; it needs a measured current profile and a defined playing pattern.

## Cost evidence and limits

The controller module has a current listed retail price range linked below. Switches, diodes, PCB, prints, springs, and small hardware use planning estimates in [BOM.csv](BOM.csv), not supplier quotations. Obtain real cart and fabrication quotes before ordering.

The US$28.79 figure is a parts-only DIY target for a small batch. It excludes labor, tools, shipping, taxes, returns, quality yield, certification, enclosure tooling, and business margin. It is not evidence that a finished retail instrument can sell for US$30.

## Primary references

- [Waveshare RP2040-Zero product page](https://www.waveshare.com/rp2040-zero.htm) — current listed price range, USB-C, module features.
- [Waveshare RP2040-Zero wiki](https://www.waveshare.com/wiki/RP2040-Zero) — board documentation.
- [Raspberry Pi RP2040 datasheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf) — USB 1.1 device/host peripheral and chip specifications.
- [MIDI 1.0 message summary](https://midi.org/summary-of-midi-1-0-messages) — Note On, Note Off, note number, and velocity.
- [USB MIDI 1.0](https://midi.org/usb-midi-1-0) — MIDI Association transport specification.
- [BLE MIDI](https://midi.org/midi-over-bluetooth-low-energy-ble-midi) — MIDI Association BLE transport specification.
- [ESP32-S3 hardware design guidelines](https://docs.espressif.com/projects/esp-hardware-design-guidelines/en/latest/esp32s3/schematic-checklist.html) — USB OTG, capacitive channels, and touch-sensor caveat for a later revision.
- [ESP32-S3 BLE overview](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/api-guides/ble/overview.html) — BLE capability for a later revision.
