---
deck: Media Embeds
tags: [demo, audio, video, image]
---

### Card
Q: Who is this character?

![Wirt](test_image.jpg)

A:
**Wirt** — the anxious, poetry-loving protagonist of *Over the Garden Wall* (Cartoon Network, 2014).

---

### Card
Q: What animal makes this sound?

<audio controls src="https://upload.wikimedia.org/wikipedia/commons/transcoded/1/15/Parus_major_15mars2011.ogg/Parus_major_15mars2011.ogg.mp3"></audio>

A:
A **great tit** (*Parus major*) — one of the most common European songbirds.

---

### Card
Q: What does this landscape look like?

<video controls width="100%" style="max-width:480px;border-radius:8px">
  <source src="https://upload.wikimedia.org/wikipedia/commons/transcoded/4/46/GoldenGateBridge-001.ogv/GoldenGateBridge-001.ogv.480p.vp9.webm" type="video/webm">
  <source src="https://upload.wikimedia.org/wikipedia/commons/4/46/GoldenGateBridge-001.ogv" type="video/ogg">
</video>

A:
The **Golden Gate Bridge**, San Francisco.

Opened: May 27, **1937**. Span: 1,280 m. Color: *International Orange.*

---

### Card
Q: How do you embed **audio** in a flashcard?

A:
```html
<audio controls src="path/to/sound.mp3"></audio>
```

For local files, place them relative to `index.html`.
Remote URLs (Wikimedia Commons, CDN, etc.) also work when online.

---

### Card
Q: How do you embed **video** in a flashcard?

A:
```html
<video controls width="100%" style="max-width:480px;border-radius:8px">
  <source src="video.webm" type="video/webm">
  <source src="video.mp4" type="video/mp4">
</video>
```

Multiple `<source>` elements provide browser fallbacks.

---

### Card
Q: What image formats can you embed?

A:
Standard HTML `<img>` tags work:

```html
![alt text](path/to/image.png)
```

or inline HTML:

```html
<img src="diagram.svg" style="max-width:400px">
```

Paths are relative to `index.html`.
