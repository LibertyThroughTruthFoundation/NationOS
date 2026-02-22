---
name: heg-manuscript
description: Maintain and extend the High Effort God manuscript research system. Use when adding new theological research, prayer closet entries, cosmology findings, Nephilim/Bene Elohim content, Divine Council material, or any content destined for the High Effort God book trilogy. Also use when asked to find, update, or cross-reference existing research in this system.
---

# High Effort God Manuscript Research Skill

This skill manages a three-document research system for the High Effort God book trilogy. It ensures consistency across document types and provides a structured workflow for adding new material.

## The Three-Document System

The research system consists of three document types, each serving a distinct purpose:

| Document | File | Purpose |
|:---|:---|:---|
| **Reference Index** | `heg-[topic]-reference-index.md` | Obsidian-ready. Keyword tags, topic headers, `[[backlinks]]`, scripture index, repository map. For rapid lookup and navigation. |
| **Detailed Summary** | `heg-[topic]-detailed-summary.md` | Polished prose. Manuscript-ready theological synthesis with full scriptural citations. For book chapters, audio scripts, video content. |
| **Raw Research Notes** | `heg-[topic]-raw-notes.md` | Unedited source aggregation. Prayer closet transcripts, debate transcripts, repository content summaries. The evidence locker. |

**Naming Convention:** All files follow the pattern `heg-[topic-slug]-[document-type].md`. The topic slug identifies the research domain (e.g., `cosmology`, `covenant-economics`, `mercy`, `divine-council`). This prevents file name collisions when multiple topic sets exist simultaneously.

All three documents are stored at: `/home/ubuntu/high_effort_god_research/`

Canonical copies are archived to:
- **GitHub:** `LibertyThroughTruthFoundation/NationOS` under `docs/00-High-Effort-God-Trilogy/research/`
- **Google Drive:** `manus_google_drive:The_ARK/High-Effort-God-Research/`

## Workflow: Adding New Research

When the user provides new material (prayer closet entries, uploaded documents, verbal research, or links), follow this sequence:

### Step 1: Ingest and Classify

Read all provided material. Classify each piece by its primary topic(s) using the tag taxonomy in the Reference Index. If a topic does not exist in the index, create a new entry.

### Step 2: Append to Raw Research Notes

Add the new material verbatim (or near-verbatim) to the appropriate `heg-[topic]-raw-notes.md` file under a new numbered subsection with:
- Source filename or description
- Date received
- Brief summary of content

Do not edit the user's original words in this document. Preserve the prayer closet voice.

### Step 3: Update the Reference Index

For each new topic, scripture reference, or concept introduced:
1. Add or update the relevant concept entry with tags, key passages, core idea, and `[[See Also]]` links.
2. Add any new scripture passages to the Scripture Index table.
3. Update the Repository Map if new files were created or discovered.

### Step 4: Extend the Detailed Summary

Rewrite the new material as polished prose and integrate it into the appropriate section of `detailed_summary.md`. Follow these rules:
- Write in third-person academic style with full paragraphs.
- Include inline scriptural citations for every claim.
- Maintain the existing section numbering (Part 1, Part 2, etc.). Add new Parts at the end or insert sub-sections where they fit thematically.
- Do not duplicate content already present — extend or refine existing sections.
- Reference the correct topic-scoped file, e.g., `heg-cosmology-detailed-summary.md`.

### Step 5: Archive

After all three documents are updated:
1. Copy the updated files to the NationOS GitHub repository under `docs/00-High-Effort-God-Trilogy/research/`.
2. Copy to Google Drive under `The_ARK/High-Effort-God-Research/`.
3. Confirm archival to the user.

Do not push to GitHub without user review if the material contains private prayer closet content. Ask first.

## Workflow: Finding Existing Research

When the user asks about a topic already in the system:
1. Search the appropriate `heg-[topic]-reference-index.md` for the relevant tags and `[[backlinks]]`.
2. Pull the corresponding section from `heg-[topic]-detailed-summary.md` for the polished version.
3. Pull the corresponding section from `heg-[topic]-raw-notes.md` for the original source material.

## Topic Taxonomy

The current core topics (see Reference Index for full details):

Cosmology, Divine Council, Fallen Angels / Watchers, Nephilim, Demons, Jurisdictional Theology, The Great Deception / ET Psyop, Multi-Canon Theology, The Nachash / Serpent Seed, Leviathan / Chaos Monster, Spiritual Warfare, The Flood / Cherem, Forbidden Knowledge, Mastema and the 10% Plea, Sinodos Patterns, High Effort Intelligence, Remnant Theology, Fiat & PHIAT, Covenant Economics, Jubilee.

## Current Topic Sets

| Topic Slug | Raw Notes | Reference Index | Detailed Summary |
|:---|:---|:---|:---|
| `cosmology` | `heg-cosmology-raw-notes.md` | `heg-cosmology-reference-index.md` | `heg-cosmology-detailed-summary.md` |
| `covenant-economics` | *(not yet created)* | *(not yet created)* | *(not yet created)* |

When a new topic set is needed, create all three files following the naming convention and add a row to this table.

## Key Repositories

When scanning for related content, check these locations:

- `NationOS/docs/01-Divine-Council-Framework/` — Creedal audits and deep dives
- `NationOS/docs/00-High-Effort-God-Trilogy/` — Book material and prayer closet
- `NationOS/docs/05-Bezalel-Market/` — Outlines, scripts, and public posts
- `NationOS/docs/theology/` — Theological guides
- `NationOS/docs/strategic-intelligence/eschatology/` — Eschatological analysis
- `NationOS/docs/01-Digital-Prayer-Closet/` — Prayer closet entries
- `Google Drive: The_ARK/` — Archived theological notes
- `Google Drive: NationOS/` — Session documents and prayer closet entries
