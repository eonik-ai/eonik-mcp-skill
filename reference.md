# eonik: the tools

The live list comes from the person's eonik connection (`tools/list`); this is a map of it, not
a second schema. `tests/test_the_skill_names_only_served_tools.py` in eonik-backend fails when this
file names a tool the server does not serve.

## The work (run in the person's eonik app, signed in to this connection's account)

| Tool | What it does |
|---|---|
| `get_adapts_status` | Where things stand: what needs the person, what is being made, what came back, which of their computers has eonik open |
| `find_creatives` | Finds creatives by name, project or theme in the folders linked in eonik |
| `make_adapts` | Opens eonik's own review of a creative's sizes (the sizes named, or the person picks from eonik's); nothing is made until the person presses Make |
| `revise_adapts` | Prepares a change to sizes already made; shown to the person before it is applied |
| `check_before_sending` | The brand's rules on every size, reported as facts |
| `send_for_approval` | Shares the sizes to the brand's review room and returns the link |
| `get_client_notes` | What reviewers said, note by note, on which size |
| `deliver_set` | Exports every size to the delivery folder, named by size, zipped |
| `update_project_facts` | Saves a project's changed RERA number, price, offer or phase, then shows which of its creatives no longer say what the facts say |
| `check_copy` | Checks Meta or Google copy against the brand's limits and legal lines |

## The brand, and what it has learned

| Tool | What it does |
|---|---|
| `get_brand_overview` | The brand: profile, rules, what the person told eonik, watched competitors |
| `search_brand_memory` | What the person told eonik before, in their words |
| `save_brand_note` | Saves a rule, preference or correction, verbatim |
| `save_dated_plan` | Saves a dated sale, launch or season |

## Research

| Tool | What it does |
|---|---|
| `list_watched_competitors` · `list_competitor_ads` · `get_competitor_activity` | What watched competitors run, and what changed |
| `list_ad_breakdowns` · `get_ad_breakdown` · `request_ad_breakdown` | Scene-by-scene breakdowns of competitor ads |
| `list_my_ads` · `get_my_ad_performance` · `get_my_tested_history` | The brand's own Meta results, as facts |
| `search_ad_library` | Public ads from any advertiser |

## Prompts

`adapts` · `where-are-we` · `phase-change` · `package`: starts that need no typing.

## Decisions

Making the sizes, choosing another way for a size, putting a piece back or taking it off, saying
what a piece of the design is, answering eonik's questions, approving: these are the person's. They reach eonik as clicks in its
panel (tools a host hides from you) or as forms your host shows. You cannot call them.
