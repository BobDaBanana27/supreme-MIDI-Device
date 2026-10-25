# Power and budget

## Revision A

Revision A is powered from USB. The RP2040-Zero module includes the USB-C connector and a 3.3 V regulator, so the first carrier board does not need a LiPo cell, charging IC, battery protection circuit, or battery switch. The initial electrical target is to remain below the default bus-powered USB current allowance; measure actual draw with all keys idle, active, and the RGB LED at full brightness before host compatibility is claimed.

## Parts budget

The [BOM.csv](BOM.csv) totals US$28.79 as a planning estimate for a small DIY batch. Only the controller module price is tied to a current public listing. Remaining amounts are budget placeholders and need supplier or fabrication quotes. Labor, tools, shipping, taxes, paid printing, and commercial margin are excluded.

## Why the supplied battery target moved

A 500 mAh label does not prove 10–12 hours of use. That claim needs measured average current, usable battery capacity, radio duty cycle, charging cutoff, and an agreed playing pattern. Revision A has no battery, so it makes no runtime claim.

## Future wireless revision

A later ESP32-S3 revision could add BLE MIDI, a battery, and a capacitive strip. Before approving that path, build a radio prototype, measure active BLE current, evaluate touch-sensor noise, determine battery protection and charging, and produce an updated costed BOM. Keep BLE support and a 10–12 hour runtime as unverified future requirements until those measurements exist.
