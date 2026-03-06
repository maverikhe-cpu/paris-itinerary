# Repository Guidelines

## Project Structure & Module Organization
This repository is currently a lightweight static project centered on [`paris_itinerary_mobile_friendly_hotel.html`](/Users/mingjiehe/Desktop/development/Paris%202026/paris_itinerary_mobile_friendly_hotel.html). HTML markup, CSS, and JavaScript are embedded in that file. If the project grows, keep related assets in dedicated folders such as `assets/` for images, `styles/` for extracted CSS, and `scripts/` for reusable JavaScript rather than expanding inline blocks indefinitely.

## Build, Test, and Development Commands
There is no build system or package manager configured yet. Use simple local-preview commands:

- `open paris_itinerary_mobile_friendly_hotel.html`: open the page in the default browser on macOS.
- `python3 -m http.server 8000`: serve the repository locally at `http://localhost:8000` for browser testing.

If you add tooling later, document the exact install and run commands here and keep them reproducible.

## Coding Style & Naming Conventions
Use 2-space indentation in HTML, CSS, and JavaScript to match the existing file. Prefer semantic, readable class names such as `.mobile-days`, `.checklist`, and `.content-grid`. Keep CSS custom properties in `:root` for shared colors and spacing. For JavaScript, use `const` by default, `let` only when reassignment is required, and name functions by behavior, for example `renderChecklist()` or `updateProgress()`.

## Testing Guidelines
No automated test suite exists today. Validate changes manually in desktop and mobile-width browser views, and verify key interactions:

- checklist progress updates correctly
- day selection switches content
- the bookings-only toggle filters without breaking detail rendering

When adding nontrivial JavaScript, consider introducing browser-based tests in a `tests/` directory.

## Commit & Pull Request Guidelines
Git history is not available in this workspace, so follow a simple imperative commit style such as `Add hotel summary card` or `Refine mobile day scroller`. Keep each commit focused on one change. Pull requests should include a short description, before/after screenshots for visual edits, and notes on manual testing performed.

## Content & Data Updates
Trip dates, booking items, and day plans are stored in the inline `tripDays` and `checklistItems` arrays. Update those data structures carefully and keep labels user-facing, concise, and consistent with the rendered UI.
