# AI‑Text‑Summarizer

An agile, full‑stack web app delivering bite‑size summaries of long texts via the Hugging Face Inference API. No Python dependencies — just plain HTML, CSS, vanilla JS, and a lean Node.js/Express backend.

## 🚀 Core Highlights

* **Seamless UX**: Client‑side validation enables the “Summarize” button only when your input is between 200–100 000 characters
* **Robust API Layer**: `index.js` exposes a single `/summarize` endpoint, serving static assets and relaying payloads
* **AI‑Driven**: `summarize.js` posts your text to `facebook/bart-large-cnn` on Hugging Face, returning an abstractive summary (30–100 tokens)
* **Zero‑Config Frontend**: Plain `index.html` + `style.css` + `script.js`—drop into any static host

## 🗂️ Project Structure

```plaintext
AI-Text-Summarizer/
├── backend/
│   ├── index.js          # Express server & static middleware
│   └── summarize.js      # Hugging Face API integration
├── public/
│   ├── index.html        # Input form & result display
│   ├── style.css         # Responsive, clean styling
│   └── script.js         # Fetch logic & UI state management
├── .gitignore
├── package.json          # express, axios, dotenv, etc.
└── README.md             # ← This file
```

## ⚙️ Quickstart

1. **Clone & Install**

   ```bash
   git clone https://github.com/pranav89624/AI-Text-Summarizer.git
   cd AI-Text-Summarizer
   npm install
   ```

2. **Configure**
   Create a `.env` at project root:

   ```
   ACCESS_TOKEN=<your Hugging Face API token>
   PORT=3000
   ```

3. **Launch**

   ```bash
   npm start
   ```

   Open `http://localhost:3000` and paste any long text. Hit **Summarize**.

## 🔧 Customization & Scaling

* **Model Swap**: Point `summarize.js` at any HF-hosted model (e.g. `facebook/bart-large-cnn`)
* **Chunking**: Enhance for ultra‑long documents—split & re‑join to respect rate limits
* **UI Enhancements**: Add loading spinners, error banners, or copy‑to‑clipboard
* **Deployment‑Ready**: Containerize or deploy on Netlify/Heroku with NODE\_ENV optimization

## 🤝 Contributing

We’re lean and mean—every pull request counts. Whether you:

* Fix an edge case
* Improve style or UX
* Add unit tests or CI/CD workflows
* Extend to multi‑model support

…jump in! Fork → PR → Let’s ship.
