# PF-hgfds — Personal Portfolio Website

A clean, single-page personal portfolio website for Girish Lade — full-stack web developer, UI/UX designer, and AI enthusiast.

## What it does

A static portfolio landing page with a hero section, about/skills/experience/contact sections, and an **interactive particle-network background** (particles.js) with mouse repulse interaction. The **Projects** section is dynamic — it fetches the author's public GitHub repositories at runtime via the GitHub REST API (`https://api.github.com/users/girishlade111/repos`) and renders them as cards with name, description, and a "View on GitHub" link.

## Features

- Animated particle-network background (repulse on hover, push on click)
- Hero, About, Projects, Skills, Experience, Contact sections with smooth nav
- Live project cards pulled from the GitHub API — no manual updates needed
- Zero build step — pure HTML/CSS/JS, loads in milliseconds
- Responsive layout for mobile and desktop

## Tech stack

- HTML5, CSS3, vanilla JavaScript
- TypeScript source (`script.ts`) alongside compiled output (`script.js`)
- [particles.js](https://github.com/VincentGarreau/particles.js) via jsDelivr CDN
- GitHub REST API for the live projects feed

## Quick start

No dependencies, no build. Serve the folder with any static server:

```bash
# option 1: Python
python3 -m http.server 8080

# option 2: Node
npx serve .
```

Then open `http://localhost:8080`.

Or simply open `index.html` directly in a browser (the GitHub project feed works best over HTTP).

## Project structure

```
.
├── index.html   # page markup, section layout
├── style.css    # styling
├── script.ts    # TypeScript source (particles config + GitHub API loader)
├── script.js    # compiled JS used by the page
└── README.md
```

## Deployment

Fully static — deployed to **GitHub Pages**: https://girishlade111.github.io/PF-hgfds/

No environment variables, no server, no secrets required. Redeploy by pushing to `gh-pages` via the publicize helper (`gh-pages-push.py`).

---

Built by Girish Lade — https://ladestack.in
