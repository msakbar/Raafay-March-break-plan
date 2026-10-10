---
name: gta-kids-outings
description: Find and plan things to do with Raafay (born Sept 2021) and his younger sibling (~2) around Toronto / the GTA, from home in Mimico / South Etobicoke (M8Y 3M1). Use this whenever the user asks what to do with the kids or family — "what can we do tonight after 5", "anything on this weekend", "long weekend ideas", "March break", "PA day", "rainy day indoor stuff", "pumpkin patch / Halloween / Christmas lights for kids", "summer camps for a 5 year old" — even if they don't say "research", "kids" or "Toronto" explicitly.
---

# GTA Kids Outings

Turn a time window ("tonight after 5", "Thanksgiving weekend", "March break week") into a short, verified, ranked list of things the kids can actually do, answered directly in chat.

## Family profile (compute, don't copy)

- **Raafay**: born September 2021. Compute his age from today's date. Ages flip pricing ("4 & under free") and eligibility (camps, shows "ages 5+") — check which side of each cutoff he's on.
- **Sibling**: about 2 years younger (~2 in mid-2026). Flag anything that fails a toddler: no stroller access, long lines, loud, late finish, scare content.
- **Home base**: Mimico / South Etobicoke, **M8Y 3M1**. Give rough drive times from there. West/central/downtown are 10–25 min; Vaughan/Mississauga ~25–35; Markham, Pickering, Milton, Burlington, Hamilton 35–60+ and should be flagged as a trip.
- **Family context**: Muslim family — Eid events, halal food and prayer-friendly timing are a plus when present; never exclude something for lacking them.
- If the user mentions existing plans or friends joining, fit around them.

## Workflow

### 1. Pin the window
Resolve the request to concrete dates/times (America/Toronto). Note what's special: statutory holiday (holiday hours or closures), long weekend, school break, season edges (farms, splash pads, rinks opening/closing), sunset if the ask is evening, weather if outdoor.

### 2. Search wide, then verify narrow
Run several web searches in parallel — one per angle — rather than one long query:
- Aggregator roundups for the window (see `references/sources.md`)
- Seasonal/holiday events (pumpkin, Halloween, maple syrup, holiday lights, Eid, Canada Day, CNE…)
- Evergreen venues' hours for that exact date (`references/sources.md` has anchors by category)
- Free programming: library, EarlyON, city events
- Shows for ages 2–6

Pitfalls learned the hard way:
- **Say "Toronto" or the city name, not "GTA"** — "GTA" pulls Grand Theft Auto results.
- Some aggregators (todocanada.ca, childslife.ca) can fail on direct fetch; fall back to search snippets and fetch the venue's own site.
- Aggregators disagree on dates/hours/prices and often carry last year's data. Prefer the venue's own page; when only aggregators exist, say so and mark **Verify**.
- Confirm the event is on **this** window — a "2026" listing can still be the following weekend.

### 3. Filter against the window and the kids
- **Hours overlap**: for "after 5 pm", a 6 pm close leaves one hour → "short window" bucket, not the main list. Note last entry (often 60–90 min before close).
- **Age fit** for both kids. Haunts and scare parks are out.
- **Booking**: timed tickets that sell out → "book now".
- **Distance** from M8Y.
- **Cost**, including age-pricing cutoffs and whether a pass beats à la carte for small kids (usually not).

### 4. Report
Lead with the date, any holiday, and assumptions. Then:

```
## Fully viable
| # | Option | Where (drive from M8Y) | Hours | Cost | Notes |
## Short window
| Option | Closes | Verdict |
## Ruled out
- Name — reason (closes 5 pm / next weekend / scare event / not confirmed this year)
## Plan
One concrete sequence: dinner → main activity → fallback.
```
End with a Sources list of links. Mark anything not confirmed on the venue's own site as **Verify**. Keep it blunt and scannable; no filler.

## Judgment calls

- Late nights with a 2-year-old are costly; prefer things that end by ~8 pm unless asked otherwise.
- Always include one indoor fallback.
- Rank on fit × proximity, not raw appeal — one great option 15 min away beats three good ones an hour out.
- When hours are uncertain, say so; don't paper over source conflicts.
