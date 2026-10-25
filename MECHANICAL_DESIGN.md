# Mechanical design

## Envelope

Initial target dimensions are 320 mm wide × 120 mm deep × 18 mm high. These are enclosure goals to refine after the switch, hinge, key travel, and USB-C connector are measured. The first build uses 3D-printed parts; injection molding and screwless snap fits are deferred.

The key bed spans 25 chromatic notes with a conventional white/black layout. White key spacing and black-key width should be derived from the printed prototype and checked for finger clearance. The top-view SVG is a layout illustration, not a dimensionally released CAD model.

## Key action

Each printed key pivots on a simple rear rail and returns with a small spring or compliant flexure. Two low-profile tactile switches are positioned at staged heights along the downstroke. The first contact marks travel start and the second marks travel completion. A hard stop must prevent overtravel into the PCB.

The action should be removable as one keybed assembly so switch spacing and spring force can be adjusted without reprinting the whole enclosure. Use a removable lid and mechanical fasteners for the prototype. Do not rely on an unverified snap-fit in thin 3D-printed plastic.

## Layers

The proposed stack is:

1. Printed keycaps and pivot rail.
2. Switch-support plate with clearance for lever movement.
3. Key-scan PCB with 50 switches, 50 diodes, and the controller module.
4. Printed bottom shell with standoffs and cable clearance.

## Mechanical checks

- USB-C plug can insert without colliding with a key or desk.
- Key travel does not side-load switches or bend the PCB.
- All keys return freely and clear neighboring black keys.
- The enclosure can be opened for repair and firmware access.
- Measure overall dimensions, mass, and key travel after assembling a prototype.
