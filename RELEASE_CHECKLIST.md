# Revision A design package checklist

This checklist keeps the design status clear before any order or fabrication run.

## Design files

- [x] USB-first 25-key scope documented; battery, BLE, and touch strip deferred.
- [x] MIDI note span and 50-contact key map defined.
- [x] GPIO assignment and native USB controller module selected for a prototype.
- [x] Concept views, schematic drawing, and native KiCad schematic included.
- [x] BOM target totals US$28.79 using planning estimates.
- [ ] Confirm every KiCad symbol and electrical connection in KiCad ERC.
- [ ] Select measured footprints for switches, diodes, connectors, and module.
- [ ] Replace PCB outline-only board with placed footprints and routed nets.

## Prototype and release gates

- [ ] Order parts only after current module/module-revision and quotes are confirmed.
- [ ] Build one key and validate contact order, bounce, return, and velocity timing.
- [ ] Scan all keys and controls; test multi-key combinations for ghosting.
- [ ] Implement USB MIDI firmware and verify Note On/Off and velocity in a DAW.
- [ ] Measure USB current and check cable/connector mechanical support.
- [ ] Measure the assembled enclosure, weight, and final parts cost.
- [ ] Replace concept illustrations with photos after the physical prototype exists.

The KiCad board is not fabrication-ready, and no hours or prototype tests are claimed by this checklist.
