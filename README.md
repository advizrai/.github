# advizrai/.github

Org-level defaults for the [Advizr](https://advizr.ca) GitHub organization.

Nothing here is application code. Every file is either the public org profile or a community health
default that GitHub inherits into any repo in the org that does not define its own.

## What lives here

| Path | What it does |
|---|---|
| `profile/README.md` | The **public** org overview rendered at [github.com/advizrai](https://github.com/advizrai) |
| `profile/banner-light.svg`, `profile/banner-dark.svg` | Theme-aware banner for that page |
| `SECURITY.md` | How to report a vulnerability |
| `CONTRIBUTING.md` | Branch, commit, and review conventions |
| `SUPPORT.md` | Where to get help |
| `CODE_OF_CONDUCT.md` | Contributor Covenant 2.1 |
| `.github/ISSUE_TEMPLATE/` | Bug and feature forms |
| `.github/pull_request_template.md` | Default PR body |

## Two org profiles, not one

GitHub renders a different overview depending on who is looking.

| Viewer | What renders |
|---|---|
| Anyone on the internet | `profile/README.md` in this repo |
| Signed-in org members | A separate members-only profile |

This repo is the public one, and it is a credibility surface for prospects, partners, and candidates.
The members-only profile is the engineering front door: setup, architecture, conventions, and who
owns what. Internal detail belongs there and never here. See `handbook/15-github-org-profile.md` in
the agency knowledge base for how to reach it.

## Editing rules

- Never name a private client or a private repo in this repo. It is public. Speak to verticals
  generally. The full standard is `handbook/15-github-org-profile.md` in the agency knowledge base.
- Public copy follows `handbook/brand-positioning.md`. The headline is "You will have superpowers."
  and the subhead is "AI transformation for businesses that refuse to fall behind." Do not invent a
  third tagline.
- No fabricated testimonials and no invented metrics. The only quantified line is the guarantee,
  which is an offer rather than a client result.
- Changing a health file here changes the default for every repo in the org that lacks its own copy.
  A repo with its own `CONTRIBUTING.md` always wins.

## Banner

`profile/banner-*.svg` is traced from the Advizr mark and set in a system font stack. Palette is
ink `#14130F`, cream `#FAF8F5`, coral `#E66A6A`, and near-black `#0F0F11` for dark mode. It is an
interim asset. Replace it when the final brand kit lands.
