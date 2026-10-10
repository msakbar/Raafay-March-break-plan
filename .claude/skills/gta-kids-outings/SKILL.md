---
name: gta-kids-outings
description: Research and plan outings, events, camps and activities for Raafay (born Sept 2021) and his younger sibling (~2) around Toronto / the GTA, from home in Mimico / South Etobicoke (M8Y 3M1). Use this whenever the user asks what to do with the kids — "what's on today after 5", "plan this weekend", "long weekend ideas", "March break", "PA day", "rainy day indoor stuff", "find summer camps", "process the inbox" — or wants a new tab/scan added to the planner in this repo, even if they don't say "research" or name the repo.
---

# GTA Kids Outings

Turn a time window ("tonight after 5", "Thanksgiving weekend", "March break week") into a short, verified, ranked list of things the kids can actually do — and, when asked, persist it into the planner site (`index.html`) and notes (`activities.md`, `inbox.md`, `schedule.md`).

## Family profile (compute, don't copy)

- **Raafay**: born September 2021. Compute his age from today's date. Ages flip pricing ("4 & under free") and eligibility (camps, shows "ages 5+") — always check which side of a cutoff he is on.
- **Sibling**: about 2 years younger (~2 in mid-2026). Anything that fails a 2-year-old (no stroller access, long lines, loud, late bedtime, scare content) needs a note.
- **Home base**: Mimico / South Etobicoke, **M8Y 3M1**. Give rough drive times from there. West/central/downtown are easy; Markham, Pickering, Milton, Burlington are 35–60 min and should be flagged as a trip.
- **Family context**: Muslim family — Eid events, halal food availability and prayer-friendly timing are relevant when present; never exclude something for lack of them.
- **Friends/notes**: check `activities.md` and `schedule.md` for already-confirmed plans and recurring companions (e.g. Zain) before suggesting conflicts.

## Workflow

### 1. Pin the window
Resolve the request to concrete dates/times in America/Toronto. Note what's special about it: statutory holiday (venues often run holiday hours or close), long weekend, school break, season edges (farms/splash pads/patios opening or closing), sunset time if the ask is evening, weather if outdoor.

### 2. Read what's already known
Skim `activities.md`, the relevant `index.html` tab, `summer-camps.json`, and `inbox.md` for venues already researched. Reuse them (with re-verified hours) instead of rediscovering. Evergreen anchors (aquarium, indoor bike park, libraries, EarlyON, indoor playgrounds) are good fallbacks for any window.

### 3. Search wide, then verify narrow
Run several searches in parallel — one per angle — rather than one long query. Angles:
- Aggregator roundups for the window (see `references/sources.md`)
- Seasonal/holiday-specific events (pumpkin, Halloween, maple syrup, holiday lights, Eid, Canada Day, CNE…)
- Evergreen venues' hours for that specific date
- Free / library / city programming
- Shows for ages 2–6 (YPT, TYT, Meridian, Living Arts Centre)

Search pitfalls learned the hard way:
- **Write "Toronto" or the city name, not "GTA"** — "GTA" pulls Grand Theft Auto results.
- Several aggregators (todocanada.ca, childslife.ca) **fail on direct fetch** in this environment; rely on search snippets for them and fetch the venue's own site instead.
- Aggregators disagree on dates/hours/prices and often carry last year's data. Prefer the venue's own page; when only aggregators exist, say so and mark **Verify**.
- Confirm the event is on **this** window — a "2026" listing can still be the wrong weekend (e.g. a pumpkin trail that starts the following week).

### 4. Filter against the window and the kids
For each candidate, check:
- **Hours overlap**: does it open/stay open across the requested window? For "after 5 pm", a 6 pm close leaves one hour — put it in a "short window" bucket, not the main list. Note last-entry times (often 60–90 min before close).
- **Age fit**: suitable for Raafay's age *and* the sibling? Scare/haunt events (e.g. Wonderland Haunt, Screemers) are out.
- **Booking**: timed tickets that sell out → say "book now".
- **Distance** from M8Y.
- **Cost**, including the age-pricing trap and whether a pass beats à la carte for small kids (usually it doesn't).

### 5. Report
Lead with the fact pattern (date, holiday, assumptions), then a ranked table. Keep it blunt and scannable:

```
## Fully viable
| # | Option | Where (drive from M8Y) | Hours | Cost | Notes |
## Short window
| Option | Closes | Verdict |
## Ruled out
- Name — reason (closes 5 pm / next weekend / scare event / unconfirmed for this year)
## Plan
One concrete sequence (dinner → main activity → fallback).
```
End with a Sources list of markdown links. Mark anything not confirmed on the venue's own site as **Verify**.

### 6. Persist (only when asked, or when the user says "add it" / "make a tab")
- New dated scan → new tab in `index.html` using the card markup in `references/planner-format.md`. Put the newest tab first and make it active.
- Venue ideas worth keeping → `activities.md` entry (format in `references/planner-format.md`).
- Raw links the user dropped → process `inbox.md`, move into `activities.md`, clear processed items.
- Confirmed plans → `schedule.md`.
- Commit on the working branch with a message like `Add Thanksgiving weekend tab: 24 activities for Oct 10-12, 2026`.

## Judgment calls

- A late evening with a 2-year-old is costly; prefer things that end by ~8 pm unless asked otherwise.
- Indoor fallbacks belong on every list for weather.
- One great nearby option beats three good ones an hour away — rank on fit × proximity, not raw appeal.
- When unsure about hours, say so plainly; don't paper over aggregator conflicts.
