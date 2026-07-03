# Punit Kulkarni — Portfolio Website

A modern, responsive, single-page portfolio built with plain **HTML5, CSS3, and JavaScript** (no frameworks, no build step). Just open the file in a browser.

## Files

```
index.html   → the entire site (structure + styles + scripts, self-contained)
README.md    → this file
```

## Features

- Responsive layout (mobile, tablet, desktop)
- Light/dark mode toggle (follows system preference by default)
- Glassmorphism navbar with smooth-scroll navigation
- Animated hero with a typing "code editor" panel
- Scroll-reveal animations on every section
- Sections: Home, About, Education (timeline), Skills, Projects, Certifications, Interests, Contact
- Contact form that opens the visitor's email client pre-filled with their message (no backend required)
- Respects `prefers-reduced-motion` for accessibility

## How to view it

**Option A — just open it**
Double-click `index.html`, or drag it into any browser. Everything (fonts, icons) loads from CDNs, so you need an internet connection the first time.

**Option B — local server (optional, avoids any file:// quirks)**
```bash
cd path/to/folder
python -m http.server 8000
```
Then visit `http://localhost:8000`.

## What to customize before publishing

Search the file for these placeholders and swap in your real details:

| Section | Placeholder | Where |
|---|---|---|
| Hero | `PK` avatar circle | Replace the `<div class="avatar">PK</div>` with `<img src="your-photo.jpg" alt="Punit Kulkarni">` and add matching CSS (`border-radius:50%; object-fit:cover; width:100%; height:100%;`) |
| Education | `[Add College Name]`, `[Add University Name]`, `[Add Year]` | `#education` section, 3 timeline cards |
| Projects | GitHub links currently point to your profile (`github.com/beep-ACLR8`) | Update each `<a class="project-link">` `href` to the specific repo once you push these projects (or new ones) |
| Certifications | `[Certification Name]`, `[Issuing Platform / Organization]`, `[Month, Year]` | `#certifications` section — duplicate a `.cert-card` block for more entries |
| Contact form | Sends via `mailto:` | To collect messages without opening the visitor's email app, wire the form to a service like Formspree, EmailJS, or your own backend — replace the `submit` handler in the `<script>` |

## Deploying it for free

Any static host works since it's a single file:

- **GitHub Pages**: push `index.html` to a repo (e.g. `beep-ACLR8.github.io`), enable Pages in repo settings → live in minutes.
- **Netlify / Vercel**: drag-and-drop the folder in their dashboard.

## Tech stack

- HTML5
- CSS3 (custom properties for theming, no framework)
- Vanilla JavaScript (theme toggle, mobile nav, scroll reveal, typing animation, mailto contact form)
- Google Fonts: Sora, Inter, JetBrains Mono
- Font Awesome (icons, via CDN)
