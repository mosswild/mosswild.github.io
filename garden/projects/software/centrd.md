---
title: "Centrd: A Pottery Throwing Diary"
tags:
  - software
  - pottery
  - self-hosted
  - local-first
---

# Centrd: A Throwing Diary

> *Find your center. Challenge your limits. Log your growth.*

**Centrd** is a free, open-source, and self-hostable web diary designed for potters to track throw counts, stages, weight classes, and milestones (like the 200 Cylinder or 100 Bowl challenge).

It was built with a **100% self-hosted, local-first architecture** so all potter profiles, throw logs, configurations, and photos remain on a home server (Docker, Synology, Raspberry Pi) or local machine with complete privacy and zero subscription fees.

---

## Why I Built It

Most pottery tracking apps either push expensive subscriptions or suffer from bloated input forms with hundreds of required fields. When you are sitting at the potter's wheel with slip-covered, muddy fingers, you want to log a throw in 5 seconds without friction.

Centrd is designed around **speed at the wheel**: minimal taps, quick weight logging, and photo capture that can be categorized later.

![[centrd-dashboard.jpeg]]
*Centrd throwing dashboard displaying active challenge progress and quick-log metrics.*

---

## Core Features

- **Local-First & Self-Hostable**: No cloud dependency, zero trackers, 100% data ownership via Docker.
- **Mud-Friendly Logging**: Quick tap interface built for rapid entry between throws.
- **Multiple Challenge Series**: Track progress toward custom challenge goals (e.g. *Spring 100 Bowl Challenge*, *200 Cylinder Sprint*) using tag-based progress.
- **Pure Studio Logbook Mode**: Option to turn off challenge targets entirely for a calm, pressure-free studio diary.
- **Interactive Sticky Notes**: Attach stage-specific notes (*Wet Clay*, *Trimmed*, *Glaze Application*, *Fired*) directly to each piece with stage remapping.
- **Flexible Decimal Weights**: Log in precise decimal weights (`1.3 lb` or `0.8 kg`) with automatic mapping to target weight categories.
- **ZIP Backup & Rebuild**: Full export and import of journals, markdown logs, and photos into a portable archive.
- **Multi-Potter Support**: Multiple isolated potter profiles on a single shared studio server.

![[centrd-history-logbook.jpeg]]
*Chronological logbook view recording weights, throwing notes, and piece stages.*

![[centrd-sticky-notes.jpeg]]
*Interactive sticky notes attached to individual pieces for kiln and glaze updates.*

---

## Tech Stack

- **Framework**: Next.js / TypeScript
- **Styling**: Tailwind CSS
- **Database**: SQLite / Local filesystem
- **Deployment**: Docker container / Node.js
- **Architecture**: Local-first, zero external telemetry

---

## Interconnected Notes
