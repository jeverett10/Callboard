# Callboard

Volunteer scheduling for production teams. Callboard is a single-file web app for
building the call list for events such as Christmas Eve, Easter and VBS: cameras,
shading, lyrics, PPT and similar roles. Each event is a project with its own shifts,
positions and volunteers.

No build step, no server, no dependencies to install. Everything runs in the browser.

## Features

- Multiple projects, one per event, with templates or a copy of an earlier project
- Create a project straight from a form-export CSV: shifts, positions and
  volunteers are built from the answers
- Import volunteer responses from `.eml` emails, PDF (selectable text), CSV, or pasted text
- Review screen to fix names, availability, roles and preferences before adding
- Dropdowns only list volunteers who are trained for the role and available for the shift
- One-click fill that balances shift counts, honors each volunteer's max shifts and
  favors their preferred roles
- Warnings for shifts that cannot be fully staffed, over-scheduled volunteers and
  assignments that no longer match someone's qualifications
- CSV export, print layout, undo, and full backup and restore
- Light and dark mode

## Run it

Open `index.html` in a browser. That's it.

## Host it on GitHub Pages

1. Push this repository to GitHub.
2. In the repository, go to **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**,
   choose the `main` branch and the `/ (root)` folder, then save.
4. After a minute the site is live at `https://<your-username>.github.io/callboard/`.

## Your data

Projects and volunteers are stored in your browser's `localStorage` on the device you
use. Nothing is sent to a server. Because storage is per browser and per site address:

- Use **Save backup of everything** on the home screen before clearing browser data
  or moving to another computer, then **Restore backup** on the other one.
- A copy opened from a file and a copy on GitHub Pages do not share data.

Do not commit real volunteer exports, emails or backups to a public repository.
The included `.gitignore` skips `.eml`, `.csv` and backup `.json` files for that reason.

## Importing responses

Drop files anywhere on a project page, or use **Import responses** on the Volunteers tab.

| Format | Notes |
| --- | --- |
| `.eml` | Drag messages out of Apple Mail. Outlook `.msg` files are not supported. |
| PDF | Must contain selectable text. Scans and photos do not work. One response per PDF. |
| CSV | One volunteer per row. Columns are matched by the form's question text. |
| Pasted text | Paste the body of one response email. |

A form answer counts as a shift when it contains that shift's **match text** (set on the
Setup tab, for example `december 22` or `session 1`).

## Third-party resources

- [Instrument Sans](https://fonts.google.com/specimen/Instrument+Sans) from Google Fonts
- [pdf.js](https://mozilla.github.io/pdf.js/) from cdnjs, loaded only when a PDF is imported

## License

MIT. See [LICENSE](LICENSE).
