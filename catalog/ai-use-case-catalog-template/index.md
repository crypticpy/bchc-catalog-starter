---
layout: entry
render_with_liquid: false
title: AI Use Case Catalog template
slug: ai-use-case-catalog-template
published: "2026-08-18"
featured: false
thumbnail: ""
organization: Big Cities Health Coalition
solution_type: Source code
use_case_category: Communications, media & writing
area:
  - Staff & partner coordination
  - Data & informatics
stage: In production
summary: "A GitHub-Pages catalog template for sharing AI use cases across health departments. Entries are submitted through a form that opens a GitHub issue, reviewed as a pull request, and published on merge — no server, no database, no CMS login."
impact: A member catalog goes from template to live, configured site in about 40 minutes.
review_status: Under review
ai_role: AI was used to build it
ai_types:
  - Generative text (LLM)
ai_tools:
  - "None at run time — the site itself runs no AI"
  - "Claude Code (an LLM coding agent) during development — behind the same lint/test/build gates as any human change"
platform:
  - Vendor / SaaS hosted
vendor: GitHub (Pages hosts the site, Actions runs the issue-to-pull-request automation)
expertise: Power user
readiness:
  - Guided setup
repo_url: "https://github.com/crypticpy/bchc-template"
demo_url: "https://crypticpy.github.io/bchc-template/"
docs_url: "https://github.com/crypticpy/bchc-template/blob/main/docs/launch.md"
resources:
  - label: A fresh copy on day one
    url: "https://crypticpy.github.io/bchc-catalog-starter/"
  - label: Configuration reference
    url: "https://github.com/crypticpy/bchc-template/blob/main/docs/configuration.md"
  - label: Content model
    url: "https://github.com/crypticpy/bchc-template/blob/main/docs/content-model.md"
screenshots: []
deck_pdf: "/catalog/ai-use-case-catalog-template/deck.pdf"
license: MIT
access_terms: ""
portability: "Partially — with rework"
portability_notes: "The site is plain Jekyll and builds anywhere Ruby runs. The submission workflow (issue form → pull request → merge) is written for GitHub Actions and GitHub Pages; moving to another host means replacing that half."
reused_from: []
cost_band: No new spend
run_cost: No ongoing cost
procurement:
  - No procurement needed
approvals: []
equity_note: ""
no_pii_attestation: true
data_sensitivity:
  - Public data only
data_sources:
  - Entry metadata contributors type into the submission form (titles/summaries/links/contact details they choose to publish)
  - Nothing is collected from readers
audience: Public-facing
data_governance_notes: The catalog is public by design. The submission form tells contributors not to include protected health information, credentials or non-public data, and a maintainer reviews every entry in a pull request before it publishes.
contact_name: BCHC catalog template maintainers
contact_title: ""
contact_email: "info@bigcitieshealth.org"
---

## What it is

A template for a public catalog of AI use cases, built for the Big Cities Health Coalition's AI community of practice and reusable by any member health department. Create a repository from it, answer the setup wizard's questions, and you have a searchable, filterable catalog on GitHub Pages: entry pages, cards, facet filters, a search index and a submission form, all driven by one content model in `_data/schema.yml`.

## How it works

- **No server.** The site is static Jekyll, hosted on GitHub Pages. There is nothing to patch, back up or pay for.
- **Submissions are issues.** The `/submit/` form pre-fills a GitHub issue; a workflow turns the issue into a pull request containing the entry's front matter and screenshots. A maintainer reviews the checklist and merges. The site rebuilds itself.
- **Everything reads the schema.** The entry page, the cards, the filter panel, the search index, the web form, the GitHub issue form and CI validation all iterate the same field list, so a department can rename, add or remove fields without touching a template.
- **Reviewable by design.** Every change to content or configuration arrives as a pull request. The setup wizard's output can be applied the same way.

## What it takes to reuse

- A GitHub organization that can host a public repository, and about 40 minutes.
- Three repository settings (Pages source, Actions may open pull requests, the content labels) — the launch guide walks through them.
- No terminal is required; every step can be done in a browser.

## Data

The template touches no health data. Entries are public metadata that contributors choose to publish; the submission form and review checklist exist to keep protected or non-public information out.

## This entry

This catalog is itself a fresh copy of the template — configured through the setup wizard, sample content removed, and this entry published through the same issue form any submitter would use.
