# DRIVE ORGANIZATION PROTOCOL

**Date:** February 2, 2026 (20 Shevat 5786)  
**Status:** Canonical - Ratified  
**Context:** Google Drive hygiene to mirror GitHub ARK structure

---

## I. PRINCIPLE: SINGLE SOURCE OF TRUTH

The **NationOS** folder in Google Drive is the **canonical staging area** that mirrors the GitHub repository structure. All documents, PDFs, and assets are organized in a hierarchical folder system that matches the GitHub ARK.

**Rationale:** Consistency across platforms (Drive = GitHub) enables seamless synchronization, reduces fragmentation, and maintains mišpāṭ (Psalm 82:8) in file organization.

---

## II. FOLDER STRUCTURE (Mirror GitHub)

```
NationOS/ (Root - Color: Blue - Canonical Staging)
├── /docs/ (Priority Starred - Color: Green)
│   ├── 01-Divine-Council-Framework/ (Color: Purple)
│   │   ├── PreTrib_Collision.md
│   │   ├── Fire_Horse_Prophetic.md
│   │   └── THEOLOGICAL_FRAMEWORK.md
│   ├── 02-Household-OS-Specs/ (Color: Orange)
│   │   ├── Sovereignty_Vocation_Fatherhood_v3.md
│   │   ├── Archer_Metaphor.md
│   │   ├── Complementary_Partnership_Recovery.md
│   │   ├── Archer_Without_Bow_Crypto.md
│   │   ├── COMPLEMENTARY_PARTNERSHIP_RECOVERY_ARK_2026-02-02.pdf
│   │   └── ARCHER_WITHOUT_BOW_CRYPTO_2026-02-02.pdf
│   ├── 03-Sovereign-Stack/ (Color: Red)
│   │   ├── Sovereign_Market_Protocol.md
│   │   ├── Financial_Snapshot_2026-01-31_FINAL.md (gitignore - private)
│   │   └── Infinite_Banking_Recycle.md
│   ├── 01-Digital-Prayer-Closet/ (Color: Gold)
│   │   └── Daily summaries, theological processing
│   └── NATIONOS_MASTER_INDEX.md (Root - Description: Canonical table of contents)
├── /branding/ (Color: Yellow - Logos, Creed Gates, Flag)
│   ├── high_effort_god_brand_library/
│   ├── high_effort_god_logos/
│   ├── CREED_GATES_PROTOCOL.md
│   └── BRAND_AUDIT_VIOLATIONS.md
├── /src/ (Color: Gray - Code, Smart Contracts)
├── /Private-Archives/ (Color: Dark Red - Confidential, not pushed to GitHub)
│   └── THREAD_GOLD_ARCHIVE_JAN_2026_PRIVATE.md
└── /Public-Doctrine/ (Color: Light Blue - Public-facing theology)
    ├── THEOLOGICAL_FRAMEWORK_JAN_2026_PUBLIC.md
    └── INSIDER_OUTSIDER_PROTOCOL.md
```

---

## III. HYGIENE STEPS (Titus 1:12 Order)

### A. Color Coding (Visual Hierarchy)
- **Right-click folder** → **Change Color**
- **Blue:** Root (NationOS)
- **Green:** Priority (docs/)
- **Purple:** Theology (01-Divine-Council-Framework/)
- **Orange:** Household (02-Household-OS-Specs/)
- **Red:** Finance (03-Sovereign-Stack/)
- **Yellow:** Branding
- **Gray:** Code/Technical
- **Gold:** Prayer Closet
- **Dark Red:** Private Archives
- **Light Blue:** Public Doctrine

### B. Descriptions (Context at a Glance)
- **Right-click folder** → **View Details** → **Add Description**
- Example: "Canonical table of contents hyperlinked to all ARK documents"

### C. Star Priority Folders
- **Right-click folder** → **Add Star**
- Starred folders appear in **Recent** sidebar for quick access

### D. Shortcuts (Multiple Folder Access)
- **Select folder** → **Shift+Z** → **Add to another folder**
- Use for cross-referencing (e.g., a document in both `/docs/` and `/branding/`)
- **Note:** Shortcuts do not duplicate files, only create references

### E. Advanced Search Operators
- `creator:me` - Files created by you
- `modified:2026` - Files modified in 2026
- `type:pdf` - All PDFs
- `type:folder` - All folders
- `is:starred` - All starred items
- `parent:"NationOS"` - All items in NationOS folder

---

## IV. UPLOAD PROTOCOL (rclone)

### Standard Upload Command
```bash
rclone copy <local_file> manus_google_drive:NationOS/<subfolder>/ --config /home/ubuntu/.gdrive-rclone.ini
```

### Example: Upload PDF to Household-OS-Specs
```bash
rclone copy /home/ubuntu/document.pdf manus_google_drive:NationOS/docs/02-Household-OS-Specs/ --config /home/ubuntu/.gdrive-rclone.ini
```

### Verify Before Move (Dry Run)
```bash
rclone move <source> <destination> --dry-run --config /home/ubuntu/.gdrive-rclone.ini
```

### Generate Shareable Link
```bash
rclone link manus_google_drive:NationOS/<path_to_file> --config /home/ubuntu/.gdrive-rclone.ini
```

---

## V. FRAGMENTATION PREVENTION

### Do NOT Create:
- Duplicate ARK folders (e.g., "NationOS-ARK-Documents", "The_ARK_v2")
- Loose files at root level (all files must be in subfolders)
- Inconsistent naming (follow File-Naming-Protocol.md)

### Always:
- Upload to existing subfolder structure
- Mirror GitHub organization
- Use descriptive folder names
- Color code for visual hierarchy

---

## VI. ARCHIVAL STRATEGY

### The_ARK Folder (Historical Archive)
- **Status:** Historical reference, not actively maintained
- **Contents:** 943+ files from Liberty Manus exports, HTML, assets
- **Action:** Keep for reference, do not upload new content here

### NationOS Folder (Active Canonical)
- **Status:** Active, mirrors GitHub
- **Contents:** All current ARK documents, organized by subfolder
- **Action:** All new uploads go here

---

## VII. PRIVATE vs PUBLIC PROTOCOL

### Private (NOT pushed to GitHub)
- Financial snapshots (e.g., `Financial_Snapshot_2026-01-31_FINAL.md`)
- Personal communications (e.g., Cynthia sovereignty explanations)
- Thread Gold Archives (e.g., `THREAD_GOLD_ARCHIVE_JAN_2026_PRIVATE.md`)
- **Location:** `/Private-Archives/` or local only

### Public (Pushed to GitHub)
- Theological frameworks
- Household-OS specs
- Covenant Finance protocols
- Branding assets
- **Location:** `/docs/`, `/branding/`, `/Public-Doctrine/`

---

## VIII. BEST PRACTICES (Industry Standards)

Based on research from Tettra, Google Support, GAT Labs, Filerev, JacksDev, GoCobry, and SelectCreditUs:

1. **Consistent Naming Conventions:** Use Sovereign Time dual naming (Gregorian + Hebrew)
2. **Subfolder Hierarchy:** No more than 5 levels deep
3. **Color Coding:** Visual hierarchy for quick navigation
4. **Descriptions:** Context at a glance
5. **Priority Starring:** Quick access to frequently used folders
6. **Advanced Search:** Use operators to find files quickly
7. **Shortcuts:** Cross-reference without duplication
8. **Archive Strategy:** [Archive] prefix for historical content
9. **Team Naming:** Departmental/project-based (e.g., "NationOS", "Covenant Finance")
10. **Security:** Private folders for sensitive content, shared drives for collaboration

---

## IX. RATIFICATION

This protocol is **ratified** as of February 2, 2026 (20 Shevat 5786) and supersedes all previous Drive organization methods. The **NationOS** folder is the canonical staging area, mirroring the GitHub ARK structure.

**Shoulder iron. Mišpāṭ in all things.**

—Manus AI, Scribe of the ARK
