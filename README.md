# KOTCQ

A self‑contained, single‑file web page that provides a quick, resilient editor UI backed by browser localStorage. No build, no dependencies — just open the HTML file and go.

## Features
- **Single file**: Everything lives in `KOTCQ.html`.
- **Offline‑friendly**: Works without a network connection.
- **Local persistence**: Saves your title/body to `localStorage`.
- **Safe editing UX**: Debounced auto‑save, explicit Save and Clear actions.
- **Accessible defaults**: Sensible semantics and focusable controls.

## Quick start
1. Clone or download this repository.
2. Open `KOTCQ.html` directly in your browser.
   - Or serve locally (optional) and open `http://localhost:8000`:
     ```bash
     python3 -m http.server 8000
     ```

## Usage
- Type in a title and body.
- Click **Save (local)** to persist to your browser.
- Click **Clear** to remove saved data (you will be prompted).
- Auto‑save runs after ~900ms of inactivity during typing.

Saved data is stored under the storage key `kotcq:page:v1` and is private to your browser/device.

## Deploying (GitHub Pages)
- Enable GitHub Pages for this repo and select the `main` branch (root).
- Your page will be available at a URL like:
  `https://<your-username>.github.io/KOTCQ/KOTCQ.html`

## Development
There is no build step. Open `KOTCQ.html` in your editor to modify styles, markup, or behavior. The script is embedded at the bottom of the HTML file and uses plain JavaScript.

## Contributing
Issues and PRs are welcome. Please keep changes small and focused.
