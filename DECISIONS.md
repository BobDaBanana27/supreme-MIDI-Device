# Scope and decisions

## Product objective

Build a small, affordable 25-key MIDI piano controller that connects directly to a computer and can drive software instruments in a DAW such as FL Studio. Its primary success criteria are a playable two-octave keybed, dependable USB MIDI, and a realistic parts-only budget below US$30.

## Revision A: MetroKey 25 USB Core

Revision A is a wired, USB-powered design. It uses a low-cost RP2040 module with USB-C, a 25-key physical keyboard, two staged contact closures per key for a velocity estimate, octave controls, and one mode/function button. Its estimated parts total is US$28.79 before labor, tools, shipping, tax, and commercial margin.

The 25-key span is C3 through C5, MIDI notes 48 through 72. The MIDI note numbers are the stable definition because DAWs do not all use the same octave-name convention for middle C.

## Features deferred from the supplied concept

Bluetooth LE MIDI, a rechargeable battery, and the capacitive expression strip are deferred. They add radio, charging, power-management, sensor, and testing work that is difficult to reconcile with the first-build budget. The initial project is USB-only; it does not claim wireless capability.

The original 10–12 hour battery target becomes a future-version requirement. Revision A has no battery. A later ESP32-S3 design could combine USB device support, BLE, and capacitive touch, but its radio current, touch reliability, battery life, and cost need their own measured prototype.

## Keybed decision

Each key has a first and second closure. Their time separation is used to estimate key-on velocity. Revision A uses inexpensive tactile switches as a learning prototype, not as a claim of piano-grade action. It must pass feel, consistency, bounce, and velocity-repeatability checks before the mechanism is treated as validated.

## What this document does not claim

This is a design package, not a fabricated or tested instrument. There is no firmware, supplier quotation for most line items, manufacturing quote, enclosure tooling quote, or physical photo yet. The concept drawings are clearly labeled as illustrations.
