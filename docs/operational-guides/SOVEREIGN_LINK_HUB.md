# OPERATIONAL GUIDE: SOVEREIGN LINK HUB

**Directive:** WEB-01-B
**Date:** 2025-12-14

---

## 1. Purpose

This document provides the operational guide for maintaining the NationOS Sovereign Link Hub, located at `nationOS.io/links`. This self-hosted page replaces third-party services like Linktree, ensuring full sovereignty over our digital presence.

## 2. Location & Technology

-   **Live URL:** `https://libertythroughtruthfoundation.github.io/nationos-website/links.html`
-   **Source File:** `links.html` in the root of the `nationos-website` repository.
-   **Technology:** Static HTML and CSS, hosted on GitHub Pages.

## 3. Maintenance & Updates

To add, remove, or modify links on the hub, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/LibertyThroughTruthFoundation/nationos-website.git
    cd nationos-website
    ```

2.  **Edit the `links.html` File:**
    Open `links.html` in a text editor. The links are structured as simple `<a>` tags. To add a new link, copy an existing block and modify the `href` and text content.

    **Example Link Block:**
    ```html
    <a href="https://gab.com/YourNewHandle" class="link-button" target="_blank" rel="noopener">
        <span class="icon">💡</span>
        <span class="label">New Project</span>
        <span class="handle">@YourNewHandle</span>
    </a>
    ```

3.  **Commit and Push Changes:**
    ```bash
    git add links.html
    git commit -m "Update sovereign link hub with new project"
    git push origin main
    ```

4.  **Verification:**
    Changes will be live within 1-2 minutes. Verify the update by visiting the live URL.

## 4. Current Link Structure (as of 2025-12-14)

### Covenant Bureau Network
-   **Bryan Pavlovic:** `https://gab.com/BryanPavlovicX`
-   **Sovereign Sentinel:** `https://gab.com/SovereignSent`
-   **Liberty Through Truth Foundation:** `https://gab.com/LTTFoundation`
-   **The NationOS:** `https://gab.com/TheNationOS`
-   **God Man Markets:** `https://gab.com/GodManMarkets`

### For Advanced Builders
-   **GitHub Repository:** `https://github.com/LibertyThroughTruthFoundation`
-   **Builder Resources:** `index.html#table-of-contents`
-   **Full Covenant Bureau:** `index.html`

---

**END OF GUIDE**
