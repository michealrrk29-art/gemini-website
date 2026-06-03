# Microelectronics Section — Design

**Date:** 2026-06-03
**Site:** Gemini Commercial Broker (gemini-cb.ae) — static HTML/CSS/JS, no build step, Cloudflare Pages from `main`.

## Goal

Present a new business line: Gemini as a professional broker for the supply of
microelectronics component base, holding **direct long-term contracts with
manufacturing plants and FABs**. Language: English (matches the rest of the site).
Tone: premium, discreet, consistent with existing sections.

## Scope

A dedicated page `/microelectronics/index.html` plus a teaser block and nav entry
on the homepage. Reuse existing CSS classes — minimal-to-no new CSS.

### In scope
1. New page `/microelectronics/index.html`.
2. Homepage teaser section + new nav link.
3. `sitemap.xml` entry.

### Out of scope (YAGNI)
- No Track Record case for microelectronics.
- No component catalog / pricing / part-number search.
- No new contact forms — reuse existing WhatsApp + email.
- No new fonts or color tokens.

## 1. New page `/microelectronics/index.html`

Full standalone HTML page mirroring `index.html` head/header/footer, with its own
SEO/OG metadata.

**Head:** own `<title>`, `<meta description>`, and `og:*` tags focused on
microelectronics component sourcing. Same favicon/font/stylesheet links as homepage
(absolute paths, so they resolve from the subdirectory).

**Header:** same `site-header` markup as homepage. Nav links point back to
homepage anchors with absolute paths (`/#track-record`, etc.); the Microelectronics
link points to `/microelectronics/`.

**Page body sections (reusing existing classes):**

1. **Hero** (`section .section-dark` or `hero` pattern)
   - Eyebrow: "Component Sourcing · Microelectronics"
   - Title: brokerage of microelectronics component base
   - Lede: direct, long-term contracts with manufacturers and FABs; structured
     cross-border supply.

2. **What we source** (`geo-grid`, 2 cards)
   - *Semiconductors & ICs* — microprocessors, MCUs, memory, FPGA/ASIC, analog and
     power ICs.
   - *Wafers & FAB-grade materials* — wafers, substrates, production-grade
     materials and chemistry.

3. **Why Gemini** (`practice-list`, 3 items) — core positioning
   - *Direct factory & FAB contracts* — long-term direct agreements with
     producers and FABs; no grey market, no intermediary chains.
   - *Authenticity & traceability* — provenance traceable to the factory,
     counterfeit protection, certificates of origin.
   - *Cross-border settlement & logistics* — payment structuring and delivery
     across constrained jurisdictions (ties to Gemini's core strength).

4. **Contact CTA** (`section-contact` pattern or simple CTA)
   - WhatsApp + email buttons reusing existing contact endpoints
     (`https://wa.me/971505279506`, `mailto:info@gemini-cb.ae`).

**Footer:** same `site-footer` markup as homepage.

## 2. Homepage `index.html`

- **Nav:** add `<a href="/microelectronics/">Microelectronics</a>` to `.site-nav`
  (becomes 6 links).
- **Teaser section:** insert a new `<section>` immediately **after** the `#practice`
  section and before `#insights`. Contains eyebrow, short title, 1–2 sentence lede,
  and a `btn btn-ghost` "Explore microelectronics →" linking to `/microelectronics/`.
  Use alternating section background to keep the dark/light rhythm correct (practice
  is `section-dark`, so teaser is light `section`, insights stays `section`). Verify
  rhythm during implementation and adjust the insights/contact classes only if the
  alternation breaks.

## 3. `sitemap.xml`

- Add `<url><loc>https://gemini-cb.ae/microelectronics/</loc></url>` with
  `lastmod` 2026-06-03, consistent with existing entries' format.

## Success criteria

- `/microelectronics/` renders with correct styling (no new CSS required, or only
  trivial additions), header/footer/nav consistent with the rest of the site.
- Homepage teaser links correctly; nav link works from both homepage and subpage.
- Dark/light section alternation on the homepage remains visually correct.
- sitemap.xml is valid and includes the new page.
- Local preview (`python3 -m http.server 8000`) shows all of the above.

## Testing

Manual verification via local static server: load `/`, confirm nav + teaser +
alternation; load `/microelectronics/`, confirm all sections render and CTAs/links
resolve. Validate sitemap.xml is well-formed.
