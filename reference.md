# eonik: the tools

The live list comes from the person's eonik connection (`tools/list`); this map is rendered from it by `python -m ops.mcp_skill`, never written by hand.

## Setting eonik up

| Tool | What it does |
|---|---|
| `get_setup` | Show where this person's eonik stands and the one next step: their account, an invitation waiting for them, their brand, then the rest of setting up (competitors to watch, their ad account, eonik on their Mac), each naming the tool to use or the page where the person does it. |
| `use_brand` | Work on one of the person's brands in this conversation: every tool after this works on that brand, with no new sign-in. |
| `create_brand` | Set up a new brand in eonik from its website: eonik reads what the brand sells, who it is for, its voice and its products from the site, and saves the brand. |
| `add_competitors` | Add the competitors the person named to the brand's watch list, so eonik watches their ads for this brand. |
| `invite_teammates` | Invite people to work in eonik with the person: each address gets eonik's invitation email and joins their workspace, with every brand in it, when they accept. |

## Connecting the brand's ad account

| Tool | What it does |
|---|---|
| `connect_source` | Connect the brand's ad account so eonik reads the brand's own ads and what each one bought. |

## The work (in the person's eonik app, signed in to this connection's account)

| Tool | What it does |
|---|---|
| `get_work` | Show where the person's work for this brand stands: what needs their decision, what is being made, what was delivered, which of their computers has eonik open, and what reviewers said in eonik's review room (each shared creative, whether it is waiting, approved or sent back, and each open note with who wrote it and its size; pass a creative's creative_file to change_creative to change exactly that one). |
| `find_creatives` | Find creatives by name or project: the person's own design files and eonik projects on their computer, and every creative saved to this brand in eonik, whoever made it, with each one's size, project, where it is and the sizes already made from it. |
| `get_creative` | Look at one creative as it stands: every size of it with the words on each and what each line is for, whether its end block says the project's current facts, its recent saved states, and one picture of the whole set. |
| `make_ad` | Make a new ad in eonik, from what the person wants said, or by recreating an existing ad (from_ad) with the brand's product, person or place in it, keeping its film, shots and timing. |
| `make_versions` | Make versions of one creative that differ in one thing: the person shown, the setting, the language of its words, or one line's words, such as a price or an offer. |
| `onboard_brand` | Bring a brand's handover files into eonik: a folder on the person's computer or a zip they attached, with content sheets, brand guidelines, typefaces, logos and project facts. |
| `find_brand_pictures` | Find the brand's own pictures by what they are called or show: its photos, logos and lockups, people, places and products, with one picture of them to look at. |
| `change_creative` | Change one creative in the person's eonik. |
| `make_adapts` | Make adapts, which are new sizes of a creative for a media plan, in the person's eonik app, with the brand's fonts, rules and layout kept the same way on every size. |
| `check_before_sending` | Check work before it goes out, in the person's eonik app. |
| `send_for_approval` | Share the adapts of the named creatives to the brand's review room, where the client can comment on each size and approve or ask for changes, and return the review link. |
| `answer_client_note` | Answer one reviewer's note in eonik's review room, where they will read it: a reply under their note in the person's name, and the note marked done once the change is made. |
| `deliver_set` | Export every adapt of the named creatives into the person's delivery folder, one file per size named by its size, and zip them for the client or the media team. |
| `update_project_facts` | Save a change to one product's facts (a price, an offer, a registration number, an address: each a label and the exact words a creative prints) as a new dated version. |
| `check_copy` | Check ad copy against the brand's rules before it is used: each line's length against the limit the brand's brief or content sheet sets, another project's legal line appearing by mistake, figures no project fact supports, and legal lines the creative must carry. |

## The brand and research

| Tool | What it does |
|---|---|
| `get_brand` | Read who this brand is: name, category, audience, positioning, the rules it keeps, what the team has told eonik to do and not do (in their own words), the competitors it watches and what changed among them recently. |
| `save_brand_note` | Save something the team wants eonik to remember about the brand, such as a rule, preference, decision or correction, exactly as they said it, and return the saved wording. |
| `save_dated_plan` | Save an upcoming dated event for the brand, such as a sale, launch or seasonal moment, with its dates. |
| `get_competitor_ads` | Show what the brand's watched competitors are doing, in three parts: `watched` (each competitor eonik watches, with its id and how many of its ads were captured on each channel), `changes` (what changed in the last days: new ads, stopped ads, ads past 30 days running, landing-page changes, discount emails and standout organic posts, each dated) and `ads` (their ads, newest first, with channel, the date the platform says each started, days live and copy). |
| `get_ad_breakdown` | Read the scene-by-scene breakdown of one competitor ad: transcript, scenes with timing, each shot's role and framing, and the hook, or its status when none exists yet. |
| `request_ad_breakdown` | Start a scene-by-scene breakdown of one competitor ad that does not have one yet; it is ready a few minutes later through get_ad_breakdown. |
| `get_my_ads` | Read the brand's own Meta ads. |
| `search_ad_library` | Search eonik's library of public ads from any advertiser, including brands this workspace does not watch, by advertiser, industry, opening style or creative style. |

## The team

| Tool | What it does |
|---|---|
| `get_activity` | Show what assistants did for this brand in eonik over a recent window: each request with when it was made, who made it, from which assistant, what was asked, how it ended and whether its result was checked. |

## Prompts

`adapts` · `where-are-we` · `facts-change` · `package` · `client-notes` · `check-package` · `versions` · `onboard` · `change` · `reel`: starts that need no typing.

## Guides

- `eonik://guide/set-up`: Setting eonik up
- `eonik://guide/where-are-we`: Where things stand
- `eonik://guide/adapts`: Adapts for a media plan
- `eonik://guide/change`: An exact change to a creative
- `eonik://guide/reel`: A static made into a reel
- `eonik://guide/versions`: Versions of one creative
- `eonik://guide/ads`: A new ad
- `eonik://guide/recreate`: An ad recreated with the brand's own
- `eonik://guide/client-notes`: The client's notes
- `eonik://guide/package`: Check, approve and deliver
- `eonik://guide/check-package`: A finished package checked
- `eonik://guide/facts-change`: A product's facts changed
- `eonik://guide/copy`: Ad copy
- `eonik://guide/onboard`: A brand's handover files
- `eonik://guide/brand-and-research`: The brand and what competitors run
- `eonik://guide/activity`: What assistants did

## Decisions

Making the sizes, keeping a change, approving, answering eonik's questions: these are the person's. They reach eonik as clicks in its panel (`answer_change`, `open_in_eonik`, `read_job`, `send_choice`, which a host shows only to the panel) or as forms your host shows. You cannot make them.
