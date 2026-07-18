# Morgan's Second Brain

A structured knowledge base ingested from past Claude chats, artifacts, and Google Drive.
Built 2026-07-18. Most project state is current as of 2026-07-17 (the last Project Status Board rebuild).

> ⚠️ **PRIVATE — do not publish.** This directory contains legal/clemency details, personal
> contacts, board finances, immigration information, and unpublished research. It lives on the
> `claude/second-brain-ingestion-tn4wck` branch, which does **not** deploy (GitHub Pages builds
> from `main`). **Do not merge this folder into `main`** — the site at `morgangodvin.github.io`
> would serve it publicly. If you want this to be durable, move it to a separate **private** repo.

## What this is

A "second brain" pass over everything I could reach from your past work: 15 published artifacts,
your Google Drive, and the two living dashboards you maintain (the Project Status Board and the
DCLA Work Products board). It reorganizes that scattered material into a browsable, cross-linked
set of notes so any future chat can pick up context fast.

## How it's organized

| Path | What's in it |
|------|--------------|
| [`profile.md`](profile.md) | Who you are, roles, affiliations, identity anchors |
| [`projects/_index.md`](projects/_index.md) | The full project portfolio with live status |
| `projects/*.md` | One note per active project |
| `knowledge/*.md` | Durable research findings (the drug-policy data work) |
| [`people.md`](people.md) | Key collaborators and contacts |
| [`organizations.md`](organizations.md) | Orgs you work with |
| [`sources.md`](sources.md) | Where everything physically lives (Drive, Canva, Figma, artifacts, repos) |

## Ingestion decisions

**Ingested** (high-signal, durable, or actively referenced):
- All 12 active projects from the Project Status Board
- The 4 research knowledge products (fentanyl purity DB, fentanyl epi-timing dashboards,
  THC/FTIR briefing, MME estimation)
- DCLA's work-product structure and external asset homes
- The harm-reduction influencer-landscape synthesis (D4DPR deliverable)
- People / org / source maps

**Noted but not deep-ingested** (working tools, one-offs, or superseded):
- DCC + OD2A budget workbench, FTE reconciliation, budget-scenario artifacts → pointers in
  [`projects/california-cannabis-dcc-grant.md`](projects/california-cannabis-dcc-grant.md) and the UCLA note
- Agent Channel Launch Plan, usage_dashboard, DCLA site-search preview, ER illustration,
  status-pill check → these are UI/experiment artifacts, listed in [`sources.md`](sources.md) only
- Coursework docs (CPH528), raw scan folders → pointers in the relevant project notes

## Maintenance

The two dashboards (`Project Status Board`, `DCLA Work Products`) remain the *live* source for
day-to-day status and email snapshots. This second brain is the *durable* layer underneath them —
update it when a project's shape changes, not on every email.
