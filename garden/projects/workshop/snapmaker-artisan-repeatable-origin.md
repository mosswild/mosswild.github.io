---
title: "Snapmaker Artisan Repeatable CNC Origin System"
tags:
  - 3d-printing
  - cnc
  - workshop
  - woodworking
  - fusion360
---

# Snapmaker Artisan Repeatable CNC Origin System
### Parametric Fixture & Custom Fusion 360 Post-Processor

> A 3D-printed alignment rail and probe holster system paired with a custom Fusion 360 CAM post-processor to achieve fast, repeatable work coordinate origins on the Snapmaker Artisan 200W CNC.

- **Thingiverse Model & F3D CAD**: [thingiverse.com/thing:7301429](https://www.thingiverse.com/thing:7301429)
- **Companion Buzzer Device**: [thingiverse.com/thing:7305460](https://www.thingiverse.com/thing:7305460)
- **Local Repo**: `/Users/cfaber/repos/snapmaker-artisan-repeatable-origin`

---

## The Problem

Setting a reliable Work Coordinate System (WCS) origin on the Snapmaker Artisan spoil board is traditionally slow and prone to error, especially when:
- Swapping end mills mid-job.
- Machining repeatable batches of identical stock.
- Flipping material for two-sided machining.

Stock alignment by eye often results in ruined workpieces or broken bits.

---

## The System Architecture

This project solves repeatability through a tight integration between **physical fixturing**, **CAD modeling**, and **CAM post-processing**:

```
[ Parametric F3D Fixture ] ──> 3D Printed Rail bolted to Spoilboard (50mm grid)
             │
             ├──> Stock aligned to Corner Joint in Fusion 360 CAD
             │
             ├──> Conductive Z-Probe in Holster (Buzzer/Multimeter continuity)
             │
             └──> Custom Post-Processor (.cps) enforces safe Z-clearance
```

### 1. Parametric 3D-Printed Corner Rail
- Anchors directly into the Snapmaker spoilboard's **50mm M4 grid sockets**.
- Features a circular holster that houses a low-cost conductive Z-probe puck.
- Fully parametric in Fusion 360 (`ProbeHeight` and `ProbeDiameter` user parameters allow adapting the fixture to any probe).

![[snapmaker-origin-fixture-installed.jpeg]]
*3D printed alignment rail and probe holster bolted to the Snapmaker Artisan spoilboard.*

### 2. Fusion 360 Modeling & CAM Workflow
- The fixture component is imported directly into the Fusion 360 design as a hybrid assembly.
- Material stock is snapped directly to the fixture's inner origin corner using a Fusion **Joint ($J$)**.
- The WCS Origin is mapped to a pre-defined construction point at the center-top of the probe puck.

![[snapmaker-origin-diagram.png]]
*Coordinate relationship and stock alignment relative to the probe holster.*

### 3. Custom G-Code Post-Processor (`.cps`)
- Standard post-processors might plunge or rapid-traverse across the rail, causing a crash.
- The custom post-processor (`snapmaker_artisan_origin_tool_post_processor.cps`) guarantees the tool head lifts to a safe clearance height (e.g. 10mm above the probe puck) before any XY moves toward the stock, and returns to clearance height at job end.

### 4. Probing & Zeroing
- Conductive probe puck slides into the corner holster.
- An alligator clip connects to the CNC bit.
- Jogging down until an audible continuity buzzer sounds sets exact Z-zero without marring stock.
- The puck is slipped out before the job starts.

![[snapmaker-origin-buzzer.jpeg]]
*Compact standalone buzzer enclosure used for audible electrical continuity probing.*

---

## Hardware & Tooling

- **Machine**: Snapmaker Artisan (200W CNC Module)
- **Fixturing**: 3D printed PETG/PLA+ rail with M4 mounting bolts
- **Probe**: Conductive Z-probe disc with alligator grounding clip
- **Continuity**: Standalone 3D-printed piezo buzzer enclosure ([Thingiverse #7305460 ↗](https://www.thingiverse.com/thing:7305460)) or multimeter continuity setting
- **Software**: Autodesk Fusion 360 (CAD/CAM) + custom JavaScript post-processor

---

## Interconnected Notes

- [[projects/home/govee-light-covers|Govee Outdoor Lights]]
- [[projects/workshop/workshop-setup|Workshop Setup & Jigs]]
