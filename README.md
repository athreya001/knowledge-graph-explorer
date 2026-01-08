# Knowledge Graph Explorer 🧠

A lightweight, client-side explorer for the **Google Knowledge Graph Search API**. Search entities, view relevance scores, and inspect raw JSON responses directly in your browser.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🚀 Live Demo
Once you enable **GitHub Pages** (see below), your demo will be available at:

`https://athreya001.github.io/knowledge-graph-explorer/`

## ✨ Features
- **Client-side only:** no backend, no build step.
- **API key stays local:** stored in your browser’s `localStorage` and sent only to Google’s API.
- **Smart ID detection:** supports text queries (e.g., `Taylor Swift`) or entity IDs (e.g., `/m/05f4p` or `kg:/m/05f4p`).
- **Dark mode:** follows system preference with a manual toggle.
- **JSON inspector:** view and copy raw responses.
- **Export:** download search results as a JSON file.

## 🛠️ Usage
1. Get a **Google Knowledge Graph Search API key** from the [Google Cloud Console](https://console.cloud.google.com/apis/library/knowledgegraphsearch.googleapis.com).
2. Open the app (local, localhost, or GitHub Pages).
3. Paste your key into the **API Key** field.
4. Start exploring!

> Tip: In Google Cloud Console, restrict the API key (HTTP referrers) to your GitHub Pages domain and/or localhost.

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

## 📝 License
Distributed under the MIT License. See `LICENSE` for details.

## ⚠️ Disclaimer
Not affiliated with Google. Data is provided via the Google Knowledge Graph Search API.
