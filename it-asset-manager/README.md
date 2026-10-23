# AssetDesk — IT Asset Manager

A responsive, local-first IT asset inventory application built with **vanilla JavaScript, HTML and CSS**. Designed as a hands-on portfolio project for IT support and front-end fundamentals.

## Features
- Create, view, update and delete IT assets (CRUD).
- Filter by equipment type and status; search by name, tag, owner or notes.
- Live summary metrics.
- Persistent storage with `localStorage`.
- Export inventory as CSV; download/import JSON backups.
- Validate required fields and prevent duplicate asset tags.
- Responsive dark dashboard. All demo records are fictional.

## Getting started
1. Download or clone this repository.
2. Open the folder in Visual Studio Code.
3. Open `index.html` with **Live Server** (or directly in a modern browser).
4. Add/edit example records to explore the app.

No packages, build steps, authentication or backend required.

## Project structure
```
index.html   # Dashboard and accessible forms
styles.css   # Responsive styles
app.js       # Inventory operations, validation, CSV/JSON, persistence
```

## How to test
1. Add a laptop tagged `IT-100`.
2. Try adding another record with the same tag (it should be blocked).
3. Edit the first record and change status to `Maintenance`.
4. Filter by maintenance; verify the count and row.
5. Reload the page and verify the record persists.
6. Export CSV and JSON backup; import the JSON (replaces all current records).
7. Delete a record and verify counts update.

## Privacy and limitations
- Data stays in **this browser/profile** and can be lost if browser storage is cleared.
- **Do not enter client or employer-confidential data.** Use sample/non-sensitive data.
- No real authentication, authorization, multi-user sync, audit trail or server database. This is a portfolio demo, **not an enterprise asset system**.
- Importing JSON replaces the current local inventory after confirmation. Create a backup first.

## Next improvements
- Unit tests and end-to-end browser tests.
- IndexedDB or real backend for larger inventories.
- Assigned-user directory, maintenance histories and audit log.
- Role-based access, API and deployment.

## License
MIT. See [LICENSE](LICENSE).
