# Micheal Roark / Deal Architect — v1

Standalone personal site, English-first, static HTML/CSS/JS. No dependencies or build step. Gemini corporate files and main are unchanged.

## Preview
Serve dist with any static server. Hosted review: https://micheal-roark.ochrebloom32.chatgpt.site (owner-private).

## Features
Eight individually flipping keyboard-accessible cards; responsive 4/2-column layout; reduced-motion support; native accessible proposal dialog; category-prefilled brief; explicit WhatsApp/email handoff; clipboard fallback; downloadable office-labelled vCard; QR SVG.
No backend, analytics, cookies, submission storage or automatic sending. Office contacts are taken from the existing Gemini website; personal phone/email remain unconfirmed. No claim that an enquiry was delivered.

## Separate Cloudflare Pages deployment
Create a NEW Pages project; do not edit the Gemini project or its domain.
- Current GitHub branch: mikhail/deal-architect-v1
- Root directory: personal-deal-architect
- Build command: exit 0
- Output directory: dist
- Production branch for the NEW project only: mikhail/deal-architect-v1
Alternatively copy this directory into a dedicated repository and use its main branch. The GitHub connector cannot create repositories, so this is an isolated branch/folder pending a dedicated repo.
Cloudflare account access is not available in this session. Configuration verified against https://developers.cloudflare.com/pages/framework-guides/deploy-anything/ . No Cloudflare deployment has been performed.

Before public release: choose final domain or pages.dev address; regenerate qr.svg and update contact.vcf URL to public origin; confirm whether enquiries should use the Gemini office or personal contact details. The current QR points to the private review URL and is not the print master.

## Verification
JS syntax and static assertions checked. No browser automation capability supplied under the managed Sites workflow, so mobile visual QA and interactive browser testing remain unverified. Check 390px, 768px and 1440px; flip/close cards using Enter and Escape, Tab focus, open/close dialog, required validation, brief special-character encoding, WhatsApp/email handoff, copy fallback and vCard import before public launch.

Sources: supplied October 9 decisions; Notion personal-brand page 3bd55da7afb6810fbce4ccb6f3a26b2d; Gemini index.html for office contacts. No confidential deal amounts or counterparties included.
