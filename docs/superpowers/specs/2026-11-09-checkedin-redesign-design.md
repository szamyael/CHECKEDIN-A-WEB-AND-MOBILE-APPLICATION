# CHECKEDIN page redesign

## Intent and goals

Redesign the existing capstone page for students, panelists, and researchers. Give visitors a clear route to the live system and a separate route to research methods and results. Improve readability, responsive behavior, and perceived smoothness without removing research context.

## Approaches

- **Research first:** foreground objectives, methodology, and evaluation; the live product is secondary.
- **Product first:** foreground student-facing features and the live system; research is supporting evidence.
- **Hybrid (selected):** introduce the product with equally clear paths to the live system and research evidence. This was selected in the browser comparison because it accommodates the three stated audiences.

## Constraints and design

- Keep the implementation in the existing standalone `index.html`; no framework, build step, or new runtime dependency.
- Preserve factual research content, project links, screenshot placeholders, responsive navigation, and current page destinations.
- Improve visual hierarchy, spacing, typography, mobile layouts, focus visibility, and keyboard/screen-reader usability.
- Add restrained, short CSS transitions and reveal motion where they aid feedback or orientation. Keep motion transform/opacity based where practical, and honor `prefers-reduced-motion`.
- Avoid inventing research claims or replacing the established academic/project identity.

## Non-goals

- Changing the application, research findings, or project scope.
- Adding heavy animation libraries, scroll hijacking, or motion that delays access to content.
- Replacing placeholder screenshots with unapproved imagery.

## Builder decisions

The precise color tuning, component spacing, transition timing, and responsive breakpoints remain implementation choices, provided they preserve the hybrid hierarchy, accessibility, and existing behavior above.
