# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.5.0] - 2026-11-17

### Changed
- Renamed the project to Callboard. The page title, home heading, README and
  backup filename (`callboard-backup.json`) now use the new name.
- Saved data is unaffected by the rename; existing projects and volunteers load as before.

## [0.4.0] - 2026-11-17

### Added
- Create a project directly from a form-export CSV. Shifts are built from the
  distinct availability answers (sorted by date and time, with chip labels and
  match text), positions are built from the trained roles, and the volunteers
  open in the review screen.
- Preview in the New project dialog showing the responses, shifts and positions
  found in the chosen CSV.
- Standalone download support: CSV and backup saves fall back to a normal
  browser download when the page is not running inside claude.ai.

### Changed
- Replaced the green theme with a blue one and neutral grays, in light and dark mode.
- Removed the serif typeface; the whole interface now uses Instrument Sans.
- Sample data now uses fictional volunteer names.

## [0.3.0] - 2026-11-17

### Added
- Import volunteer responses from PDF files with selectable text (pdf.js, loaded on first use).
- Import volunteer responses from CSV form exports, one volunteer per row.
- Clear error messages for scanned PDFs, unreadable files and unrecognized CSV columns.

## [0.2.0] - 2026-11-17

### Added
- Multiple projects (Christmas Eve, Easter, VBS, or any event), each with its own
  volunteers, shifts, positions and schedule.
- Project templates (Christmas Eve, VBS, blank) and copy-from-existing-project.
- Setup tab for editing shifts (title, details, time, chip label, form match text)
  and positions (role needed, which shifts each is needed on).
- Import of volunteer response emails by drag and drop of `.eml` files, file picker,
  or pasted text, with a review screen and update-existing-volunteer matching.
- Volunteer preferences (1st, 2nd and 3rd role choice), max shifts, notes and
  partial-availability notes.
- Role groups (Stationary, Wireless, Dolly, Jib, Shading, Lyrics, PPT) replacing
  per-camera qualification columns.
- Auto-fill using an optimal assignment (Hungarian algorithm) that balances shift
  counts, honors max shifts and favors preferred roles.
- Undo for destructive actions, backup and restore of all projects, and
  drag-anywhere import overlay.

### Changed
- Dropdowns now list volunteers by preference rank and show "(1st choice)" style hints.

### Migrated
- Data from the single-event version is converted automatically on first load.

## [0.1.0] - 2026-11-17

### Added
- Single-event Christmas Eve camera schedule converted from the original spreadsheet.
- Dropdowns filtered by role qualification and shift availability, with no
  double-booking within a shift.
- Shifts-per-volunteer tally, coverage warnings for shifts that cannot be fully
  staffed, CSV export and print layout.
- Data saved in the browser with `localStorage`.
