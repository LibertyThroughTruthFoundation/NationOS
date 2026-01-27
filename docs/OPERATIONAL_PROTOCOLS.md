# NationOS Operational Protocols

**Document Created:** January 27, 2026  
**Purpose:** Comprehensive operational protocols for NationOS project management, file organization, and administrative workflows

---

## File Naming Convention

**Purpose:** Systematic file naming/labeling protocol to eliminate "poor searching capabilities" and administrative bottlenecks.

**Problem Identified:** "I really am kind of at a loss as to how to refer to what should be there with respects to data like this." (Bryan Pavlovic, Jan 27, 2026)

**Solution:** Standardized file naming convention with date prefix, name/topic, platform/event, and file type.

---

### Conversation Screenshots

**Format:** `YYYY-MM-DD_[NAME]_[PLATFORM]_[TOPIC].png`

**Examples:**
- `2026-01-15_Cynthia_WhatsApp_League7PM.png`
- `2026-01-19_Heather_Text_Release.png`
- `2026-01-20_Albert_Signal_Interrogator.png`
- `2026-01-26_Steven_Telegram_CharityStatus.png`
- `2026-01-22_Bella_Signal_PotipharsWife.png`
- `2026-01-15_Kyle_Telegram_ForgeRemnant.png`

**Folder Structure:**
- `/NationOS/Private-Archives/Conversations/Cynthia/`
- `/NationOS/Private-Archives/Conversations/Heather/`
- `/NationOS/Private-Archives/Conversations/Albert/`
- `/NationOS/Private-Archives/Conversations/Kyle/`
- `/NationOS/Private-Archives/Conversations/Bella/`
- `/NationOS/Private-Archives/Conversations/Steven/`
- `/NationOS/Private-Archives/Conversations/Mom/`
- `/NationOS/Private-Archives/Conversations/Brandon/`
- `/NationOS/Private-Archives/Conversations/Brydon/`
- `/NationOS/Private-Archives/Conversations/Braymil/`

---

### Relationship Development Files

**Format:** `YYYY-MM-DD_[NAME]_[EVENT].md`

**Examples:**
- `2026-01-15_Cynthia_100PercentFit.md`
- `2026-01-19_Heather_ReleaseConfirmed.md`
- `2026-01-20_Bella_PotipharsWifeTest.md`
- `2026-01-20_Albert_InterrogatorNoted.md`
- `2026-01-26_Steven_CharityStatusStrategy.md`
- `2026-01-22_Cynthia_7PMLeagueTest.md`

**Folder Structure:**
- `/NationOS/Private-Archives/Relationships/Cynthia/`
- `/NationOS/Private-Archives/Relationships/Heather/`
- `/NationOS/Private-Archives/Relationships/Bella/`
- `/NationOS/Private-Archives/Relationships/Albert/`
- `/NationOS/Private-Archives/Relationships/Kyle/`
- `/NationOS/Private-Archives/Relationships/Steven/`

---

### Digital Prayer Closet Entries

**Format:** `YYYY-MM-DD_[TOPIC]_MISPAT.md`

**Examples:**
- `2026-01-26_LIBERTYSWAP_MEGAETH_MISPAT.md`
- `2026-01-27_INSIDER_OUTSIDER_SPECTRUM.md`
- `2026-01-26_RENEE_GOOD_MINNEAPOLIS_MISPAT.md`
- `2026-01-26_PASS_INTERFERENCE_CORRECTION.md`
- `2026-01-26_COEXISTENCE_STEVEN_MISPAT.md`
- `2026-01-26_DISCERNMENT_JUDGMENT_CLARITY.md`

**Folder Structure:**
- `/NationOS/docs/01-Digital-Prayer-Closet/`

---

### Theological Framework Documents

**Format:** `[TOPIC]_PROTOCOL.md` or `[TOPIC]_FRAMEWORK.md`

**Examples:**
- `INSIDER_OUTSIDER_PROTOCOL.md`
- `THEOLOGICAL_FRAMEWORK.md`
- `COVENANT_ARCHITECTURE.md`
- `DIVINE_COUNCIL_WORLDVIEW.md`
- `CRYPTO_PROVISION_PROTOCOL.md`
- `LIBERTYSWAP_MEGAETH_PROTOCOL.md`

**Folder Structure:**
- `/NationOS/docs/01-Divine-Council-Framework/`
- `/NationOS/docs/02-Household-OS-Specs/`
- `/NationOS/docs/03-Sovereign-Stack/`

---

### Thread Gold Summaries

**Format:** `YYYY-MM-DD_THREAD_GOLD_[TOPIC].md`

**Examples:**
- `2026-01-15_THREAD_GOLD_CYNTHIA_100PERCENT.md`
- `2026-01-19_THREAD_GOLD_HEATHER_RELEASE.md`
- `2026-01-22_THREAD_GOLD_ANNIVERSARY_PIVOT.md`
- `2026-01-27_THREAD_GOLD_BORDER_RESET.md`

**Folder Structure:**
- `/NationOS/Private-Archives/Thread-Gold/`

---

### Provision/Accounting Files

**Format:** `YYYY-MM-DD_[CATEGORY]_[AMOUNT].md`

**Examples:**
- `2026-01-15_PAYPAL_649.90_VICTORY.md`
- `2026-01-20_MASSMUTUAL_POLICY_LOAN.md`
- `2026-01-22_NESTOR_3000PESOS_MERCY.md`
- `2026-01-27_PHIAT_1.3MILLION_HARVEST.md`

**Folder Structure:**
- `/NationOS/Private-Archives/Provision/`

---

### Mission Products

**Format:** `[PRODUCT]_[VERSION].md` or `[PRODUCT]_[DATE].md`

**Examples:**
- `NATIONOS_MASTER_INDEX.md`
- `HIGH_EFFORT_GOD_LOGOS_V1.png`
- `LIBERTYSWAP_MEGAETH_INTEL.md`
- `RENEE_GOOD_MINNEAPOLIS_MISPAT.md`

**Folder Structure:**
- `/NationOS/docs/`
- `/NationOS/assets/`
- `/NationOS/products/`

---

## Google Drive Folder Structure

**Purpose:** Mirror NationOS GitHub repository structure in Google Drive for backup and accessibility.

**Root:** `NationOS/`

**Subfolders:**
- `NationOS/Private-Archives/`
  - `Conversations/[NAME]/`
  - `Relationships/[NAME]/`
  - `Thread-Gold/`
  - `Provision/`
  - `Digital-Prayer-Closet/`
- `NationOS/Public-Doctrine/`
  - `01-Divine-Council-Framework/`
  - `02-Household-OS-Specs/`
  - `03-Sovereign-Stack/`
- `NationOS/Assets/`
  - `Logos/`
  - `Screenshots/`
  - `Images/`
- `NationOS/Products/`
  - `High-Effort-God/`
  - `LibertySwap-MegaETH/`
  - `NationOS-Ark/`

---

## Operational Workflow

### 1. Conversation Screenshot Capture

**Action:** Capture conversation screenshot (WhatsApp, Signal, Telegram, Text)

**Naming:** `YYYY-MM-DD_[NAME]_[PLATFORM]_[TOPIC].png`

**Storage:**
- **Local:** Save to `/home/ubuntu/upload/` (temporary staging)
- **Google Drive:** Upload to `NationOS/Private-Archives/Conversations/[NAME]/`
- **GitHub:** Do NOT push to GitHub (private dialogue, excluded from public repo)

---

### 2. Relationship Development Documentation

**Action:** Document relationship development event (100% fit, release, test, interrogator)

**Naming:** `YYYY-MM-DD_[NAME]_[EVENT].md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/Private-Archives/Relationships/[NAME]/`
- **Google Drive:** Upload to `NationOS/Private-Archives/Relationships/[NAME]/`
- **GitHub:** Do NOT push to GitHub (private dialogue, excluded from public repo)

---

### 3. Digital Prayer Closet Entry

**Action:** Create digital prayer closet entry (mišpāṭ, discernment, theological processing)

**Naming:** `YYYY-MM-DD_[TOPIC]_MISPAT.md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/docs/01-Digital-Prayer-Closet/`
- **Google Drive:** Upload to `NationOS/Private-Archives/Digital-Prayer-Closet/`
- **GitHub:** Push to GitHub `LibertyThroughTruthFoundation/NationOS` (public doctrine, private details excluded)

---

### 4. Theological Framework Document

**Action:** Create theological framework document (protocol, framework, worldview)

**Naming:** `[TOPIC]_PROTOCOL.md` or `[TOPIC]_FRAMEWORK.md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/docs/01-Divine-Council-Framework/` (or 02/03)
- **Google Drive:** Upload to `NationOS/Public-Doctrine/01-Divine-Council-Framework/` (or 02/03)
- **GitHub:** Push to GitHub `LibertyThroughTruthFoundation/NationOS` (public doctrine)

---

### 5. Thread Gold Summary

**Action:** Create thread gold summary (daily/weekly summary of theological, provision, relational, mission updates)

**Naming:** `YYYY-MM-DD_THREAD_GOLD_[TOPIC].md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/Private-Archives/Thread-Gold/`
- **Google Drive:** Upload to `NationOS/Private-Archives/Thread-Gold/`
- **GitHub:** Do NOT push to GitHub (private dialogue, excluded from public repo)

---

### 6. Provision/Accounting File

**Action:** Document provision event (PayPal victory, MassMutual loan, Nestor mercy, PHIAT harvest)

**Naming:** `YYYY-MM-DD_[CATEGORY]_[AMOUNT].md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/Private-Archives/Provision/`
- **Google Drive:** Upload to `NationOS/Private-Archives/Provision/`
- **GitHub:** Do NOT push to GitHub (private accounting, excluded from public repo)

---

### 7. Mission Product

**Action:** Create mission product (logos, intel report, mišpāṭ analysis)

**Naming:** `[PRODUCT]_[VERSION].md` or `[PRODUCT]_[DATE].md`

**Storage:**
- **Local:** Save to `/home/ubuntu/NationOS/products/` or `/home/ubuntu/NationOS/assets/`
- **Google Drive:** Upload to `NationOS/Products/` or `NationOS/Assets/`
- **GitHub:** Push to GitHub `LibertyThroughTruthFoundation/NationOS` (public product)

---

## File Organization Best Practices

### 1. Date Prefix (YYYY-MM-DD)

**Purpose:** Chronological sorting, easy search by date

**Example:** `2026-01-27_INSIDER_OUTSIDER_SPECTRUM.md` sorts before `2026-01-28_CYNTHIA_LEAGUE_TEST.md`

---

### 2. Name/Topic Identifier

**Purpose:** Easy search by person or topic

**Example:** `2026-01-15_Cynthia_WhatsApp_League7PM.png` (search "Cynthia" returns all Cynthia files)

---

### 3. Platform/Event Identifier

**Purpose:** Context clarity (WhatsApp vs. Signal vs. Telegram)

**Example:** `2026-01-26_Steven_Telegram_CharityStatus.png` (Telegram conversation, not WhatsApp)

---

### 4. File Type Extension

**Purpose:** Format clarity (.png for images, .md for Markdown, .pdf for PDFs)

**Example:** `2026-01-27_INSIDER_OUTSIDER_SPECTRUM.md` (Markdown document, not PDF)

---

## Folder Structure Best Practices

### 1. Private vs. Public Separation

**Private (Google Drive only, NOT GitHub):**
- `/NationOS/Private-Archives/Conversations/`
- `/NationOS/Private-Archives/Relationships/`
- `/NationOS/Private-Archives/Thread-Gold/`
- `/NationOS/Private-Archives/Provision/`

**Public (Google Drive + GitHub):**
- `/NationOS/Public-Doctrine/`
- `/NationOS/Assets/`
- `/NationOS/Products/`

---

### 2. Name-Based Subfolders

**Purpose:** Easy search by person (all Cynthia files in one folder)

**Example:**
- `/NationOS/Private-Archives/Conversations/Cynthia/`
  - `2026-01-15_Cynthia_WhatsApp_League7PM.png`
  - `2026-01-22_Cynthia_WhatsApp_AnniversaryPivot.png`
  - `2026-01-27_Cynthia_WhatsApp_BorderReset.png`

---

### 3. Topic-Based Subfolders

**Purpose:** Easy search by topic (all Divine Council files in one folder)

**Example:**
- `/NationOS/Public-Doctrine/01-Divine-Council-Framework/`
  - `INSIDER_OUTSIDER_PROTOCOL.md`
  - `Insider-Outsider-Spectrum.md`
  - `THEOLOGICAL_FRAMEWORK.md`
  - `DIVINE_COUNCIL_WORLDVIEW.md`

---

## Implementation Plan

### Phase 1: Rename Existing Files (Immediate)

**Action:** Rename all existing conversation screenshots, relationship files, and thread gold summaries using new naming convention.

**Example:**
- Old: `cynthia_league.png`
- New: `2026-01-15_Cynthia_WhatsApp_League7PM.png`

**Tool:** Manus batch rename script (to be created)

---

### Phase 2: Create Folder Structure (Immediate)

**Action:** Create all subfolders in Google Drive and local `/home/ubuntu/NationOS/` directory.

**Folders:**
- `/NationOS/Private-Archives/Conversations/[NAME]/` (13 individuals: Cynthia, Heather, Albert, Chris, Kyle, Bella, Steven, Mom, Brandon, Brydon, Braymil, Enrique, Juan)
- `/NationOS/Private-Archives/Relationships/[NAME]/` (same 13 individuals)
- `/NationOS/Private-Archives/Thread-Gold/`
- `/NationOS/Private-Archives/Provision/`
- `/NationOS/Private-Archives/Digital-Prayer-Closet/`
- `/NationOS/Public-Doctrine/01-Divine-Council-Framework/`
- `/NationOS/Public-Doctrine/02-Household-OS-Specs/`
- `/NationOS/Public-Doctrine/03-Sovereign-Stack/`

**Tool:** Manus folder creation script (to be created)

---

### Phase 3: Move Files to Folders (Immediate)

**Action:** Move all renamed files to appropriate subfolders.

**Example:**
- `2026-01-15_Cynthia_WhatsApp_League7PM.png` → `/NationOS/Private-Archives/Conversations/Cynthia/`
- `2026-01-15_Cynthia_100PercentFit.md` → `/NationOS/Private-Archives/Relationships/Cynthia/`

**Tool:** Manus file move script (to be created)

---

### Phase 4: Sync to Google Drive (Immediate)

**Action:** Sync all organized files to Google Drive using rclone.

**Command:**
```bash
rclone sync /home/ubuntu/NationOS/Private-Archives/ manus_google_drive:NationOS/Private-Archives/ --config /home/ubuntu/.gdrive-rclone.ini
rclone sync /home/ubuntu/NationOS/Public-Doctrine/ manus_google_drive:NationOS/Public-Doctrine/ --config /home/ubuntu/.gdrive-rclone.ini
```

---

### Phase 5: Push to GitHub (Immediate)

**Action:** Push all public doctrine files to GitHub `LibertyThroughTruthFoundation/NationOS`.

**Command:**
```bash
cd /home/ubuntu/NationOS
git add docs/
git commit -m "Jan27 Border Reset: File Naming Protocol + Insider-Outsider Spectrum refined"
git push origin main
```

---

### Phase 6: Establish Operational Habit (Ongoing)

**Action:** Bryan captures conversation screenshots and saves using new naming convention immediately after conversation.

**Habit:**
1. **Capture screenshot** (WhatsApp, Signal, Telegram, Text)
2. **Rename immediately** using `YYYY-MM-DD_[NAME]_[PLATFORM]_[TOPIC].png`
3. **Upload to Google Drive** `NationOS/Private-Archives/Conversations/[NAME]/`
4. **Manus processes** (extracts theological doctrine, creates relationship development file if needed)

**Tool:** Manus automated upload + processing script (to be created)

---

## Manus Automation Scripts (To Be Created)

### 1. Batch Rename Script

**Purpose:** Rename all existing files using new naming convention.

**Input:** List of files with old names + metadata (date, name, platform, topic)

**Output:** Renamed files with `YYYY-MM-DD_[NAME]_[PLATFORM]_[TOPIC].png` format

**Command:**
```bash
manus-batch-rename --input /home/ubuntu/upload/ --output /home/ubuntu/NationOS/Private-Archives/Conversations/ --metadata rename_metadata.csv
```

---

### 2. Folder Creation Script

**Purpose:** Create all subfolders in Google Drive and local directory.

**Input:** List of names (13 individuals: Cynthia, Heather, Albert, Chris, Kyle, Bella, Steven, Mom, Brandon, Brydon, Braymil, Enrique, Juan)

**Output:** Created subfolders in `/NationOS/Private-Archives/Conversations/[NAME]/` and `/NationOS/Private-Archives/Relationships/[NAME]/`

**Command:**
```bash
manus-create-folders --names Cynthia,Heather,Albert,Chris,Kyle,Bella,Steven,Mom,Brandon,Brydon,Braymil,Enrique,Juan --base-dir /home/ubuntu/NationOS/Private-Archives/
```

---

### 3. File Move Script

**Purpose:** Move all renamed files to appropriate subfolders.

**Input:** List of files with new names + target folders

**Output:** Moved files to appropriate subfolders

**Command:**
```bash
manus-move-files --input /home/ubuntu/upload/ --output /home/ubuntu/NationOS/Private-Archives/ --mapping file_folder_mapping.csv
```

---

### 4. Automated Upload + Processing Script

**Purpose:** Automate Bryan's screenshot upload + Manus processing workflow.

**Workflow:**
1. Bryan uploads screenshot to `/home/ubuntu/upload/` (via Manus interface)
2. Manus prompts: "Name? Platform? Topic?"
3. Bryan provides metadata: "Cynthia, WhatsApp, League7PM"
4. Manus renames: `2026-01-27_Cynthia_WhatsApp_League7PM.png`
5. Manus uploads to Google Drive: `NationOS/Private-Archives/Conversations/Cynthia/`
6. Manus processes: Extracts theological doctrine, creates relationship development file if needed

**Command:**
```bash
manus-upload-process --file /home/ubuntu/upload/screenshot.png --name Cynthia --platform WhatsApp --topic League7PM
```

---

## Summary

**File Naming Convention:** `YYYY-MM-DD_[NAME]_[PLATFORM/TOPIC/EVENT].[ext]`

**Folder Structure:**
- `/NationOS/Private-Archives/` (Google Drive only, NOT GitHub)
- `/NationOS/Public-Doctrine/` (Google Drive + GitHub)

**Operational Workflow:**
1. Capture screenshot
2. Rename immediately
3. Upload to Google Drive
4. Manus processes (extracts doctrine, creates relationship file)

**Manus Automation Scripts:**
1. Batch rename
2. Folder creation
3. File move
4. Automated upload + processing

**Implementation Plan:**
1. Phase 1: Rename existing files (immediate)
2. Phase 2: Create folder structure (immediate)
3. Phase 3: Move files to folders (immediate)
4. Phase 4: Sync to Google Drive (immediate)
5. Phase 5: Push to GitHub (immediate)
6. Phase 6: Establish operational habit (ongoing)

---

**End of Operational Protocols**
