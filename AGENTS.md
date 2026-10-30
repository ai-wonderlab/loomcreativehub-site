# LOOM Creative Hub — the website, handed over

This file is the memory of the project. Read it first, whoever you are (Claude in Claude Code, Claude on claude.ai with GitHub, or a human).

## What this is

- The live website of **LOOM Creative Hub · Athens** — https://loomcreativehub.com
- Owner: **Angie Simon**, founder & director (angiesimon@loomcreativehub.com, hello@loomcreativehub.com).
- Built on **7 October 2026** in one evening with Claude, in the Viral Passion / AiWonderLab office (Tatoiou 56, Athens), with Angie present. Three commits: initial, "Publish the LOOM Creative Hub website", "Phone navigation: a hang tag on the loom and a map of the whole cloth".
- Handed over to Angie on **30 October 2026** so she can change anything she wants, with her own Claude.

## Where it lives and how it goes live

| Thing | Where |
|---|---|
| Code | this repo, `main` branch |
| Hosting | **GitHub Pages**, branch `main`, folder `/` (root). HTTPS enforced, certificate valid to Jan 2027. |
| Domain | `loomcreativehub.com` + `www`, registered at Squarespace Domains (registrant: LOOM Creative Hub Athens), DNS on Google Cloud DNS. A/AAAA → GitHub Pages, `www` CNAME → `ai-wonderlab.github.io`. |
| Publish | **Every push to `main` is live within about a minute.** There is no build step, no bundler, no framework. |

Do not delete or rename: `CNAME` (keeps the custom domain), `.nojekyll` (tells GitHub to serve files as they are).

## Structure

- `index.html` — **the whole site in one file** (~215 KB): HTML + one `<style>` block + one `<script>` block. Edit this file to change anything.
- `a/` — all images and videos (62 files, WebP + MP4, ~6.4 MB). Posters for videos end in `_p.webp`.
- `404.html` — "Loose end" page.
- `og.jpg`, favicons, `robots.txt`, `sitemap.xml`.
- Fonts come from Google Fonts: Oi, Roboto Flex, Noto Serif Display, Covered By Your Grace, Mynerve.

### The concept: a cloth you pull apart

The site is one long cloth. Each section is a `<section class="band" data-weft="colour" data-name="…" data-says="…">`. The phone navigation ("hang tag") and the "map of the whole cloth" read `data-name` / `data-says` from the sections, so keep those attributes when you add or rename a section.

Sections, in order (ids in `index.html`):

1. `pull` — hero. "There is a loose thread on this cloth. Pull it."
2. `hub` — who we are. People make culture, departments make decks.
3. `five` — the five threads (what we do), index of the next five.
4. `t-question` — thread one: cultural analysis & market research ("your cultural translator").
5. `t-direction` — thread two: creative consulting ("your spirit guide").
6. `t-story` — thread three: creative content & storytelling ("your creative friend").
7. `t-room` — thread four: PR & cultural communication ("your designated driver").
8. `t-whatif` — thread five: creative lab projects (interactive pattern painter).
9. `whole` — case study, all five threads on one job: φεταλόβερ for Τυροκομείο Καλομοίρης.
10. `people` — LOOMístas, the team.
11. `edu` — we also teach (Athens College lifelong learning course, Oct–Nov 2026).
12. `clients` — got loomed: Tsakiris Mallas, Τυροκομείο Καλομοίρης, Sinsay, Golden Gym, Sun of a Beach, Blue Sails, Rom Com, Candelina, …
13. `knot` — say hello. "The person is still the point." — Angie Simon. hello@, Instagram, LinkedIn.

## How to work on it

1. Open the repo in ChatGPT Codex (chatgpt.com/codex) or Claude Code and say what you want changed. Everything is in `index.html`.
2. To add an image or video: drop it in `a/` as WebP (images) or MP4 + a `_p.webp` poster (video), reference it from `index.html`.
3. Commit and push to `main`. Check https://loomcreativehub.com a minute later (hard refresh: GitHub Pages caches for 10 minutes).
4. If something breaks, `git revert` the last commit and push. Nothing else needs to be undone.

## Known facts, so nobody re-discovers them

- The old site was `loomcreativehubathens.com` — it is now dead (404). Only `loomcreativehub.com` matters.
- Instagram handle is `loomcreativehub__` (two underscores).
- The repo describes itself as "built files" because the first version was generated inside a Claude session; there is no separate source. `index.html` **is** the source now.
- Text is in English with Greek words kept on purpose (φεταλόβερ, τριαλαλούμ, LOOMístria). Keep the voice: short, playful, no corporate.
