# ClockJoy SEO / GEO pipeline (Mon / Fri)

Operating manual for the agent that owns the ClockJoy GitHub Pages site end-to-end.

## Scope

- **Repo:** `sunzhengnj/ClockJoy` (branch `main`, site files at the **repo root**).
- **Live site:** https://sunzhengnj.github.io/ClockJoy/ (GitHub Pages serves `main` from `/`).
- **Public brands only:** 开薪 (CN) / **ClockJoy** (EN). Never use any former or internal product name anywhere public — titles, meta, OG tags, alt text, body copy, CTAs, social drafts, or links. Former site URLs are legacy redirects only; never link to them.
- **Do not:** change GitHub Pages settings, invent App Store Connect live-metadata changes, or auto-post to social.
- **Product truth:** workday countdown + estimated earnings + Lock Screen / Dynamic Island widgets. Estimates only — **not** payroll, timesheet, tax, or attendance.

## Monday / Friday routine (EN + CN)

Cadence is **Monday and Friday ~21:15 Asia/Shanghai**: publish **both** an English guide and a Chinese twin for the **same** new theme angle.

1. Open `marketing/seo-geo/QUEUE.md` and take the top item marked `[next]` (rotate themes; do not repeat the last few angles).
2. Write **one** substantial EN guide under `en/guides/` (~600–900 words equivalent HTML). Match style of recent EN guides (`../../site.css`, header, `article`, App Store CTA to `id6771261514`). Public brand: **ClockJoy**. Product truth: **Estimates ≠ paycheck**.
3. **Required:** write the CN twin under `guides/` the same run. Public brand: **开薪**. Product truth: **估算≠工资条**. Wire `hreflang` both ways and add “中文版 / English version” links.
4. Canonical / hreflang / og:image use `https://sunzhengnj.github.io/ClockJoy/…` (EN: `/ClockJoy/en/guides/<slug>.html`, CN: `/ClockJoy/guides/<slug>.html`).
5. Update `sitemap.xml` (repo root) with **both** locale URLs and today’s `lastmod` (ISO date); bump the two guide-index `lastmod`s.
6. Update `en/guides/index.html` **and** `guides/index.html` (new guide-card first; refresh title/meta description).
7. Mark the topic `[done YYYY-MM-DD]` in `marketing/seo-geo/QUEUE.md`; keep at least three `[next]` items.
8. Append an entry to `marketing/seo-geo/LOG.md`.
9. Open a PR against `sunzhengnj/ClockJoy` `main` and merge (squash) so GitHub Pages picks up both locales; then confirm both URLs return 200.
10. Write **one overseas EN social draft only** under `marketing/posts/` (manual phone post), linking only `https://sunzhengnj.github.io/ClockJoy/…` or the App Store. Do **not** auto-post Xiaohongshu; do **not** change live App Store Connect metadata.

**Cadence:** one paired EN+CN theme per Mon/Fri fire. Do not spam thin pages. Public brand is ClockJoy / 开薪 only.

## Also write one social draft

After the SEO page steps (or when the SEO queue is blocked), write **one** social draft under [`../posts/`](../posts/) using [`../posts/QUEUE.md`](../posts/QUEUE.md). Do not publish until the user asks — drafts stay `draft`/`ready`; posting is browser + human-gated. See [`../posts/README.md`](../posts/README.md).

## GEO rules (generative engine optimization)

- Lead with a clear definition in the first 2–3 sentences (quotable by AI engines).
- Prefer FAQ blocks with short, self-contained answers; add FAQ JSON-LD when useful.
- Use comparison tables when the query implies “vs timesheet / payroll / calculator.”
- Explicit payroll disclaimer on every earnings-related page.
- Internal-link to related guides and the App Store.
- Canonical URLs under `https://sunzhengnj.github.io/ClockJoy/en/guides/…` and `https://sunzhengnj.github.io/ClockJoy/guides/…`.

## Quality bar

- Accurate product claims only (estimates, widgets, Live Activity / Dynamic Island, privacy-safe share cards).
- No competitor smears; no invented legal overtime math.
- Only ClockJoy / 开薪 in titles, descriptions, body, alt text, OG tags, or CTAs. Before merging, `grep -ri` the diff for any former product name and remove it.
- English for US/EN search intent; keep CN and EN in sync when both exist.

## Files

| Path (repo `sunzhengnj/ClockJoy`) | Role |
|------|------|
| `en/guides/*.html` | EN guides |
| `guides/*.html` | CN guides |
| `en/guides/index.html`, `guides/index.html` | Guide indexes |
| `sitemap.xml` | Sitemap |
| `marketing/seo-geo/PIPELINE.md` | This manual |
| `marketing/seo-geo/QUEUE.md` | Ordered topic backlog |
| `marketing/seo-geo/LOG.md` | Ship log (entries before 2026-10-23 refer to the old `docs/` layout) |
| `marketing/posts/` | Overseas EN social drafts + `QUEUE.md` / `LOG.md` / `README.md` |

## URLs after Pages deploy

- Site: https://sunzhengnj.github.io/ClockJoy/
- EN home: https://sunzhengnj.github.io/ClockJoy/en/
- EN guides index: https://sunzhengnj.github.io/ClockJoy/en/guides/
- CN guides index: https://sunzhengnj.github.io/ClockJoy/guides/
- US App Store: https://apps.apple.com/us/app/id6771261514
