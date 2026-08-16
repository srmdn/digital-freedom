# Contributing

Digital Freedom is a static editorial archive: dark editorial landing page, terminal and intelligence-dossier sequences, single-file HTML, self-hosted fonts, no third-party runtime dependencies. Read [EDITORIAL.md](EDITORIAL.md) for the editorial methodology before contributing content.

## Editorial standards

The project's rule is: **no fabricated facts, quotations, events, chronology, causal relationships, attribution, or certainty.** Editorial interpretation is allowed when clearly distinguishable from established fact and grounded in cited evidence.

- Unsupported editorializing presented as fact is not accepted.
- Editorial analysis is accepted when it is evidence-based, clearly identifiable, properly sourced, logically derived, and not presented with false certainty.
- Distinguish fact from inference. Every material claim is either a sourced FACT, a FORENSIC FINDING, an ALLEGATION by an identified party, an ATTRIBUTION that names who made it, an EXPERT INTERPRETATION, or an EDITORIAL INFERENCE — and must be written so the reader can tell which.

Examples of silent evidence promotion that will be rejected:

- "targeted" presented as "compromised"
- "selected phone number" presented as "infected device"
- "proposed legislation" presented as "enacted law"
- "jury award" presented as "final judgment"
- "attributed by researchers" presented as "proven state responsibility"

## What we accept

- Corrections to factual errors (with source)
- New sequences or cases with complete source documentation
- Updates to existing content when new information becomes public
- Typo and formatting fixes
- Accessibility improvements

## What we don't accept

- Fabrication of any kind — invented quotes, fake data, fictional events
- Unverifiable claims or anonymous sources
- Content that incites violence, harassment, or illegal activity
- Content sourced from disinformation websites or unverified social media
- Copyright-infringing material

## Source requirements

Every factual claim in a contribution must include:

1. A verifiable public source (URL, document reference, or publication date)
2. A primary or reputable secondary source — no aggregation sites, no social media posts as sole source
3. Quotations as exact transcriptions from the recorded or published source
4. Statistics linked to the original dataset or report, not a news article about the report
5. The latest trusted source when both exist — current reports, updated datasets, and recent reporting over older materials

## Sequence conventions

- **Single-file HTML per sequence** in `sequences/` — no build system, no framework
- **Two-layer architecture**: interactive terminal/dossier hook → full editorial essay with inline source markers (`.source-ref`)
- **Naming**: `<episode>-<nn>-<case>.html` for episode sub-sequences
- **Fonts**: self-hosted only (JetBrains Mono, Source Serif 4, Source Sans 3, Special Elite, Cutive Mono in `assets/`). No Google Fonts CDN requests.
- **No third-party runtime dependencies**: no analytics, no trackers, no remote scripts or assets
- **Inline CSS** is acceptable per sequence
- Every sequence must carry:
  - episode/case context ("Episode II / Pegasus / Case 04 of 05")
  - prev/episode/next navigation inside multi-case episodes
  - publication metadata block (Last reviewed + Evidence current through; Published only when reliably known)
  - a note that classified/dossier interfaces are editorial presentation devices
- Data sections must identify each dataset: report name, edition/year, what it measures, score direction, access/review date. Never present different indices as normalized equivalents.

## How to contribute

1. **Propose**: Open an issue describing the sequence, case, or correction you want to contribute, with your sources.
2. **Write**: Create a single-file HTML sequence following these conventions and [EDITORIAL.md](EDITORIAL.md).
3. **Submit**: Open a pull request with your sequence and source documentation.
4. **Review**: A maintainer will verify all claims against sources before merging.

## Corrections

Material factual errors are corrected transparently. See the corrections section in [EDITORIAL.md](EDITORIAL.md). Report errors via the issue tracker with the claim, the contradicting source, and the affected sequence.

## License

By contributing, you agree that your work will be released under the project's [MIT License](LICENSE).
