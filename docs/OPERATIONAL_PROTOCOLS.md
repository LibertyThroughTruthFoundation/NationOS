# OPERATIONAL PROTOCOLS

**Date:** February 2, 2026 (20 Shevat 5786)  
**Status:** Canonical - Master Reference  
**Purpose:** Centralized operational guidelines for NationOS project management

---

## I. GITHUB ARK PROTOCOL

### Repository Structure
**Canonical Repository:** [LibertyThroughTruthFoundation/NationOS](https://github.com/LibertyThroughTruthFoundation/NationOS)

The GitHub repository is the **single source of truth** for all public-facing NationOS documentation, theology, and code. All final, approved versions of doctrinal modules, technical specifications, and architectural plans must reside in this repository.

### Commit Protocol
- **Descriptive commit messages:** Use clear, concise descriptions of changes
- **Atomic commits:** One logical change per commit
- **Push frequency:** Push to GitHub after each major document completion or revision

### Branch Strategy
- **master:** Production-ready, canonical content
- **dev:** (Future) Development branch for experimental content

---

## II. GOOGLE DRIVE ORGANIZATION PROTOCOL

**Full Documentation:** [DRIVE_ORGANIZATION_PROTOCOL.md](./DRIVE_ORGANIZATION_PROTOCOL.md)

### Canonical Folder
**NationOS** folder in Google Drive mirrors the GitHub repository structure and serves as the **staging area** for all documents, PDFs, and assets.

### Key Principles
1. **Single Source of Truth:** NationOS folder is canonical
2. **Mirror GitHub Structure:** Subfolders match GitHub organization
3. **Color Coding:** Visual hierarchy for quick navigation
4. **Descriptions:** Context at a glance for each folder
5. **Priority Starring:** Quick access to frequently used folders
6. **Advanced Search:** Use operators to find files quickly

### Upload Command (rclone)
```bash
rclone copy <local_file> manus_google_drive:NationOS/<subfolder>/ --config /home/ubuntu/.gdrive-rclone.ini
```

### Shareable Link Generation
```bash
rclone link manus_google_drive:NationOS/<path_to_file> --config /home/ubuntu/.gdrive-rclone.ini
```

---

## III. FILE NAMING PROTOCOL

### Standard Format
```
YYYY-MM-DD_Description_Context.md
```

### Examples
- `2026-02-01_NationOS-Response-PreTrib-Rapture-Divine-Council-Framework.md`
- `2026-02-02_Complementary-Partnership-Recovery.md`
- `2026-02-02_Archer-Without-Bow-Crypto.md`

### Sovereign Time Dual Naming
For documents requiring both Gregorian and Hebrew dates:
```
Gregorian [Date] [Time] MST [Location] Biblical [Hebrew Year] [Hebrew Month] [Hebrew Day]
```

Example:
```
Gregorian Mon Feb 2 2026 ~8:30 AM MST Rocky Point Peñasco Biblical ~5786 Shevat 20
```

---

## IV. DIGITAL PRAYER CLOSET PROTOCOL

### Purpose
The Digital Prayer Closet is a **trilingual** (English/Spanish/Hebrew) private journal for theological processing, personal reflections, and strategic planning.

### Location
- **GitHub:** `/docs/01-Digital-Prayer-Closet/`
- **Google Drive:** `NationOS/docs/01-Digital-Prayer-Closet/`

### Format
```markdown
Digital Prayer Closet / Armario de Oración Digital / אַרְמוֹן תְּפִלָּה דִּיגִיטָלִי: [Hebrew Month Day] / [Gregorian Date] [Topic]
אָבִינוּ / Father / Padre: [Prayer content in trilingual format]
אָמֵן / Amen / Amén.
```

### Privacy
Digital Prayer Closet entries are **private by default** and should only be pushed to GitHub if they contain public doctrine or teaching material.

---

## V. PRIVATE vs PUBLIC PROTOCOL

### Private (NOT pushed to GitHub)
- Financial snapshots (e.g., `Financial_Snapshot_2026-01-31_FINAL.md`)
- Personal communications (e.g., Cynthia sovereignty explanations)
- Thread Gold Archives (e.g., `THREAD_GOLD_ARCHIVE_JAN_2026_PRIVATE.md`)
- **Location:** `/Private-Archives/` in Google Drive or local only

### Public (Pushed to GitHub)
- Theological frameworks
- Household-OS specs
- Covenant Finance protocols
- Branding assets
- Evangelism materials
- **Location:** `/docs/`, `/branding/`, `/Public-Doctrine/`

---

## VI. MASTER INDEX PROTOCOL

**File:** [NATIONOS_MASTER_INDEX.md](./NATIONOS_MASTER_INDEX.md)

The Master Index is the **canonical table of contents** for the entire NationOS project. It provides:
- Quick reference to all major documents
- Hyperlinked navigation to key files
- Status indicators (✅ **[NEW]**, 🚧 **[WIP]**, etc.)
- Organizational structure overview

### Update Protocol
The Master Index must be updated whenever:
1. A new document is added to the ARK
2. A major document is revised or renamed
3. A new subfolder is created
4. A document is archived or deprecated

---

## VII. NOTEBOOKLM INTEGRATION PROTOCOL

### Purpose
NotebookLM is used to generate **audio explainer videos** for complex theological or technical documents.

### Workflow
1. Upload document(s) to NotebookLM
2. Generate audio discussion
3. Download audio file
4. Create video script (if needed)
5. Archive audio and script in Google Drive

### Location
- **Audio Files:** `NationOS/NotebookLM-Audio/`
- **Scripts:** `NationOS/docs/01-Digital-Prayer-Closet/` (with `_NotebookLM-Video-Explainer` suffix)

---

## VIII. TELEGRAM FORGE PROTOCOL

### Purpose
The Telegram Forge is the **inner sanctum** for strategic intelligence, covenant warfare planning, and remnant network building.

### Content Sharing
When sharing NationOS documents with the Forge:
1. Provide GitHub link (canonical source)
2. Provide Google Drive shareable link (PDF for easy viewing)
3. Include brief context or summary
4. Tag relevant members if needed

### Privacy
Forge communications are **private** and should not be pushed to GitHub unless they contain public doctrine.

---

## IX. CREED GATES COMPLIANCE PROTOCOL

**Full Documentation:** [/branding/CREED_GATES_PROTOCOL.md](../branding/CREED_GATES_PROTOCOL.md)

All NationOS content must comply with the **5 Immutable Creed Gates:**
1. **No Syncretism** - Deuteronomy 13:1-5
2. **No Egalitarianism** - Ephesians 5, Psalm 127
3. **No Anthropocentrism** - Isaiah 55:8-9
4. **No Transhumanism** - Genesis 1:27
5. **No Replacement Theology** - Romans 11:1-2

### Audit Protocol
Before pushing any content to GitHub:
1. Review for Creed Gates violations
2. Remove or correct any violations
3. Document rationale in commit message

---

## X. RATIFICATION

These operational protocols are **ratified** as of February 2, 2026 (20 Shevat 5786) and supersede all previous operational methods.

**Shoulder iron. Mišpāṭ in all things.**

—Manus AI, Scribe of the ARK
