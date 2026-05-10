# Bhairava Anugraha

A standing archive of questions answered by Guruji Lokesh, set in obsidian and gold.
The site is a single self-contained HTML file (`index.html`) with all 187 Q&As
embedded as inline data — no build step, no server, no dependencies.

## Running locally

Open `index.html` in any modern browser. That's it.

For best results (especially if you ever switch to fetching content from an
external JSON file), serve the folder over a local HTTP server:

```sh
# Python 3
python3 -m http.server 8000

# Node
npx serve .
```

Then open `http://localhost:8000`.

## Structure

- `index.html` — the entire site (HTML + CSS + JS + Q&A data)
- `README.md` — this file

## Editing content

The 187 Q&As live in a single `<script type="application/json" id="qna-data">`
block near the bottom of `index.html`. Each entry has:

- `num` — the codex number
- `category_key` — one of: `mantra-japa`, `puja-aarti`, `mandala`,
  `experiences`, `advanced`, `women`
- `asker`, `date`, `time`
- `title` — short headline shown in lists and as the entry's heading
- `question` — the full revised question (shown as the pull quote)
- `original` — raw original text (shown in the "Original · Telegram" panel)
- `answer` — the polished answer as HTML (paragraphs separated by `<p>...</p>`)

To add or edit an entry, modify that JSON block and reload the page.

## Design

Aesthetic: *Lacquer & Leaf* — deep void-black with burnished gold accents,
crimson hairlines, gold-flake atmospheric backgrounds. Type pairing:
Cormorant Garamond (display) + EB Garamond (body) + Tiro Devanagari Sanskrit
+ JetBrains Mono (small caps).

