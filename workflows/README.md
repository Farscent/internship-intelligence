# Sanitized n8n workflow exports

Export the actual workflows from n8n's canvas menu → **Download** (JSON), and save them here with these suggested names:

- `01-application-intake.json`
- `02-gmail-ai-intake.json`
- `03-calendar-sync.json`
- `04-deadline-digest.json`

**No real workflow exports are included in this starter package.** This folder is a placeholder until you export your own flows.

Before publishing, examine exports for:
- OAuth credential names and IDs (may identify accounts or projects)
- API keys, bearer tokens, authentication headers and webhook secrets
- Google Spreadsheet IDs, Calendar IDs, addresses or other identifiers
- Pinned execution data and embedded sample emails

Replace private values with nonfunctional placeholders, then re-import the sanitized export into a test n8n instance to check structure. Do not rely on merely removing credential objects from the UI to sanitize an export.
