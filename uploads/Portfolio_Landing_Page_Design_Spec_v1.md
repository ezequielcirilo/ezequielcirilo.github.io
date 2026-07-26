# PORTFOLIO SITE — Landing Page
## Design & Build Handover Specification

**Status:** Ready for build
**Version:** 1.0
**Date:** July 2026
**Owner:** Ezequiel Cirilo
**Target:** Claude Design — generate a production-ready, single-page portfolio landing page
**Deployment target:** Static site on GitHub Pages or Cloudflare Pages (free tier)

---

## 1. Purpose & Audience

Personal portfolio for an AI Product Leader actively job seeking in Ireland. The primary reader is a recruiter or hiring manager who already has the owner's name (from LinkedIn or an application) and is deciding whether to interview. The page must communicate, within 10 seconds of landing: senior AI product credibility, a distinctive thesis (human-in-the-loop AI), and hard metrics.

Secondary jobs: deep case study showcase (case study pages will be added later as separate pages) and personal brand hub.

Tone: confident, precise, evidence-led. No buzzword filler. The copy provided in Section 4 is final and must be used verbatim unless a layout constraint forces truncation, in which case flag rather than rewrite.

## 2. Technical Constraints

- Static HTML/CSS/JS or a single-page React build that compiles to static assets. No backend, no CMS, no database.
- Must deploy cleanly to GitHub Pages or Cloudflare Pages: relative asset paths, no server-side rendering dependencies.
- No localStorage or sessionStorage.
- Fully responsive: mobile-first, tested at 375px, 768px, 1440px.
- Fast: no heavy animation libraries, no video backgrounds. Lighthouse performance 90+.
- Semantic HTML with accessible landmarks; alt text on all logos and images.
- SEO basics: title tag ("Ezequiel Cirilo — AI Product Leader"), meta description drawn from the hero supporting line, Open Graph tags.
- Navigation: sticky top nav with anchor links to sections (Work, Case Studies, Brands, About) plus a "Get in touch" button. Case study card links can point to placeholder routes (/case-studies/benchmark-builder, /case-studies/video-redaction, /case-studies/ai-qa) — pages to be delivered in a later phase; use a "Coming soon" state, never a dead link.

## 3. Page Structure & Layout Guidance

Section order (single page, top to bottom):

1. **Hero** — full-viewport or near-full. Name, subtitle, headline statement as the dominant element, supporting line, two CTAs (primary: View case studies → anchors to Section 4; secondary: Get in touch → mailto). Include a subtle "Download CV" text link.
2. **Thesis** — short text section, generous whitespace, reads as a manifesto. Stack line rendered as a single small-type row of tool names beneath it (plain text, no logo cards, no descriptions).
3. **What I've Built** — six items as a 2×3 or 3×2 card grid on desktop, single column on mobile. Each card: bold label + one-line description with metrics visually emphasised (e.g. metric figures in accent colour or heavier weight).
4. **Case Studies** — three cards, horizontal row on desktop. Each: title, hook paragraph, "Read case study" link (Coming soon state).
5. **Brands & Industries** — single flat logo grid grouped by industry with small industry sub-labels. NO tabs, NO carousel: all logos visible at once. Logos greyscale, consistent sizing, on light card backgrounds. Six industry groups in this order: Insurance, Banking, Energy, Pension, Education, Sports Betting.
6. **Testimonials** — stacked or two-up static layout. NO carousel. One confirmed quote plus two visually lighter placeholder slots (design them so removing or filling them later is trivial).
7. **About & Contact** — short text block plus contact row: email, LinkedIn, Download CV button. Footer with copyright line.

## 4. Final Copy (verbatim)

### 4.1 Hero
- H1: Ezequiel Cirilo
- Subtitle: AI Product Leader
- Headline statement: I build AI products people actually trust in production.
- Supporting line: Human-in-the-loop systems where AI suggests, humans decide, and every decision is auditable. Most recently Head of Product Enablement & Delivery at Global Reviews, leading AI product development across a research and competitive intelligence SaaS platform.
- Primary CTA: View case studies
- Secondary CTA: Get in touch

### 4.2 Thesis
Heading: Why human-in-the-loop

Body: Most AI products fail at the trust layer, not the model layer. An AI suggestion that is only 50% accurate can still transform a workflow, if the review experience lets humans confirm, correct, and override it quickly, and every dismissal is logged. That is the pattern behind everything I have built: audit automation, video redaction curation, duplicate detection, respondent quality monitoring. AI does the volume. Humans own the judgement.

Stack line: Working with: Anthropic Claude · OpenAI GPT · Amazon Rekognition · AWS AI services · UserZoom · Power BI · Figma

### 4.3 What I've Built
Heading: What I've built

1. AI audit agents — Led the integration of an agentic, multi-model LLM system automating website feature audits: 93% of AI assessments confirmed correct at QA, 63% reduction in audit costs and manual assessment time.
2. AI QA Copilot — Shipped a QA copilot combining LLM reasoning, image analysis, and human-in-the-loop review: QA cycle time cut 69%, QA costs cut 61%, 87% of AI suggestions approved without correction.
3. Respondent quality monitoring — Led 0-to-1 delivery of an AI module screening study data for non-genuine responses, with inline evidence and human review of every exclusion.
4. Video intelligence — Launched an AI platform extracting usability KPIs (satisfaction, ease, confidence, success) from moderated research sessions.
5. PII redaction curation — Designed an AI-suggested redaction workflow where nothing is published without explicit curator sign-off.
6. Platform strategy — Cut infrastructure costs 74% through a full platform rebuild strategy that designed out the legacy cost base.

### 4.4 Case Studies
Heading: Case studies

Card 1 — Benchmark Builder
Removing a human bottleneck without removing human judgement. How a benchmark creation process moved from Excel-and-email round-trips to a governed, self-serve builder with AI duplicate detection and a full decision audit trail.

Card 2 — AI Video Redaction
Publishing research recordings safely at scale. An AI-suggested PII redaction workflow where curators confirm, correct, or reject every suggestion, and unredacted content can never reach the wider team.

Card 3 — AI-Assisted Quality Assurance
From 50% AI accuracy at launch to 87% of suggestions approved without correction. How the review experience, not the model, turned an unreliable AI into a copilot Quality Analysts trust across 3,000 criteria decisions per study.

### 4.5 Brands & Industries
Heading: Brands that made decisions with insights from my platforms

- Insurance: Allianz · AIG · Liberty Insurance · RACQ · Irish Life Health · Génesis by Liberty Seguros · Medibank
- Banking: Nationwide · NAB · St. James's Place · Vanguard · TD Bank
- Energy: EnergyAustralia · Origin · Bord Gáis Energy · Energia · Power NI · SSE
- Pension: AustralianSuper · Rest · Australian Retirement Trust · QSuper · Sunsuper
- Education: University College Cork · The University of Sydney · University of New England · Griffith University · Deakin University · UNSW Sydney
- Sports Betting: 888 · Ladbrokes · William Hill · Coral · bwin · Sportingbet · BetMGM

Logo assets: to be supplied by owner (greyscale versions from existing site plus new Sports Betting and Medibank logos). Until supplied, render brand names as styled text chips in the same grid layout.

### 4.6 Testimonials
Heading: What it's like to work with me

Testimonial 1 (confirmed):
"There are very few that I can compare with Ezequiel's natural talent for digital product management. His ability to understand the underlying needs of an organization and translate these business requirements into actionable steps that can be effectively produced by a software development team is rare."
— Katie Gandomi, Co-Founder at Avantsoft

Testimonials 2 and 3: placeholder slots. Placeholder text: "More recommendations on the way." Keep visual weight low.

Link below section: See more recommendations on LinkedIn → https://ie.linkedin.com/in/ezequielcirilo

### 4.7 About & Contact
Heading: About

Body: Product leader based in Ireland. I have spent my career at the intersection of research operations, UX, and applied AI, taking products from zero to production across Insurance, Banking, Energy, Pension, Education, and Sports Betting.

I also run an AI-native design workflow: production-ready UI designs and developer documentation generated directly from product specs with Claude Design, replacing the traditional Figma cycle. This site was built the same way.

Open to AI Product Manager, Senior Product Manager, and Product Lead roles in Ireland (Dublin, Cork, or remote).

Contact row:
- Email: ezequiel.cirilo@gmail.com (mailto link)
- LinkedIn: https://ie.linkedin.com/in/ezequielcirilo
- Download CV: link to /assets/Ezequiel_Cirilo_CV.pdf (asset supplied by owner)

## 5. Visual Direction

- Aesthetic: modern, editorial, confident. Closer to a well-designed AI product marketing page than a template portfolio. Avoid: stock illustrations, gradient blobs, emoji, skill progress bars.
- Strong typographic hierarchy: the hero headline statement is the visual anchor of the page.
- One accent colour used sparingly for metrics, CTAs, and links. Neutral palette otherwise (dark text on light background; a dark hero variant is acceptable).
- Metrics (93%, 63%, 69%, 61%, 87%, 74%) should be visually scannable across the What I've Built grid.
- Logos strictly greyscale for visual calm and equal treatment.
- Generous whitespace; the page should feel curated, not dense.

## 6. Assets Required From Owner

1. Greyscale brand logos (existing site set + Sports Betting brands + Medibank).
2. Profile photo (optional; if used, hero or About only, professional crop).
3. CV PDF (Ezequiel_Cirilo_CV_v3) placed at /assets/Ezequiel_Cirilo_CV.pdf.
4. Favicon (initials mark acceptable; can be generated in the build).

## 7. Out of Scope (This Phase)

- Case study pages (three planned; routes reserved, "Coming soon" state in this phase).
- Blog or writing section.
- Analytics (can be added later via a single script tag; do not block on it).
- Custom domain (site launches on the free Pages subdomain).

*End of specification — Portfolio Landing Page v1.0*
