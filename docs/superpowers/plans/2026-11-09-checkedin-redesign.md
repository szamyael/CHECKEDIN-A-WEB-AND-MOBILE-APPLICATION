# CHECKEDIN Page Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Redesign the CHECKEDIN research page around clear student and academic-reviewer paths, with responsive layouts and restrained accessible motion.

**Architecture:** Keep the existing standalone HTML/CSS/JavaScript page and its content. Refine semantic structure and CSS in place; use lightweight CSS transitions and entrance motion without adding libraries or a build step.

**Tech Stack:** HTML, CSS, vanilla JavaScript; existing browser preview.

**Spec:** `docs/superpowers/specs/2026-11-09-checkedin-redesign-design.md`

## Global Constraints

- Keep the implementation in the existing standalone `index.html`; no framework, build step, or new runtime dependency.
- Preserve factual research content, project links, screenshot placeholders, responsive navigation, and current page destinations.
- Improve visual hierarchy, spacing, typography, mobile layouts, focus visibility, and keyboard/screen-reader usability.
- Add restrained, short CSS transitions and reveal motion where they aid feedback or orientation. Keep motion transform/opacity based where practical, and honor `prefers-reduced-motion`.
- Avoid inventing research claims or replacing placeholder screenshots with unapproved imagery.

## Review Focus

- Mobile navigation must remain operable and accurately expose its expanded state.
- Reduced-motion preferences must suppress nonessential animation and smooth scrolling.
- Keyboard users must retain visible focus and access every navigation/action link.
- Narrow screens and long card text must not cause horizontal overflow or clipped content.
- Existing section anchors, live/repository URLs, research metrics, and screenshot placeholders must remain intact.

---

### Task 1: Redesign the standalone page

**Files:**
- Modify: `CHECKEDIN-A-WEB-AND-MOBILE-APPLICATION/index.html`
- Reference: `docs/superpowers/specs/2026-11-09-checkedin-redesign-design.md`

**Interfaces:**
- Consumes: Existing section IDs, anchors, menu button, navigation links, research content, and external project URLs.
- Produces: A visually refreshed hybrid research/product landing page in the same standalone document.

- [x] **Step 1: Refresh visual hierarchy and responsive layout** in `index.html`; retain all current content and destinations, and make the hero present the live system and research/results as clear parallel paths.
- [x] **Step 2: Improve accessible interaction states** for navigation, buttons, and cards; preserve the mobile menu's `aria-expanded` behavior and provide visible keyboard focus.
- [x] **Step 3: Add restrained interaction and entrance motion** using opacity/transform transitions; disable nonessential motion under `prefers-reduced-motion`.
- [x] **Step 4: Validate desktop and mobile behavior** in the browser: check the navigation toggle and close behavior, keyboard focus, reduced-motion mode, narrow viewport overflow, links/anchors, existing research metrics, and all six screenshot placeholders.
