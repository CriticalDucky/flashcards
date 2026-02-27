# Flashcards

A local, single-file flashcard app for Gecko-based browsers (Firefox, Zen).
Open `index.html` directly — no server needed.

---

## Features

- **Library** — all decks shown at a glance, organised into folders
- **Folders** — create, rename, delete; choose an icon from 50 Lucide icons
- **Animated card flip** — smooth 3-D CSS `rotateY` transition; slide animation between cards
- **Math** — KaTeX renders `$...$`, `$$...$$`, `\(...\)`, `\[...\]`
- **Markdown** — GFM via marked.js: bold, italic, code, tables, lists, blockquotes
- **Media** — `<audio>` and `<video>` tags work inside card content
- **Shuffle** — Fisher-Yates; toggle on/off per session
- **Transparent background** — Settings → toggle; topbar hides, floating pill toolbars appear for both library and deck views (Zen/Firefox)
- **Accent color** — Settings → color wheel; any hue, persisted across sessions
- **Drag to folder** — drag deck cards between folders in the library
- **Persistent** — folder layout, imported decks, and settings survive page reloads (localStorage)
- **Import** — file picker button (top-right); no global drag-drop to avoid conflicts
- **Keyboard** — `Space`/`F` flip · `←`/`→` navigate · `S` shuffle · `Esc` back · `keyboard` icon for reference

---

## Deck format

Decks live in `decks/` and are registered in `decks/manifest.json`.

### Q / A format

```markdown
---
deck: My Deck
tags: [tag1, tag2]
---

### Card
Q: Your question here.

A:
Your answer here. Supports **markdown** and $\LaTeX$.

---

### Card
Q: Another question?

A:
Another answer.
```

### Front / back format

```markdown
---
deck: Chemistry
tags: [chem]
---

## front
What is the conjugate base of $\mathrm{HSO_4^-}$?

## back
$\mathrm{SO_4^{2-}}$

---

## front
Next question.

## back
Next answer.
```

Cards are separated by `---` lines. YAML frontmatter (`deck:`, `tags:`) is optional.

---

## Media embeds

Any HTML is valid inside card content:

```markdown
Q: What interval is this?

<audio controls src="media/perfect-fifth.mp3"></audio>

A:
Perfect 5th — 7 semitones.
```

```markdown
Q: What do you see?

<video controls width="100%" style="max-width:480px;border-radius:8px">
  <source src="media/clip.webm" type="video/webm">
  <source src="media/clip.mp4"  type="video/mp4">
</video>

A:
The Golden Gate Bridge.
```

Place media files relative to `index.html`. Remote URLs also work when online.

---

## Repository structure

```
flashcards/
├── index.html          ← open this in Zen/Firefox
└── decks/
    ├── manifest.json   ← deck registry + default folder assignments
    ├── linear-algebra.md
    ├── music-theory.md
    └── media-demo.md
```

### manifest.json

```json
{
  "decks": [
    { "id": "my-deck", "file": "my-deck.md" }
  ],
  "folders": [
    { "id": "math", "decks": ["my-deck"] }
  ]
}
```

Decks in `manifest.json` are loaded automatically on first launch and placed into the specified folders. Subsequent launches preserve the user's folder organisation. Deleting a folder never deletes decks — they move to "Unfiled".

---

## Transparent background (Zen)

Enable via **Settings (gear icon) → Transparent background**.
UI elements stay dark with `backdrop-filter` blur; the desktop shows through the gaps.
Requires Firefox 103+ / Zen (both have `backdrop-filter` enabled by default).

---

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Space` / `F` | Flip card |
| `←` / `A` | Previous card |
| `→` / `D` / `Enter` | Next card |
| `S` | Toggle shuffle |
| `Esc` | Back to library / close modal |
