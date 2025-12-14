# Wireframe: Intelligence Dashboard

**Component:** `IntelligenceDashboard.vue`

## 1. Layout

- **Main View:** A two-column layout.
- **Left Column (25%):** Search, filters, and a list of all contacts.
- **Right Column (75%):** The main content area, displaying the selected contact's profile.

## 2. Left Column: Filters & Contact List

- **Search Bar:** A prominent search bar at the top to filter contacts by name or keyword.
- **Filter by Type:** A set of checkboxes or buttons to filter by profile type:
    - [ ] Individual
    - [ ] Organization
    - [ ] Movement
- **Filter by Status:**
    - [ ] Strategic Ally
    - [ ] Person of Interest
    - [ ] Adversary
    - [ ] Unwitting Oracle
- **Contact List:** A scrollable list of all contacts, each with a small avatar/icon and their name.

## 3. Right Column: Contact Profile View

- **Header:** The contact's name, profile type, and status are displayed prominently.
- **Tabs:** The profile is organized into tabs:
    - **Profile:** The main intelligence profile content.
    - **Engagements:** A chronological list of all engagement history entries.
    - **Related:** A list of other contacts or documents that are cross-referenced.
- **Tags:** A section displaying all associated tags (e.g., #DivineCouncil, #Narcissism), which are clickable to filter the main contact list.

## 4. Visual Representation (ASCII)

```
+--------------------------------------------------------------------+
| Intelligence Dashboard                                             |
+--------------------------------------------------------------------+
| [Search Contacts...]                                               |
+----------------------+---------------------------------------------+
|                      |                                             |
|  Filters:            |  **Milo Yiannopoulos**                        |
|  - [x] Individual    |  *Strategic Ally*                             |
|  - [ ] Organization  |                                             |
|                      |  +----------------------------------------+ |
|  Status:             |  | Profile | Engagements | Related        | |
|  - [x] Ally          |  +----------------------------------------+ |
|  - [ ] Adversary     |                                             |
|                      |  Core Thesis / Narrative:                   |
|  Contacts:           |  Monarchist ideologue promoting...          |
|  - Milo Y.           |                                             |
|  - Reptile H.        |  Strategic Analysis:                        |
|  - Steven C.         |  Strengths: Articulate, platform...         |
|                      |                                             |
+----------------------+---------------------------------------------+
```
