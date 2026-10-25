# MetroKey 25

MetroKey 25 is a design-stage concept for a compact, 25-key USB MIDI controller intended to connect to a computer and play instruments in a DAW. Its target is a parts-only build below US$30. The current work focuses on the keybed, mechanical action, enclosure, component placement, and KiCad handoff.

## Downloads

- [Complete project source and design files](MetroKey25_Project_Source.zip) — FreeCAD models, KiCad project, drawings, BOMs, research, and chunk-by-chunk design progress. Extract the archive to browse the `MetroKey25/` project folder.
- [Keycap STL exports](MetroKey25_Keycap_Exports.zip) — separate 15-white-key and 10-black-key meshes, the combined 25-key layout, and mesh validation notes.

The combined keycap STL lifts the black-key shells by 0.2 mm above the white-key tops to avoid coincident mesh faces. The separate white and black STL files retain the individual key positions from the FreeCAD integration model.

## Current design scope

- 25-note C3–C5 piano layout with rearward black keys.
- Modeled dual-contact key action and a 5-row × 10-column switch map for velocity-sensing development.
- USB-C and RP2040-Zero placement represented in the mechanical assembly.
- FreeCAD 1.1 project files, STEP/STL exports, dimensioned drawings, BOM, and design notes.
- Editable KiCad schematic starter and board outline for continued electrical design.

The mechanical action and electrical design are not yet validated as a working MIDI controller. The PCB outline is a starter, not a routed design; firmware and hardware prototyping remain future work. The cost target is an estimate rather than a production quote.

## Showcase files

After extracting the source archive, open the `MetroKey25/` folder. Start with `README.md` and `chunks/INDEX.md`. Open `hardware/CAD/MetroKey25/MetroKey25_Assembly.FCStd` in FreeCAD or `chunks/work_packages/CHUNK_10/KiCad_Project/MetroKey25.kicad_pro` in KiCad. SVG previews and drawings can be viewed in a web browser.
