# Plainly — Render-ready

A simple slang/idiom explainer that runs entirely in the browser.

## No API key required

This version does **not** use OpenAI, Claude, Gemini, or any other paid AI API.
There is no API key to configure and no backend required.

The site's explanations come from the local phrase database in `phrases.js`.

## Deploy to Render

### Option 1 — GitHub + Render

1. Create a GitHub repository, such as `plainly`.
2. Upload the contents of this folder to the repository.
3. In Render, choose **New → Static Site**.
4. Connect your GitHub account and select the repository.
5. Render can use the included `render.yaml` configuration automatically.

If entering the settings manually:

- **Runtime:** Static Site
- **Build Command:** leave blank
- **Publish Directory:** `.`
- **Environment variables:** none

Then deploy.

### Important

`index.html` must be in the root of the GitHub repository:

    plainly/
    ├── index.html
    ├── style.css
    ├── script.js
    ├── phrases.js
    ├── render.yaml
    └── README.md

Do not put these files inside another nested `plainly-free` folder.

## Editing the phrase database

Open `phrases.js`. Each phrase is represented by an object containing fields such as:

- `phrase`
- `type`
- `meaning`
- `implication`
- `tone`
- `literal`
- `example`
- `similar`

Add additional entries to expand the site's vocabulary.

## Local testing

Because this is a static site, you can open `index.html` directly in a browser for basic testing.

For a local server, if Python is installed:

    python -m http.server 8000

Then visit:

    http://localhost:8000

## Project files

- `index.html` — page structure
- `style.css` — styling and responsive layout
- `script.js` — search and matching behavior
- `phrases.js` — local slang/idiom data
- `render.yaml` — Render deployment configuration
- `README.md` — these instructions
