# René — AI Voice Sales Agent Demo
### House of Laurent · Luxury Jewelry Showcase

Built by **Forge** for CWB. Jay's flagship product demo.

---

## 🌐 Live URL
**https://jaylancaster470-gif.github.io/cwb-command-center/**

---

## What This Is

René is a fully functional AI voice concierge embedded in a luxury jewelry store website. This demo shows what René can do for ANY business:

- **Click → Talk → Convert.** Visitors speak naturally; René responds with voice
- No app to download, no form to fill. The website talks back
- Backed by Gemini 1.5 Flash for instant, intelligent responses
- Fully customizable per client (persona, business info, CTAs)

---

## Tech Stack

| Layer | Technology |
|---|---|
| Voice Input | Web Speech API (SpeechRecognition) |
| AI Brain | Google Gemini 1.5 Flash REST API |
| Voice Output | Web Speech Synthesis API |
| Frontend | Pure HTML/CSS/JS (zero dependencies) |
| Hosting | GitHub Pages |

---

## How René Works

```
User clicks orb → SpeechRecognition starts
   ↓
User speaks → transcript captured
   ↓
POST to Gemini API with system prompt + conversation history
   ↓
Gemini responds → text parsed
   ↓
SpeechSynthesis speaks the reply
   ↓
Loop continues (maintains conversation context)
```

---

## Setup / Customization

### Swap out for a different business
Edit the `RENE_SYSTEM_PROMPT` constant in the `<script>` section:
```js
const RENE_SYSTEM_PROMPT = `You are René, the sophisticated AI concierge for [BUSINESS NAME]...`;
```

### Change the Gemini API Key
```js
const GEMINI_API_KEY = "YOUR_KEY_HERE";
```

### Branding
- Colors: Edit CSS variables `--gold`, `--dark`, etc. at the top of `<style>`
- Fonts: Change Google Fonts import (currently Playfair Display + Lato)
- Business name: Search/replace "House of Laurent"

---

## Browser Compatibility

| Browser | Voice Input | Voice Output |
|---|---|---|
| Chrome (desktop) | ✅ | ✅ |
| Edge | ✅ | ✅ |
| Safari (macOS 14+) | ✅ | ✅ |
| Firefox | ❌ (no SpeechRecognition) | ✅ |
| Mobile Chrome | ✅ | ✅ |

> Chrome is recommended for full voice functionality.

---

## Deployment

Currently deployed via **GitHub Pages** from:
`https://github.com/jaylancaster470-gif/cwb-command-center`

Push `index.html` to the root of the `main` branch — Pages picks it up automatically.

---

## Files

```
rene-demo/
├── index.html    ← Complete website + voice agent (single file)
└── README.md     ← This file
```

---

*René is built on CWB infrastructure. For white-label licensing, contact CWB.*
