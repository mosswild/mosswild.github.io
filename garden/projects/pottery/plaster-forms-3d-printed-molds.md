---
title: "Pouring Plaster Forms from 3D Printed Molds"
tags:
  - pottery
  - 3d-printing
  - fusion360
---

# Pouring Plaster Forms from 3D Printed Molds
### Parametric Mold Jackets for Ceramic Slump, Hump & Press Forms

> A hybrid digital-to-ceramic workflow using parametric Autodesk Fusion 360 models to 3D print thin-shell mold jackets for casting repeatable plaster pottery forms.

- **Thingiverse Model & F3D CAD**: [thingiverse.com/thing:7260045](https://www.thingiverse.com/thing:7260045)
- **Profile**: [Thingiverse (@mosswildsmade)](https://www.thingiverse.com/mosswildsmade/designs)

---

## Overview & Parametric Forms

Rather than turning plaster on a wheel or hand-carving bats, this system generates custom ceramic forms and their corresponding plaster casting jackets directly in Autodesk Fusion (`.f3d`).

The project provides three primary archetype forms:
1. **Generic Bowl Form**: Spherical segment profile for standard soup and cereal bowls.
2. **Blate Form**: Flat-bottomed hybrid bowl/plate with shallow, sloping walls.
3. **Angular Bowl/Plate Form**: Crisp geometric profile for modern tableware.

Each `.f3d` file allows adjusting key user parameters (diameter, draft angles, rim radius, wall height) to output custom-dimensioned forms and matching mold shells.

![[plaster-forms-f3d-parameters.png]]
*Parametric sketch and user parameters in Autodesk Fusion for adjusting mold dimensions.*

---

## 3D Printing the Mold Shells

- **Thin Shell Construction**: Models are printed as thin shells (~1 mm wall thickness). This drastically saves filament while providing sufficient flexibility during demolding.
- **Seam Alignment**: Set slicer seam alignment to **Random**. A continuous aligned z-seam creates a prominent ridge inside the mold that transfers onto every plaster cast and subsequent clay piece.
- **Draft Angles**: Maintain minimum 3°–5° draft angles on all vertical walls so cured plaster slides out cleanly without vacuum lock.

![[plaster-forms-printed-jacket.jpeg]]
*3D printed mold jackets and resulting cured plaster slump/press forms.*

---

## Mold Release & Preparation

- **Release Agent**: Use **Murphy's Oil Soap** (thinned slightly with water or built up in multiple thin frothy coats, wiped smooth).
- **Avoid Vaseline / Petroleum Jelly**: Petroleum jelly clogs the microscopic open pores of the plaster, ruining its ability to absorb moisture from wet clay during slab draping or press molding.

---

## Plaster Mixing & Pouring

- **Plaster Formulation**: USG No. 1 Pottery Plaster (ideal porosity and surface hardness for ceramic work).
- **Consistency & Ratios**:
  - Target consistency: ~70 consistency (70 parts water to 100 parts plaster by weight).
  - Sift plaster into room-temperature water, allow to slake for 2 minutes, then mix thoroughly without whipping air into the slurry.
- **Pouring**: Pour in a steady, thin stream along the lowest point of the mold shell to minimize trapped air bubbles. Lightly tap or vibrate the mold during the initial pour.

---

## Demolding & Finishing

- **Compressed Air Assist**: Once the plaster has reached its exothermic peak and cooled slightly, use compressed air (such as a keyboard dust duster nozzle) directed along the rim seam. The puff of air breaks the surface vacuum and pops the flexible 3D printed shell off the cast.
- **Foot & Rim Dressing**: Sponge edges while the plaster is green (cheesy stage), then scrape the base flat with a surform rasp or metal rib.
- **Curing**: Allow the plaster form to dry thoroughly in a warm, ventilated area before using with clay slabs.

---

## Interconnected Notes

- [[projects/pottery/misc-pottery-3d-prints|3D Printed Pottery & Studio Tools]]
- [[projects/pottery/current-glazes|Current Studio Glazes]]
- [[projects/pottery/glaze-notes|Glaze & Studio Notes]]
- [[projects/software/centrd|Centrd: Pottery Throwing Diary]]
