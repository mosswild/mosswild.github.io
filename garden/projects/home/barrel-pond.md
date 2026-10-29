---
title: "Half-Barrel Fish Pond & Ceramic Upflow Bog"
date: 2026-10-28
tags:
  - garden/projects/home
  - aquaponics
  - pond
  - ceramics
  - 3d-printing
  - fusion360
draft: false
---

# Half-Barrel Fish Pond & Ceramic Upflow Bog

An outdoor 20-gallon half-barrel container pond located in a shaded patio nook in Portland, Oregon. Built as a closed-loop micro-ecosystem balancing mechanical filtration, biological nutrient export, native marginal plants, and cold-tolerant microfauna.

![[barrel-pond-hanging-planter-installed.jpeg]]
*3D printed planter hanging on the water rim with marginal bog plants growing immersed.*

---

## System Overview & Architecture

- **Container:** 20-gallon above-ground half-barrel with black interior walls.
- **Filter Vessel:** Custom-crafted ceramic filter pot finished in a blue glaze and fired in the kiln.
- **Plenum & Media Bed:** To accommodate the curved, kiln-warped interior of the vessel, the bottom plenum uses modular 3D-printed 7% Gyroid infill blocks (printed wall-less) that conform to the floor. This is topped with inert window screening, large base rocks, a 3/4" cinder/lava core, dense pea gravel, and established seeded pond gravel.
- **Plumbing & Flow:** Submersible circulation pump fitted with Sukh ceramic ring pre-filtration, forcing water upward through the gravel bed before it cascades through a rectangular ceramic notch spillway.
- **Hardscape & Cave:** The spillway drops directly onto a flat splash stone above an inverted terra cotta pot cave on the barrel floor, dampening flow and creating surface gas exchange.
- **Marginal Planters:** Custom parametric 3D-printed brackets hook directly over the tapered barrel staves, suspending marginal plant roots at water level without blocking benthic swimming space.

![[barrel-pond-20261028-01.png]]

---

## Parametric 3D-Printed Hanging Planters

- **Thingiverse Model:** [thingiverse.com/thing:7358797](https://www.thingiverse.com/thing:7358797)
- **Maker Profile:** [Thingiverse (@mosswildsmade)](https://www.thingiverse.com/mosswildsmade/designs)

### Design & Architecture
Standard commercial aquatic plant pots sit at the bottom of the pond, requiring stacks of bricks or cinder blocks to elevate marginal plants to the surface. Furthermore, finding planters that securely hook over the thick, tapered staves of a wooden half-barrel is nearly impossible.

The planter was custom-modeled in Autodesk Fusion with parametric dimensions:
- `RimThickness`: Adjusts the hook bracket to fit anything from thin 6 mm glass up to 35 mm thick barrel staves.
- `BasketWidth` & `BasketDepth`: Customizes plant volume for shallow groundcovers vs. deep-rooted bog marginals.
- `SlitWidth` & `Spacing`: Controls root aeration and water flow through the basket while retaining pea gravel or pond substrate.

![[barrel-pond-planter-cad.png]]
*Parametric Fusion 360 planter design with aeration slits and custom rim hook.*

### Print Settings
- **Material:** Printed in **PETG** or **ASA** to withstand continuous UV exposure and outdoor water immersion without leaching harmful chemicals or softening in summer sun.
- **Infill / Perimeters:** Printed with heavy perimeters to guarantee structural rigidity under the weight of wet gravel.

---

## Species Roster

### Fauna & Livestock
- **Golden White Cloud Mountain Minnows (*Tanichthys albonubes*):** Small school of cold-tolerant minnows. They spend much of their time shoaling low in the water column and treating the terra cotta cave as a permanent sanctuary.
- **Scuds (*Hyalella azteca* / Amphipods):** Benthic shredders established in the gravel bed and leaf litter, actively breaking down fallen organic material.
- **Snails (Ramshorn & Bladder):** Biofilm, surface, and algae grazers maintaining the glass, liner walls, and plant stalks.
- **Micro-Crustaceans:** Ostracods (seed shrimp) and copepods introduced via a live culture pack, surviving in the hornwort and benthic gaps. *(Daphnia were also introduced, though open-water adults were largely predated by the minnows).*

### Flora & Bio-Filtration
- **Hornwort (*Ceratophyllum demersum*):** Dense floating/suspended aquatic thicket serving as the primary in-column nutrient sponge and safety cover.
- **Duckweed (*Lemna minor*):** Low-profile floating carpet that naturally colonized the surface, providing overhead shade and nutrient uptake.
- **Bog & Marginal Plants:**
  - **Bloody Dock (*Rumex sanguineus*):** Hardy nutrient consumer seated directly in the upflow bog gravel.
  - **Western Maidenhair Fern (*Adiantum aleuticum*):** Planted in the upper, damp splash zone of the bog.
  - **Rushes (*Juncus*):** Fibrous marginal structure anchored in the upper filter tray.
  - **Spiral Horsetail (*Equisetum*):** Architectural marginal along the perimeter.
  - **Society Garlic (*Tulbaghia*):** Damp-loving marginal situated with roots in the wet perimeter gravel.
  - **Creeping Jenny (*Lysimachia nummularia*):** Trailing runners set along the margins and water line.

![[barrel-pond-20261028-02.png]]
*Initially filtered with a 3D printed bog filter which catastrophically failed*.

![[barrel-pond-20261028-03.png]]
*Bog Filter slab built out of clay.*

---

## Winterization & Indoor Overwintering

Although Golden White Cloud Mountain Minnows are cold-tolerant down to around 40°F (5°C), an above-ground 20-gallon half-barrel lacks the thermal mass of an in-ground pond and risks freezing solid or experiencing drastic temperature swings during Portland winter freezes.

To keep the colony thriving through the winter:
- **Indoor Transition:** In late autumn before prolonged freezing temperatures arrive, the minnows are netted from the barrel and moved indoors into an established planted aquarium.
- **Seeded Micro-Ecosystem:** Cuttings of hornwort and seeded media from the outdoor system are brought inside with them, instantly seeding the tank's biological cycle and preserving beneficial microfauna (scuds, copepods, and snails).
- **Maintenance:** The fish overwinter indoors under controlled ambient temperatures with minimal supplemental heating required, continuing to graze on biofilm and live food.
- **Spring Reintroduction:** Once late spring outdoor temperatures stabilize and marginal bog plants resume active growth, the minnows are gradually acclimated back into the barrel pond.

![[barrel-pond-indoor-aquarium-placeholder.png]]
*Placeholder: Indoor aquarium setup used for overwintering the minnow colony.*

---

## Challenges & Field Solutions

### 1. Kiln Warping & Plenum Geometry
- **Challenge:** Firing the ceramic filter pot caused uneven shrinking and warpage, meaning a standard rigid circular grate could not sit flat or form a proper plenum seal.
- **Solution:** 3D-printed modular Gyroid infill cubes (7% density) without exterior shells. Their omnidirectional permeability allowed water to disperse freely across the floor beneath the media, while the individual blocks nested naturally against the curved clay bottom.

### 2. Nocturnal Pests & Grazer Raids
- **Challenge:** Local mammalian pests (rats, raccoons) targeted tender bog greens, completely chewing down early starts of Chinese creeping lobelia (*Lobelia chinensis*), damaging horsetails, and nibbling society garlic leaves.
- **Solution:** Swapped to tougher, fibrous, and bitter-scented species (rushes, bloody dock), established perimeter scent barriers (cayenne pepper/capsaicin), and installed targeted rodent bait stations away from the water line.
- Still an ongoing problem actually. Raccoons are a pest still and regularly wreak havoc on the pond.

### 3. Bird Feeder Fallout & Elevated Phosphates
- **Challenge:** A nearby bird feeder caused oily peanut fragments and sunflower hulls to rain into the pond, creating an organic surface sheen and driving dissolved phosphates up to ~5.0 ppm.
- **Solution:** Because the barrel sits in deep shade, the phosphates did not trigger an algae bloom. The combination of scuds and snails shredding coarse fallout, heavy nutrient absorption by the hornwort canopy, and occasional surface skimming stabilized the water clarity.

### 4. Spillway Flow Dynamics
- **Challenge:** Water discharging over the wide rectangular glaze notch tended to cling to the underside or split into weak trickles due to surface tension.
- **Solution:** Directed the notch spillway directly onto a wide, flat splash rock, which broke surface tension, created a thin oxygenating sheet of cascading water, and eliminated turbulent bottom currents.

---

## Interconnected Notes

- [[projects/pottery/ceramic-filter-vessel|Ceramic Filter Vessel]]
- [[projects/home/gyroid-filter-plenum|3D-Printed Gyroid Plenum]]
- [[projects/home/portland-native-bog-plants|Pacific Northwest Bog Plants]]
- [[projects/pottery/misc-pottery-3d-prints|3D Printed Pottery & Studio Tools]]
