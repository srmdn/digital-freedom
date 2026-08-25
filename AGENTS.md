# AGENTS.md — Digital Freedom

> Repository constitution for humans and AI agents working on this project.
> Public-facing editorial standards live in `EDITORIAL.md`; contributor workflow in `CONTRIBUTING.md`.
> Private strategy and roadmap live in `.local/` (gitignored).

## Identity

Originally created around the 2026 Digital Freedom Contest; now maintained as a long-term independent archive documenting digital freedom, privacy erosion, surveillance, censorship, and related technologies through unconventional interactive narratives.

**Vision**: go-to archive for digital freedom stories in unconventional format.
**Layers**: Editorial landing page (credible, readable) → Terminal sequences (raw, immersive).
**Principle**: Cinematic presentation. Forensic discipline.
**Live**: https://srmdn.github.io/digital-freedom/

## Architecture

- **Zero third-party runtime dependencies** — self-hosted fonts only (`assets/fonts/`), no Google Fonts requests, no analytics, no trackers, no remote JavaScript libraries unless explicitly justified. The website practices the privacy principles it advocates.
- **Single-file HTML per sequence** — `sequences/<name>.html`, zero build system
- **Editorial landing page** — `index.html` (serif headlines, sans-serif body, dark theme, accent: `#c0392b`)
- **Deployment**: GitHub Pages, permanently. Auto-deploy via `.github/workflows/pages.yml` on push to master. No VPS migration is planned.
- **Static legal/info pages**: `disclaimer.html`, `privacy.html` mirror the .md equivalents.

## Information architecture

Episodes contain cases. Each case is one self-contained sequence file.

- **Episode I — State of Digital Freedom**: `freedom-report.html` (The Ship Has Already Hit the Iceberg)
- **Episode II — Pegasus**: `pegasus-01-khashoggi.html`, `pegasus-02-sanchez.html`, `pegasus-03-50k-list.html`, `pegasus-04-zero-click.html`, `pegasus-05-rehabilitation.html`
- **Episode III — Encryption Wars**: planned
- **Episode IV — Mass Surveillance / Snowden**: planned
- **Episode V — Data Brokers**: planned

Naming: `<episode>-<nn>-<case>.html`. Do not rename existing files without a strong reason.

## Evidence discipline — the core editorial system

Every material claim in a sequence belongs to one of these classes:

1. **FACT** — directly established by reliable public evidence.
2. **FORENSIC FINDING** — established through technical analysis, device forensics, network analysis, or comparable technical investigation.
3. **ALLEGATION** — a claim made by an identified party that has not necessarily been judicially or independently established.
4. **ATTRIBUTION** — an assessment linking an activity, exploit, operator, organization, or government to an event. Attribution must identify who made the attribution.
5. **EXPERT INTERPRETATION** — interpretation from a researcher, lawyer, NGO, journalist, academic, security expert, or other identified expert.
6. **EDITORIAL INFERENCE** — a conclusion Digital Freedom derives from established evidence. Allowed, but must not masquerade as a directly established fact.

### Never silently promote evidence

- targeting → successful compromise
- selected phone number → infected device
- attempted exploit → successful exploit
- allegation → established fact
- operator attribution → proven state responsibility
- correlation → causation
- nationality → physical location
- corporate infrastructure behavior → individual employee behavior
- jury award → final/current judgment
- proposed legislation → enacted law
- expert interpretation → official finding
- evidence raising questions → definitive proof
- lack of visible indication → absence of forensic traces

### Editorial rule

No fabricated facts, quotations, events, chronology, causal relationships, attribution, or certainty. Editorial interpretation is allowed when clearly distinguishable from established fact and grounded in cited evidence.

### Language discipline

- targeted vs compromised
- selected vs infected
- alleged vs established
- proposed vs enacted
- attributed vs proven
- jury verdict vs final judgment
- no visible indication to the target ≠ no forensic trace
- "The pretext is always children" is attributed Durov rhetoric, not a Digital Freedom universal conclusion

## Conventions

- Runtime: flexible. Shorter for concise cases, longer for complex narratives. No fixed duration.
- Fonts: JetBrains Mono (terminal), Source Serif 4 + Source Sans 3 (editorial), Special Elite + Cutive Mono (dossier variants) — all self-hosted.
- Dark terminal aesthetic: `#0c0c0c` background, scanline overlay, color-coded types (command, alert, critical, quote). Each sequence may use its own aesthetic (classified intel, CRT retro, etc.).
- No monolithic CSS — per-sequence inline `<style>` is acceptable (exception to per-page CSS rule).
- Every sequence must carry:
  - episode/case context breadcrumb ("Episode II / Pegasus / Case 04 of 05")
  - prev/episode/next navigation inside multi-case episodes
  - publication metadata block: Last reviewed + Evidence current through (Published only when the date is reliably known from git history)
  - simulated-interface clarification (see below)
- Use the latest trusted sources whenever possible — current reports, updated datasets, recent reporting over older materials when both exist.
- Data sections must identify each dataset: report name, edition/year, what it measures, score direction, access/review date. Never present different indices as normalized equivalents.

### Simulated interfaces

The classified-document, CIA-file, and intelligence-dossier aesthetics are **editorial presentation devices**, not leaked government documents. Every sequence using such an aesthetic must carry a subtle, discoverable note (in the terminal hook and/or disclaimer): interface is fictional presentation; underlying events and evidence are sourced from public records.

## Directory

```
.github/workflows/pages.yml  — auto-deploy GitHub Pages
index.html                   — editorial landing page (episode/case hierarchy)
sequences/                   — one .html per case
assets/                      — self-hosted fonts + fonts.css
EDITORIAL.md                 — PUBLIC editorial & sourcing methodology
CONTRIBUTING.md              — PUBLIC contributor workflow
DISCLAIMER.md / PRIVACY.md   — public legal/info (mirrored as .html)
LICENSE                      — MIT
docs/PRODUCTION.md           — PRIVATE (gitignored): strategy, roadmap, sources, changelog
research/                    — PRIVATE (gitignored): per-episode source tracking
.local/                      — PRIVATE (gitignored): local roadmap and task state
AGENTS.md                    — this file
```

## Source tracking (for local agents)

Keep a private source file per episode under `research/` (gitignored, never committed):

```
research/pegasus.md
research/freedom-report.md
```

Track per source: title, publisher, URL, publication date, access date, which claim it supports. Do not copy entire copyrighted articles into the repository. Public sequences cite sources inline via `.source-ref` links; private research files are for working provenance, not publication.

## Private vs Public

- `docs/PRODUCTION.md`, `research/`, `.local/` — gitignored. Contain strategy, roadmap, source materials, changelog.
- `EDITORIAL.md`, `CONTRIBUTING.md`, `README.md`, `DISCLAIMER.md`, `PRIVACY.md`, `LICENSE` — public. Public documentation must never require reading a private file.
- Never commit: contest deadlines, future domains, unpublished sequence ideas, private research files.

## Workflow

1. Create/edit case in `sequences/`
2. Update episode index in `README.md` and `index.html`; add URL to `sitemap.xml`
3. Check HTML tag balance; verify every cited source URL loads
4. Push to master → auto-deploys via GitHub Pages
5. (Legacy contest workflow) For video production: screen record sequence playback, add background audio in editor, export

## Git

- History force-pushed 2026-06-16 → clean single-commit baseline. Do not force-push again.
- Config: `srmdn` / `mail@saidwp.com` (set per-repo before first commit)
- Keep commits small and traceable — logical commits like `docs:`, `site:`, `audit:`, `a11y:`, `seo:`
- Git history is part of the corrections audit trail

