# Contributing

## Editorial Standards

This project has one non-negotiable rule: **facts only, no fabrication.**

Every claim in every sequence must be verifiable from:

- Government reports and declassified documents
- Court filings and public legal proceedings
- Investigative journalism by established media organizations
- Academic or NGO research publications
- Publicly recorded speeches and events
- Official statistics and datasets

## What We Accept

- Corrections to factual errors (with source)
- New sequences or cases with complete source documentation
- Updates to existing content when new information becomes public
- Typo and formatting fixes
- Accessibility improvements

## What We Don't Accept

- Opinion pieces or editorializing
- Unverifiable claims or anonymous sources
- Content that incites violence, harassment, or illegal activity
- Fabrication of any kind — invented quotes, fake data, fictional events
- Content sourced from disinformation websites or unverified social media
- Copyright-infringing material

## Source Requirements

Every factual claim in a contribution must include:

1. A verifiable public source (URL, document reference, or publication date)
2. The source must be primary or reputable secondary (no aggregation sites, no social media posts as sole source)
3. Quotations must be exact transcriptions from the recorded or published source
4. Statistics must link to the original dataset or report, not a news article about the report

## How to Contribute

1. **Propose**: Open an issue describing the sequence, case, or correction you want to contribute, with your sources.
2. **Write**: Once discussed, create a single-file HTML sequence following the existing conventions in `AGENTS.md`.
3. **Submit**: Open a pull request with your sequence and source documentation.
4. **Review**: A maintainer will verify all claims against sources before merging.

## Sequence Conventions

See `AGENTS.md` for full architectural and stylistic conventions, including:

- Single-file HTML per sequence
- Two-layer architecture (terminal hook + editorial essay)
- Naming: `<episode>-<nn>-<case>.html` for episode sub-sequences
- Inline CSS is acceptable per sequence
- All fonts via Google Fonts CDN only

## License

By contributing, you agree that your work will be released under the project's MIT License.
