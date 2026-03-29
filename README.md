# PODIUM — Impromptu Speech Trainer

A single-file web app for practicing impromptu speaking, built for NSDA competition prep and general public speaking practice. No backend, no dependencies, no install — just open `index.html` and speak.

---

## What It Does

PODIUM simulates a real impromptu speaking round. You draw prompts, pick one, prep, and deliver a speech — all timed. After each round you get a self-evaluation checklist and a session history log.

Two formats are supported:

### NSDA Mode
Follows official NSDA Impromptu rules:
- Draws **3 prompts** from a category of your choice
- You pick one and use **7 minutes total**, split however you want between prep and speech
- The clock runs continuously — you decide when to stop prepping and start speaking
- Prompt types: Quotes, Current Events, Famous People, Objects/Places, Abstract Concepts, or Mixed
- Post-speech debrief covers the 3 NSDA judging criteria: **Organization**, **Analysis**, **Delivery**

### Custom Mode
Set your own rules:
- Choose **1–5 prompts** to draw from
- Set **prep time** (0–30 min) and **speech time** (0–30 min, or 0 for untimed)
- Pick a topic category: Politics, Technology, Ethics, Society, Economics, or All
- Separate prep ring timer + live speech structure guide

---

## Features

- **Prompt draw screen** — see all your prompts at once, click to select
- **Prep timer** — countdown ring (Custom) or shared 7-min clock (NSDA)
- **Strategy hints** — 5 tips that reveal gradually during prep time
- **Speech structure guide** — auto-segments your speech time into Intro / Points / Close, highlights the current section
- **Phase alerts** — full-screen flash when a segment ends or time is running low
- **30-second warning** — timer turns red as time runs out
- **Debrief screen** — speech duration, prep used, prompt type, NSDA judging criteria checklist
- **Session history** — last 6 rounds saved to `localStorage`

---

## Deploying to GitHub Pages

1. Fork or create a new repo
2. Add `index.html` to the root of the `main` branch
3. Go to **Settings → Pages → Source → Deploy from branch → main / (root)**
4. Your app will be live at `https://yourusername.github.io/your-repo-name`

No build step required. The file is fully self-contained.

---

## Running Locally

Just open the file in any modern browser:

```bash
open index.html
# or
python3 -m http.server 8080   # then visit http://localhost:8080
```

---

## Prompt Topics

**NSDA prompts** are drawn from 5 categories:

| Category | Examples |
|---|---|
| Quotes | *"The unexamined life is not worth living."* |
| Current Events | *The global mental health crisis among young people* |
| Famous People | *Nelson Mandela, Marie Curie, Greta Thunberg* |
| Objects / Places | *A compass, A library, A ballot box* |
| Abstract | *Silence, The burden of potential, Enough* |

**Custom mode prompts** are debate-style propositions across Politics, Technology, Ethics, Society, and Economics.

---

## NSDA Judging Criteria

When using NSDA mode, the debrief reminds you of the three official evaluation areas:

**Organization** — Clear intro, body, and conclusion. Effective transitions. Easy to follow.

**Analysis** — Directly addresses the prompt. Develops justifications. Establishes significance.

**Delivery** — Consistent eye contact. Confident, varied voice. No notes used.

---

## Tech

- Vanilla HTML, CSS, JavaScript — zero frameworks, zero dependencies
- Google Fonts (Bebas Neue, DM Mono, Playfair Display) loaded via CDN
- Session history stored in `localStorage`
- Works in all modern browsers

---

## Customizing

To add your own prompts, edit the `PROMPTS` (NSDA) or `DEBATE_TOPICS` (Custom) objects in the `<script>` tag of `index.html`. Each entry follows the format:

```js
{ text: "Your prompt text here", sub: "Category Label" }
```

---

## License

MIT — do whatever you want with it.
