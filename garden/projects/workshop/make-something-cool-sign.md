---
title: "Make Something Cool: Workshop Neon LED Sign"
tags:
  - workshop
  - 3d-printing
  - lighting
  - electronics
  - fusion360
---

# "Make Something Cool" Workshop Sign
### 3D-Printed Neon Flex LED Sign & Green Wall Installation

> A custom 3D-printed workshop sign housing 6mm neon LED flex lighting, mounted onto a basement faux greenery wall with a companion motion-activated birdsong sound box.

- **Thingiverse Model**: [thingiverse.com/thing:7036613](https://www.thingiverse.com/thing:7036613)
- **Maker Profile**: [Thingiverse (@mosswildsmade)](https://www.thingiverse.com/mosswildsmade/designs)

![[make-something-cool-sign-1.jpg]]
*Illuminated 6mm neon flex sign mounted against the workshop faux foliage green wall.*

---

## Inspiration & Space Design

Basement workshops—especially windowless, compact garage-scale spaces dedicated to multi-discipline crafting (pottery, woodworking, CNC, 3D printing, electronics)—can easily feel dim and industrial.

To transform the space into an inspiring creative zone:
1. **Faux Green Wall**: Installed artificial boxwood/foliage wall panels across the shop wall to break up bare basement walls with lush green texture.
2. **Bright Script Signage**: Designed a high-contrast illuminated sign delivering a daily creative reminder: *"Make Something Cool"*.
3. **Ambient Nature Audio**: Paired with a motion-sensing birdsong sound box to bring natural soundscapes into a windowless underground room.

---

## Design & CAD Workflow

### 1. Vector Typography in Affinity Designer
- Custom script typography and layout for the three words (`Make`, `Something`, `Cool`) were hand-drafted in **Affinity Designer** as vector curves.
- Optimized stroke curves and transitions to maintain continuous paths suited for bending 6mm neon silicone flex tubing, then exported as clean SVG vector geometry.

### 2. 3D Modeling in Autodesk Fusion
- Imported the vector paths into **Autodesk Fusion** sketches.
- Extruded the sign body backing and generated recessed guide tracks specifically sized with tolerances for standard **6mm silicone neon flex LED strip lights** for a snug friction fit.
- Added rear structural webbing with integrated pass-through zip-tie holes for mounting directly to the backing grid of the green wall panels.

---

## Slicing, Splitting & 3D Printing

### 1. Dovetail Splitting in Orca Slicer
- Because the full letter groups exceeded standard 3D printer bed dimensions, each word was split into manageable print segments inside **Orca Slicer**.
- Used Orca Slicer's **Cut tool with the Dovetail connector option**.
- The interlocking dovetail geometry provided positive self-aligning mechanical registration during assembly and increased gluing surface area, preventing sagging across the extended letter spans.

### 2. Printing & Assembly
- **Filament**: **Clear PETG** (provides structural rigidity, temperature resistance in a basement shop, and subtle diffuse light transmission around the letters).
- **Assembly**: Segmented dovetail pieces were slid together and permanently bonded with adhesive along the interlocking joints before pressing the LED strip into place.

![[make-something-cool-sign-2.jpg]]
*Clear PETG backing printed with 6mm channels, dovetail segments joined, and neon flex strip seated.*

---

## Electronics & Wiring

- **Lighting**: 6mm Flexible Neon Silicone LED Strip (12V DC).
- **Wiring Run**: Routed along the internal tracks, with interconnecting wire jumps tucked behind the green foliage to keep power routing concealed.
- **Power Supply**: 12V DC adapter tied into workshop bench power.
- **Motion-Sensing Sound**: Motion-activated chirping birdsong module tucked into the foliage, bringing acoustic ambiance whenever someone walks into the workshop.

---

## Bill of Materials & Tooling

| Component / Tool | Specification / Role | Purpose |
| :--- | :--- | :--- |
| **Affinity Designer** | Vector design software | Layout and typography vector drafting |
| **Autodesk Fusion** | CAD software | 3D body extrusion, 6mm channels, zip-tie mounts |
| **Orca Slicer** | Slicer (Dovetail cut tool) | Segmenting oversized models with mechanical joints |
| **3D Printed Chassis** | Clear PETG (`Make`, `Something`, `Cool`) | Structural sign housing & LED channels |
| **Neon LED Strip** | 6mm Silicone Neon Flex LED ([Amazon ↗](https://a.co/d/4dolxAJ)) | Diffused neon-style script illumination |
| **Power Supply** | 12V DC Adapter | Main sign power |
| **Sound Box** | Motion-activated birdsong sound box ([Amazon ↗](https://a.co/d/aBkudwE)) | Ambient workspace soundscape |
| **Backdrop** | Artificial greenery / boxwood panels | Workshop wall texture & wire concealment |
| **Fasteners** | Small zip ties | Mounting chassis to greenery backing grid |

---

## Interconnected Notes

- [[projects/workshop/workshop-setup|Workshop Setup]]
- [[projects/workshop/snapmaker-artisan-repeatable-origin|Snapmaker Artisan Repeatable Origin]]
- [[projects/home/govee-light-covers|Govee Outdoor Lights]]
