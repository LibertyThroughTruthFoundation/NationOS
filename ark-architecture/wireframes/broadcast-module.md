# Wireframe: Broadcast Module (Connections)

**Component:** `BroadcastModule.vue`

## 1. Purpose

This module provides a unified interface to manage all public-facing links, effectively replacing the static `links.html` page with a dynamic, database-driven component.

## 2. Layout

- **Main View:** A simple, single-column list of all links.
- **Admin View:** A drag-and-drop interface to reorder links, add new ones, and edit existing ones.

## 3. Main View (Public)

- **Header:** Displays the user's primary avatar and name (e.g., "NationOS Covenant Bureau").
- **Link List:** A clean, vertical list of buttons, each corresponding to a link. Each button should have:
    - An icon
    - The link title
    - A brief description (optional)

## 4. Admin View (Internal)

- **Authentication:** This view is only accessible to authenticated users.
- **Link Management:**
    - **Add New Link:** A form with fields for `title`, `url`, `icon`, and `description`.
    - **Edit Link:** Clicking an existing link opens the same form populated with its data.
    - **Reorder:** Links can be dragged and dropped to change their display order.
    - **Toggle Visibility:** A switch to enable or disable a link without deleting it.

## 5. Visual Representation (ASCII)

```
+--------------------------------------------------------------------+
| Broadcast Module (Admin View)                                      |
+--------------------------------------------------------------------+
|                                                                    |
|  [+] Add New Link                                                  |
|                                                                    |
|  +--------------------------------------------------+ (drag handle) |
|  | 👑  Bryan Pavlovic (@BryanPavlovicX)              | [Edit] [Hide] |
|  +--------------------------------------------------+               |
|                                                                    |
|  +--------------------------------------------------+ (drag handle) |
|  | 🗽  Sovereign Sentinel (@SovereignSent)           | [Edit] [Hide] |
|  +--------------------------------------------------+               |
|                                                                    |
|  +--------------------------------------------------+ (drag handle) |
|  | 📚  GitHub Repository                             | [Edit] [Hide] |
|  +--------------------------------------------------+               |
|                                                                    |
+--------------------------------------------------------------------+
```
