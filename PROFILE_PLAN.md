# NextMindHQ — GitHub Profile Plan v1.0

This document explains the reasoning behind the current profile, and lays out what to add next and in what order.

## Why this structure

The `.github` repository controls two things on GitHub: the organization's public profile page (via `profile/README.md`) and, later, org-wide community health files that apply to every repo that doesn't override them.

The README is deliberately narrow. It answers three questions in order — what NextMind is, what NextMind builds, how NextMind builds — and stops. No badges wall, no emoji list, no roadmap teaser. Companies like Vercel, Stripe, and Anthropic keep their org READMEs short because the profile's job is to establish credibility in the first ten seconds, not to document everything. Depth belongs in individual repos, a future website, and this plan document — not on the landing page.

The Business AI module table exists because it's the most concrete, verifiable proof of what NextMind builds. Abstract mission statements don't convince technical visitors; a list of named, single-purpose agents does.

Engineering Principles are included in full because they double as a signal to future engineers, collaborators, and technical hires about how the org actually operates — modular, deterministic, human-reviewed. That's differentiating in a market full of "AI-first, move fast, ship anything" positioning.

ShortFactory and StoryFactory are intentionally absent. They're not active products and showing them would misrepresent NextMind's current state.

## Sections to add later (not now)

Once there's real public traction, consider adding to the README:

- **Open Source** — if/when any NextMind repo is made public, a short section linking to it.
- **Team** — only once there's a public-facing team willing to be named; premature otherwise.
- **Status/Changelog link** — once NextMind OS or the website has a public changelog worth linking.
- **Careers** — once NextMind is actively hiring externally.

None of these should be added speculatively — each earns its place when the underlying thing exists.

## Pinned repositories (recommendation)

GitHub lets an organization pin up to 6 repositories at the top of its profile. Suggested priority once repos exist and are ready to show publicly:

1. **NextMind Business AI** — the flagship product, highest priority.
2. **NextMind Website** — the public face of the company.
3. **NextMind OS** — signals internal engineering maturity.
4. A representative individual agent module (e.g. Document AI Agent) if it's built as a standalone repo — shows modular architecture in practice.
5–6. Reserved for whatever ships next; don't pin placeholders or empty repos.

Only pin repos that are in a state you'd be comfortable with a stranger opening cold. An empty or half-built pinned repo undercuts the "production ready" positioning more than not pinning anything.

## Banner

Recommended spec:

- **Dimensions:** 1280×640px (GitHub social preview ratio), safe content area centered within ~1200×600px.
- **Background:** Graphite / near-black, consistent with the dark theme.
- **Content:** Wordmark "NextMind" in white, minimal accent line or mark in `#0F6E63`. No illustration, no gradient mesh, no stock-photo texture — flat and precise, in the spirit of Vercel/Supabase banners.
- **Typography:** A single geometric sans-serif (e.g. Inter, Geist, or similar), generous letter spacing, no tagline crowding the mark.
- **File:** SVG source kept in `assets/`, exported to PNG for upload to GitHub org settings.

This is currently a placeholder — see `assets/banner-placeholder.md` for the brief. Actual banner creation is a design task, not something to generate ad hoc as a raster image inside this repo.

## Avatar

Recommended spec:

- **Format:** Square, minimum 460×460px (GitHub org avatar requirement), SVG source if available.
- **Content:** A standalone mark, not the full wordmark — wordmarks compress badly at 32px favicon size. Either a monogram ("N" or "NM") or a simple abstract glyph, in white or `#0F6E63` on graphite, or graphite on white for light-context surfaces (favicons, social cards).
- **Constraint:** Must remain legible at 16×16px (browser tab favicon size). Test at that size before finalizing — this is where most startup avatars fail.

## GitHub Features — rollout priority

Ordered by leverage vs. effort, not by how commonly companies enable them:

**Phase 1 — now / this repo**
- `profile/README.md` — done.
- Org description, URL, and avatar in GitHub org settings — low effort, immediate credibility gain.

**Phase 2 — as soon as any repo goes public**
- `CODEOWNERS` — cheap, prevents unreviewed merges once there's more than one contributor.
- Pull Request Templates — keeps PR quality consistent from day one.
- Issue Templates — same reasoning, and helps if external users ever file issues.
- `SECURITY.md` — matters the moment any repo handles user data or is public; cheap to write, costly to be missing when someone needs it.

**Phase 3 — once there's external usage or contributors**
- `CONTRIBUTING.md` at the org level (community health default) — see the repo-level file for the current draft; promote it org-wide once there's an actual external contribution flow.
- Discussions — enable once there's a community to talk to (ties to NextMind Community).
- Releases — enable per-repo once versioned software ships, not before.

**Phase 4 — later / as scale demands**
- Wiki — usually redundant with good README + docs; only add if documentation outgrows what fits in-repo.
- Projects (GitHub Projects) — useful once roadmap needs to be public or cross-repo; internal roadmap tools may cover this need first.
- `FUNDING.yml` — only relevant if NextMind wants to surface sponsorship/funding links; not a near-term priority.

The guiding rule: enable a feature when there's a real audience or workflow for it, not preemptively. An org with SECURITY.md, CODEOWNERS, and Discussions but zero real activity behind them looks less credible than one with fewer files and real signal.

## Open question for Nico

- Should the org profile stay effectively "stealth-lite" (current approach: mission + Business AI, no public repos yet) until NextMind Website and at least one public repo are ready? Recommended: yes — publishing a polished profile pointing at nothing tends to read as smaller than saying less and being ready when repos go public.
