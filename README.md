[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.18286233-blue)](https://doi.org/10.5281/zenodo.18286233)

# Knowledge Graph Explorer 🧠

A lightweight, client-side explorer for the **Google Knowledge Graph Search API**. Search entities, view relevance scores, and inspect raw JSON responses directly in your browser.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🚀 Live Demo
The GitHub Pages demo is available at:

`https://athreya001.github.io/knowledge-graph-explorer/`

The app uses a public demo API key by default, so no API key setup is required.

## ✨ Features
- **Client-side only:** no backend, no build step.
- **Public demo key:** GitHub Pages, localhost, forks, and direct local use work without copy-pasting a key.
- **Smart ID detection:** supports text queries (e.g., `Taylor Swift`) or entity IDs (e.g., `/m/05f4p` or `kg:/m/05f4p`).
- **Source-aware result links:** separates official entity URLs from source descriptions and license links when Google returns them.
- **Dark mode:** follows system preference with a manual toggle.
- **JSON inspector:** view and copy raw responses.
- **Export:** download search results as a JSON file.

## 🛠️ Usage
1. Open the [live demo](https://athreya001.github.io/knowledge-graph-explorer/), a local copy, or a fork.
2. Search immediately with the public demo key.
3. Start exploring!

Filter examples:
- Filter fields are empty by default and are only sent to Google when filled in.
- Limit is optional; leave it blank to use Google's default result count of 20.
- Languages use ISO 639 codes, such as `en`, `fr`, `es`, `de`, `ja`, or comma-separated values like `fr, en`. Language filters are case-insensitive.
- Types use schema.org-style entity types, such as `Person`, `Place`, `Organization`, `Movie`, or comma-separated values like `Person, Organization`. Common type filters are case-insensitive, so `person, organization` works too.
- Comma-separated language and type values are sent to Google as repeated parameters, for example `languages=fr&languages=en` and `types=Person&types=Organization`.

## API Scope
This project uses the public **Google Knowledge Graph Search API** endpoint at `kgsearch.googleapis.com/v1/entities:search`. It is an entity search explorer, not a clone of the live Google Search knowledge panel, SerpApi's SERP-derived Knowledge Graph response, or a relationship browser for the full graph.

Google Cloud's **Enterprise Knowledge Graph** is a related product with different endpoints, authentication, editions, quotas, and entity identifiers. This demo does not integrate Enterprise Knowledge Graph.

> Tip: Because the demo key is intentionally public and works outside GitHub Pages, rely on Knowledge Graph Search API restrictions, conservative quota limits, and usage monitoring rather than a single-origin HTTP referrer lock.

## 📦 Local Development
No dependencies required.

```bash
git clone https://github.com/athreya001/knowledge-graph-explorer.git
cd knowledge-graph-explorer
```

You can open `index.html` directly, but a tiny local server is more consistent across browsers:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## 🌐 Deploy with GitHub Pages
1. Go to **Settings → Pages**
2. Under **Build and deployment**, select **Deploy from a branch**
3. Choose your default branch (e.g., `main`) and **/(root)**
4. Save

GitHub will publish the site to the URL shown in the **Live Demo** section.

## 🔐 Demo Key Maintenance
- Use a dedicated Google Cloud project/key for this demo.
- Restrict the key to the Knowledge Graph Search API.
- Set conservative quota limits where Google Cloud allows it.
- Replace the `DEMO_API_KEY` constant in `index.html` after rotating the key.

## 🏛️ Zenodo
Published Zenodo versions are archival. If a previous Zenodo version contains an old key, rotate or delete that key in Google Cloud rather than relying on edits to old archives. Publish a new GitHub release after security fixes so Zenodo can archive a patched version.

## 📝 License
Distributed under the MIT License. See `LICENSE` for details.

## ⚠️ Disclaimer
Not affiliated with Google. Data is provided via the Google Knowledge Graph Search API.
