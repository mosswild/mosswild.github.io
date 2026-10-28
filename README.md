# Mosswild Digital Garden

A hybrid personal knowledge repository, project workbench, and public digital garden tracking crafts, physical fabrication, software experiments, and spontaneous ideas.

---

## 1. Purpose

The Mosswild Digital Garden exists as an evolving, interconnected workbench rather than a static publication or traditional blog.

- **Learning in Public**: Documenting active experiments, formulas, jigs, and code as they develop rather than waiting for polished post-mortems.
- **Cross-Disciplinary Synthesis**: Bridging physical making (pottery, studio glazes, woodworking, 3D printing, FPV drones) with software engineering (local-first tools, Model Context Protocol servers, telemetry HUDs).
- **Networked Thought**: Shifting from chronological feeds to a web of concept-driven notes linked by bidirectional associations, tags, and graph views.
- **Living Reference**: Serving as a personal manual for shop setups, CNC origins, glaze recipes, and custom hardware configurations.

---

## 2. Structure

The workspace is organized into clear boundaries separating public garden content, the web publishing engine, and vault-level configurations:

```text
mosswild_digital_garden/
├── README.md                      # Vault overview, architecture & purpose (outside garden)
├── Welcome.md                     # Obsidian default landing note
├── garden/                        # Digital Garden root (public content boundary)
│   ├── index.md                   # Garden homepage, hub & project directory
│   ├── About.md                   # Author bio, external links & profiles
│   ├── attachments/               # Photos, diagrams, and media assets
│   ├── projects/                  # Active and completed builds
│   │   ├── pottery/               # Glazes, throwing logs, plaster mold casting
│   │   ├── workshop/              # Shop setups, CNC fixtures, repeatable origin jigs
│   │   ├── home/                  # Functional home 3D prints & modifications
│   │   ├── software/              # Centrd, property-mcp, ftms-rower, qr8, garmin-camcmd
│   │   ├── fpv/                   # Drone hardware, electronics, and tuning notes
│   │   └── vlog/                  # Video production concepts and outlines
│   └── random-thoughts/           # Mental models, rules (e.g. 72-Hour Gear Rule), insights
├── quartz/                        # Quartz v5 static site generator
│   ├── content -> ../garden       # Symlink targeting the garden/ folder
│   ├── quartz.config.yaml         # Theme, fonts, plugins, and build options
│   └── public/                    # Compiled static production bundle
├── .github/
│   └── workflows/
│       └── deploy.yml             # GitHub Actions CI/CD to GitHub Pages
└── .obsidian/                     # Obsidian editor workspace settings & plugins
```

### Folder Breakdown

| Path | Purpose & Access | Published? |
| :--- | :--- | :--- |
| `garden/` | Public digital garden notes and project documentation. | **Yes** (via Quartz) |
| `garden/projects/` | Domain-specific project hubs and detailed technical logs. | **Yes** |
| `garden/random-thoughts/` | Fleeting ideas, principles, and essays in progress. | **Yes** |
| `garden/attachments/` | Media assets embedded in garden notes. | **Yes** |
| `quartz/` | SSG engine, build scripts, custom styling, and site layout. | **No** (Build Tool) |
| Root (`/`) | Architecture notes, configs, and private vault notes outside `garden/`. | **No** (Internal Only) |

---

## 3. Function & Technical Architecture

The garden functions as a local-first authoring environment that automatically synchronizes with a public static site.

### The Publishing Pipeline

```text
[ Obsidian Vault ] ──( Edit in garden/ )──> [ Git Repository ]
                                                     │
                                               (git push main)
                                                     │
                                                     ▼
                                           [ GitHub Actions CI ]
                                           - Checkout repo
                                           - Node 22 setup
                                           - npx quartz build
                                                     │
                                                     ▼
                                          [ GitHub Pages Host ]
                                        (mosswild.github.io)
```

1. **Authoring (Obsidian)**:
   - Notes are written in standard Markdown with wikilink references (`[[note-name]]`).
   - Obsidian is configured (`.obsidian/app.json`) to create new notes inside `garden/` by default.
   - Internal linking provides auto-complete and visual backlinks across notes.

2. **Publishing Engine (Quartz v5)**:
   - Quartz compiles the content using a symlink (`quartz/content -> ../garden`).
   - Any file outside `garden/` (such as this `README.md` or files inside `.obsidian/`) is excluded from compilation.
   - Generates an interactive graph view, full-text client-side search (`Cmd + K`), link preview popovers, and responsive typography (Fraunces + Plus Jakarta Sans).

3. **Continuous Deployment (GitHub Pages)**:
   - Pushes to the `main` branch trigger `.github/workflows/deploy.yml`.
   - The workflow installs dependencies, runs `npx quartz build`, and deploys the artifact in `quartz/public` to `mosswild.github.io`.

---

## 4. Conventions & Maintenance

- **Internal vs. External Boundaries**:
  - Keep public-facing notes in `garden/`.
  - Keep private notes, draft outlines, and vault meta-documentation in the root directory or in a `private/` folder (configured as ignored in `quartz.config.yaml`).
- **Linking**:
  - Connect notes whenever a project shares techniques (e.g. 3D printing molds linking into pottery slip casting).
- **Frontmatter**:
  - Notes include YAML frontmatter for titles and tags to drive Quartz tag pages and search filters.
