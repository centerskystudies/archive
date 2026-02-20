# Center for Sky Studies — Archive

A curated, card-based archive built with Jekyll + GitHub Pages.  
Mapping the sky across myth, media, aviation, and folklore.

---

## How to Add a New Entry

1. Create a new file in `_cards/` named `your-entry-id.md`
2. Copy the template below into the file
3. Drop any images into `assets/images/`
4. Push to GitHub — the site rebuilds automatically (~60 seconds)

---

## Card Template

```markdown
---
title: "Your Entry Title"
date: 2024-03-15              # Used for sorting. YYYY-MM-DD.
domain: "Domain · Era"        # e.g. "Mythology · Ancient" or "Media · WWII"
tags:
  - mythology                 # See approved tags below
  - ancient
excerpt: "One or two sentences for the card view. Keep it tight."
connected_to:                 # IDs of related cards (must match filename without .md)
  - icarus
  - magonia
header:
  teaser: /assets/images/your-image.jpg   # REQUIRED for the card cover photo
  # image: /assets/images/your-image.jpg  # Optional: full-width banner on the entry page
---

Your body text here. Standard Markdown applies.

## Section Heading

More text. You can use **bold**, *italic*, `code`, etc.

### Sub-heading

> Pull quotes use blockquote syntax.

- Lists work normally
- Like this

![Image caption](/assets/images/your-image.jpg)
*Caption text below images using italics.*
```

---

## Adding Images

1. Put the file in `assets/images/`
2. Reference in front matter: `teaser: /assets/images/filename.jpg`
3. Reference inline in body: `![Alt text](/assets/images/filename.jpg)`

**The `header.teaser` line is what creates the card cover photo on the archive grid.** Every card with an image needs it.

---

## Approved Tags

| Category | Tags |
|---|---|
| Domain | `mythology` `folklore` `aviation` `media` `ufology` `design` `language` |
| Era | `ancient` `medieval` `industrial` `wwii` `contemporary` `speculative` |
| Concept | `ascent` `fall` `transcendence` `identity` `surveillance` |

---

## Local Preview

Requires Ruby + Bundler.

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

---

## Folder Structure

```
_cards/              ← Your entries. One .md per card.
_layouts/
  card.html          ← Single card page layout (with Connected Entries)
assets/
  css/
    main.scss        ← All CSS overrides and custom styles
  images/            ← All images
_config.yml          ← Site settings, theme, plugins
index.html           ← The archive grid homepage
CNAME                ← Your custom domain (one line)
```
