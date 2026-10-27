---
title: "Property Intelligence MCP Server"
tags:
  - software
  - mcp
  - python
  - gis
  - open-data
---

# Property Intelligence MCP Server

> *A 100% Free and Open-Source Model Context Protocol server for land, parcel, and environmental intelligence.*

**property-mcp** connects LLMs and AI coding assistants (via the Anthropic Model Context Protocol) to official public US government environmental, geological, and parcel APIs.

The foundational principle of the project is **zero paid subscriptions, zero API keys, and zero commercial scrapers** (like Zillow, RentCast, or RapidAPI). It runs entirely on open public records and official federal/county endpoints.

---

## What It Does

When analyzing raw land or prospective homestead/workshop parcels, evaluating build viability usually requires checking a dozen different clunky county and federal map portals.

`property-mcp` exposes **16 specialized MCP tools** that let an AI agent perform comprehensive land due diligence in seconds:

| Category | Official Public Data Source | Tool Capabilities |
| :--- | :--- | :--- |
| **Flood Risk** | FEMA NFHL MapServer REST API | Flood zone codes, 100-year floodway, SFHA status |
| **Tsunami Elevation**| USGS 3DEP 1m Elevation API | Precise point elevation & 100-ft tsunami safety check |
| **Soil Composition** | USDA NRCS Soil Data Access API | Drainage class, hydric/wetland rating, septic tank absorption field suitability |
| **Environmental** | EPA Facility Registry Service (FRS) | Proximity to Superfund, TRI, and toxic industrial sites |
| **Wildfire Perimeters**| USFS / NIFC WFIGS REST APIs | Active wildfire incidents and historical burn perimeters |
| **Seismic Hazards** | USGS Earthquake FDSN API | Historical fault line activity and seismic hazard levels |
| **Parcel Scoring** | Multi-criteria ranking engine | Scores parcels 0–100 based on price/acre, road access, utilities, and slope |

---

## Architecture & Integration

- **Protocol**: Model Context Protocol (MCP) standard
- **Runtime**: Python 3.11+ / FastMCP
- **Data Transport**: Async `httpx` with automatic retry and exponential backoff
- **Compatibility**: Antigravity IDE, Claude Desktop, Cursor, and any MCP-compliant client
