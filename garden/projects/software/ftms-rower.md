---
title: "FTMS-Rower: Scenic Indoor Rowing Dashboard"
tags:
  - software
  - fitness
  - python
  - bluetooth
---

# FTMS-Rower

> *Transform indoor rowing into an immersive outdoor experience for Concept2 and FTMS machines.*

**FTMS-Rower** is a self-hosted telemetry HUD and scenic video dashboard for indoor rowing ergometers (Concept2 PM5 and standard Bluetooth FTMS machines). 

As you row, your stroke cadence and power dynamically modulate scenic video playback speed ($0.3\times \dots 2.5\times$), while soundtrack audio remains crystal-clear and locked at a steady $1.0\times$.

---

## The Killer Mechanic: Decoupled Video & Audio Rate

Most rowing video apps either:
1. Don't match your stroke rate at all (static video speed), or
2. Chipmunk the soundtrack audio when your cadence speeds up, ruining the immersion.

FTMS-Rower decouples the video playback engine from the audio track:
- **Video Track**: Modulated continuously via Web Bluetooth telemetry from the rower flywheel.
- **Audio Track**: Maintains a rock-solid $1.0\times$ playback speed regardless of whether you're idling at 18 SPM or sprinting at 34 SPM.

![[ftms-rower-cockpit-pm5.png]]
*Cockpit telemetry HUD featuring retro Concept2 PM5 monochrome metrics overlay.*

![[ftms-rower-cockpit-neon.png]]
*Neon cyberpunk cockpit theme with live stroke cadence, 500m split pace, and power graph.*

---

## Core Features

- **Real-Time Telemetry HUD**: Live metrics for Stroke Rate (SPM), 500m Pace, Distance, Elapsed Time, Heart Rate, and Power (Watts).
- **Dual Hardware Support**: Native support for Concept2 PM5 monitors and generic Fitness Machine Service (FTMS) Bluetooth standards.
- **Scenic Route Library**: Stream or cache curated river and water routes (e.g. Thames River, coastal waterways).
- **PWA & Mobile Support**: Responsive dashboard designed for mounting a tablet or phone directly above the ergometer monitor.
- **Docker-Ready**: Easy deployment on a local home server or Raspberry Pi.

![[ftms-rower-home-workouts.png]]
*Home dashboard with quick workout programs and hardware connection status.*

![[ftms-rower-media-center.png]]
*Media center library managing downloadable scenic video tracks and audio.*

---

## Tech Stack

- **Backend**: Python 3.10+ / FastAPI / WebSocket telemetry streaming
- **Hardware Layer**: Web Bluetooth API / Bluetooth Low Energy (FTMS 0x1826 & Concept2 GATT services)
- **Frontend**: Lightweight HTML5 Video Engine / PWA
- **Deployment**: Docker / Compose
