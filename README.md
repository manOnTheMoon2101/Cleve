# Cleve's Homepage — Est. 1996

A personal portfolio site built with a Windows 95 / Geocities aesthetic. Intentionally retro — Comic Sans, blinking text, marquees, fake ads, and all.

---

## Tech Stack

| Tool | Version |
|---|---|
| [Astro](https://astro.build) | ^7.4.11 |
| [Tailwind CSS](https://tailwindcss.com) | ^4.3.5 |
| @tailwindcss/vite | ^4.3.5 |
| Node.js | >=22.23.4 |
| TypeScript | via Astro |

---

## Getting Started

```bash
pnpm install
pnpm dev
```

```bash
pnpm build    # production build → dist/
pnpm preview  # preview the build locally
```

---

## Pages

| Route | File | Description |
|---|---|---|
| `/` | `src/pages/index.astro` | Home — intro, featured projects, retro SA ads sidebar |
| `/about` | `src/pages/about.astro` | Bio, skills table, experience timeline |
| `/projects` | `src/pages/projects.astro` | Full 2-column project grid |

---

## Color Palette

### Backgrounds

| Token | Hex | Used for |
|---|---|---|
| Space black | `#000022` | Page background |
| Deep navy | `#00003a` | Main content panels |
| Dark navy | `#000044` | Project cards, sidebar boxes |
| Navy | `#000066` | Navigation bar, skill tables |
| Win95 gray | `#c0c0c0` | Buttons, dialog boxes |
| Win95 titlebar | `#000080 → #1084d0` | Dialog title bar gradient |

### Text & Accents

| Token | Hex | Used for |
|---|---|---|
| Cyan | `#00ffff` | Links, section headings, tech badges |
| Yellow | `#ffff00` | Project titles, skill headings, highlighted names |
| Hot pink | `#ff69b4` | Subtitle text, visited links |
| Green | `#44ff44` | LIVE badges, stack labels |
| White | `#ffffff` | Body text |
| Mid gray | `#808080` | Win95 button shadow, muted text |

### CLEVE Rainbow Letters

| Letter | Color |
|---|---|
| C | `#ff4444` |
| L | `#ffaa00` |
| E | `#ffff00` |
| V | `#44ff44` |
| E | `#00ffff` |

### Link States

| State | Color |
|---|---|
| Default | `#00ffff` |
| Visited | `#ff69b4` |
| Hover | `#ffff00` |

### Retro Ad Gradients

| Ad | Gradient |
|---|---|
| Telkom Internet | `#0055cc → #002299` |
| Nando's | `#cc2200 → #880000` |
| Chappies | `#6600aa → #440077` |
| Game Stores | `#cc0000 → #880000` |
| Ouma Rusks | `#c8956c → #7a4520` |

---

## Typography

| Class / Element | Font | Used for |
|---|---|---|
| `.font-comic` | Comic Sans MS, Chalkboard SE, cursive | Headings, section titles, project names, the CLEVE logo |
| `body` default | Times New Roman, Times, serif | Body text |
| `.retro-btn`, nav | Arial, Helvetica, sans-serif | Buttons, navigation links |
| `font-mono` (Tailwind) | System monospace | Code snippets, tech badges, error codes, timestamps |

---

## Custom CSS Utilities

Defined in `src/styles/global.css`.

| Class | Description |
|---|---|
| `.font-comic` | Comic Sans MS stack |
| `.animate-blink` | Step-function blink animation (1s, infinite) |
| `.win95-raised` | Windows 95 raised/embossed bevel border |
| `.win95-sunken` | Windows 95 sunken/pressed bevel border |
| `.win95-outer` | Outer frame bevel for dark backgrounds |
| `.border-inset` | CSS inset border (`2px inset #666666`) |
| `.retro-btn` | Windows 95 gray push button — works on `<a>`, `<button>`, `<span>` |
| `.bg-rainbow` | Full-spectrum left-to-right gradient rule |
| `.bg-construction` | Yellow & black 45° diagonal construction stripes |
| `.text-led` | Red LED-glow text (`#ff2200` with layered text-shadow) |
| `.nav-active` | Active nav link — yellow, underlined |

---

## Cursors

Both cursors are hand-drawn SVG pixel art — each "pixel" is a 4×4 block for a chunky 8-bit look.

| File | CSS property | Hotspot | Used on |
|---|---|---|---|
| `public/cursor.svg` | `cursor: url('/cursor.svg') 0 0, auto` | Top-left of arrow tip | `body` (default) |
| `public/cursor-pointer.svg` | `cursor: url('/cursor-pointer.svg') 8 0, pointer` | Fingertip | `a`, `button`, `.retro-btn`, `.cursor-pointer`, interactive inputs |

---

## Features

### Sparkle Cursor Trail
Moving the mouse spawns random star characters (`★ ✦ ✧ ✩ ✶ ·`) in rainbow colors that float upward and fade out. Throttled to ~25 per second. Implemented in `Layout.astro` with a `@keyframes sparkle-fade` animation in `global.css`.

### Mobile Error Dialog
On screens below `md` (768px), a Windows 95-style error dialog blocks access with the message "It is currently 1996. Mobile phones cannot browse the World Wide Web." Clicking OK five times cycles through four escalating error messages before finally revealing the site. The dismissed state is stored in `sessionStorage` so navigating between pages doesn't re-trigger it.

### Retro SA Ads
The homepage sidebar has five fake 90s South African ads (Telkom, Nando's, Chappies, Game Stores, Ouma Rusks). Clicking any ad opens a Windows 95 fatal error dialog with a unique humorous error message per ad.

### Copy-to-Clipboard Email
Any element with `data-copy-email` copies `clevejohnclayton.2101@gmail.com` to clipboard on click and briefly shows a confirmation.

---

## Projects

| Project | Stack | Status |
|---|---|---|
| Gvelte | SvelteKit, Go, Bash | Live |
| Bidstream | Next.js, Supabase, LiveKit, Stitch.io | Live |
| Signal | React, Supabase, Advertising APIs | Live |
| Supa Tail | Next.js, Supabase, Better Auth, Framer Motion, Resend | Live |
| EES | React, Supabase, Resend | Live |
| Unilever WhatsApp Chatbot | SvelteKit, Supabase, Meta API | Live |
| Metaship | Vue.js, Express, MariaDB, AWS | Live |
| The Match Exchange | AngularJS, Firebase, AWS | Live |
| Stock POS App | Python | Local |

---
