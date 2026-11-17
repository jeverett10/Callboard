# Changelog

## [0.1.6] - 2026-11-17

### Added
- Callboard now holds multiple projects, one per event, each with its own volunteers, shifts, positions and schedule.
- You can start a project from a Christmas Eve or VBS template, a blank project, or a copy of an earlier project.
- You can start a project from a form-export CSV, and its shifts, positions and volunteers are set up for you, with a preview before you create it.
- A Setup tab lets you edit each shift's title, details, time, chip label and form match text.
- The Setup tab also lets you edit each position's name, the role it needs, and which shifts it's needed on.
- You can import volunteer responses by dropping `.eml` files anywhere on a project page, choosing files, or pasting the email text.
- You can import volunteer responses from PDF files that contain selectable text.
- You can import volunteer responses from CSV form exports, one volunteer per row.
- A review screen after every import lets you fix names, availability, roles and preferences before adding anyone.
- Someone who is already on the list is updated by an import instead of being added twice.
- Clear messages explain scanned PDFs, unreadable files and CSV columns that don't match the form.
- Each volunteer now has 1st, 2nd and 3rd role choices, a max number of shifts, notes and partial availability.
- A "Fill empty positions" button balances shift counts, respects max shifts and favors preferred roles.
- Dropdowns list only volunteers who are trained and available, show "(1st choice)" style hints, and hide anyone already placed in that shift.
- Warnings appear for shifts that can't be fully staffed, volunteers booked past their max, and assignments that no longer match.
- A shifts-per-volunteer tally sits beside the schedule.
- You can save a schedule as CSV and print it.
- Undo is available after clearing, removing or importing.
- You can save a backup of all projects and restore it later.

### Changed
- Volunteer qualifications are now role groups (Stationary, Wireless, Dolly, Jib, Shading, Lyrics, PPT) instead of one box per camera.
- The color scheme changed from green to blue, with neutral grays in light and dark mode.
- The starter project now uses fictional volunteer names.
- The app is now named Callboard, and the backup file is now `callboard-backup.json`.
- Data from the earlier single-event version is converted automatically the first time you open Callboard.

### Fixed
- Saving a CSV or backup now works as a normal browser download when the page is hosted outside claude.ai.

### Removed
- The serif typeface is gone, and the whole interface now uses Instrument Sans.

---

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
