# 📋 Free Templates: Active Tasks — Wishlist & Gift Ideas Hub

This document tracks all development tasks for this template, strictly adhering to the `AGENTS.md` protocol.

- `[ ]` uncompleted | `[/]` in progress | `[x]` completed

---

## 🏃 Current Sprint

### Local Filesystem Initialization
- [x] **T0: [DESIGN] Create Local Directory Structure and Apply Logo** — *(completed 2026-06-18 by Antigravity)*
  - **Changed:** Created subdirectories and copied `moorish_dev_logo.png` into `assets/`.
  - **Gotchas/Next Steps:** Proceed to T0.01.

### 🛠️ Refactoring & Build
- [ ] **[REFACTOR] | T0.01 | ⚡CRITICAL — Build Wishlist & Gift Ideas Hub Notion Template**
  - **Impact:** `/Wishlist and Gift Ideas Hub/notion_screenshots/`, `/docs/`
  - **Details:**
    1. **[ARCHITECTURE]** Create `[DB] Backend`. Move `Wishlist Items` and `People` databases inside. Create a Relation between Wishlist Items → People (gifter/recipient). Create Linked Views on dashboard (Gallery for visual wishlist, Board view by Person).
    2. **[FORMULA]** Add `Total Wishlist Value` via Rollup (sum of Price). Add `Priority Badge`: `ifs(prop("Priority") == "High", "🔥 Must Have", prop("Priority") == "Medium", "⚡ Would Love", "🌿 Nice to Have")`.
    3. **[NAVIGATION]** Synced Block at top for Navigation Menu.
    4. **[FOOTER]** Synced Block at bottom (Traffic Footer) with Moorish Dev brand mention.
    5. **[SEO]** Toggle titled `[Admin] SEO Metadata` with SEO Title, Meta Description, 10 Keywords.
    6. **[BUTTON]** Add Buttons: "🎁 Add Wish" and "✅ Mark as Purchased".
    7. **[CALLOUT]** Gray Callout "How to Use": (1. Duplicate, 2. Add Items to Your List, 3. Share with Family & Friends).
  - **Affiliate Check:** N/A

### 📄 Documentation
- [ ] **[CONTENT] | D12.01 | 🔴 HIGH — Populate `docs/Database_Schema.md`**
- [ ] **[CONTENT] | D12.02 | ⚠️ MEDIUM — Populate `marketing/Launch_Copy.md`**
- [ ] **[CONTENT] | D12.03 | ⚠️ MEDIUM — Populate `setup_guide/Setup_Guide.md`**

### 🚀 Launch
- [ ] **[MARKETING] | L12.01 | 🟢 LOW — Publish to Notion Template Gallery**

---

## Summary

| Phase | Tasks | Done | Remaining |
|-------|-------|------|-----------|
| Init & Structure | 1 | 1 | 0 |
| Build & Refactor | 1 | 0 | 1 |
| Documentation | 3 | 0 | 3 |
| Launch | 1 | 0 | 1 |
| **TOTAL** | **6** | **1** | **5** |

> **Priority Order**: T0.01 → D12.01 → D12.02 → D12.03 → L12.01
