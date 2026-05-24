# Obsidian Second Brain

**Status:** 🔄 Active  
**Started:** Apr 13, 2026  

## What This Is

Knowledge management system built on Obsidian and Web Clipper. Captures research,
articles, and notes into a structured, linked vault. AI-assisted synthesis and weekly
writing practice every Sunday.

## Architecture

- **Core tool:** Obsidian (local-first markdown vault)
- **Capture layer:** Obsidian Web Clipper — browser extension that clips web content
  directly into the vault with metadata intact
- **AI layer:** Claude assists with note synthesis, linking related concepts, and
  surfacing connections across captures
- **Writing practice:** Dedicated Sunday sessions — weekly writing from vault material
- **Integration target:** Grok Brain Export (Project 18) feeding structured AI outputs
  into the vault as linked knowledge nodes

## Key Decisions

**Local-first over cloud.** Obsidian stores everything as plain markdown on disk. No
vendor lock-in, no subscription required for core features, and the files are readable
by any tool — including Claude via direct file access.

**Web Clipper over manual entry.** Friction is the enemy of capture habits. Web Clipper
reduces the cost of saving something to near zero. If capturing is easy, the vault
actually fills up with useful material.

**Weekly writing practice as a forcing function.** Passive capture without synthesis is
just hoarding. The Sunday writing session forces processing — turning raw captures into
actual thinking.

## Lessons Learned

A knowledge system is only as good as the synthesis layer. Captured notes that are never
processed don't compound. The writing practice is what turns the vault from a filing
cabinet into a thinking tool.

The AI layer is most useful for finding non-obvious connections between notes captured
weeks apart — the kind of linking a human wouldn't do manually but that creates genuine
insight when surfaced.

---

*Part of the [Claude Architect Journey](../../README.md)*
