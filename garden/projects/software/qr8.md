---
title: "QR8 (Curate): Distraction-Free Video Curator"
tags:
  - software
  - web
  - self-hosted
  - productivity
---

# QR8 (Curate)

> *Distraction-Free, Self-Hosted Video Curator for Focused Workspaces & Practice*

**QR8** (pronounced *"Curate"*) is a lightweight, self-hosted web application built for people who use YouTube videos for physical routines, skills development, and daily practice—such as **Yoga, Mobility, Calisthenics, Woodworking Techniques, Pottery Throwing, and Music**—without being derailed by algorithmic rabbit holes, recommended feeds, or comment sections.

QR8 acts strictly as a **curated link lens**: it never downloads or stores copyrighted media files, running inside a single Docker container with an embedded SQLite database.

---

## The Problem QR8 Solves

YouTube is the world's greatest instructional library, but its user interface is actively hostile to focused practice:
- Algorithmic home feeds push sensationalist news and dopamine loops.
- Related videos sidebar pulls your attention away during workouts or builds.
- Autoplay pushes unsolicited videos instead of letting you repeat a drill.

QR8 strips away all the algorithmic noise, providing a clean, quiet cinema viewer dedicated strictly to the playlist or routine you chose.

---

## Core Features

- **Isolated Workspaces**: Partition different crafts and disciplines into separate spaces (e.g. *"Woodworking & Joinery"*, *"Pottery Techniques"*, *"Mobility & Calisthenics"*).
- **Distraction-Free Cinema Player**: Full-screen video player without recommendations, comments, or related videos.
- **Dynamic Blended Thumbnails**: Clean visual cards with live video and creator counts.
- **Self-Hostable Single Container**: Runs on Docker with a local SQLite database and zero external analytics.

---

## Tech Stack

- **Framework**: Next.js (App Router) / TypeScript
- **Database**: SQLite with Drizzle ORM
- **Styling**: Tailwind CSS
- **Deployment**: Single multi-arch Docker image (`docker-compose`)

---

## Interconnected Notes

- [[projects/pottery/glaze-notes|Pottery Practice]]
- [[projects/woodworking/workshop-setup|Woodworking Jigs & Techniques]]
- [[random-thoughts/the-72-hour-gear-rule|Random Thoughts]]
