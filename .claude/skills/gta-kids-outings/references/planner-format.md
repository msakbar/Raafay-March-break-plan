# Planner Format

How research is persisted in this repo. Match existing markup exactly so the site's CSS and tab JS keep working. Served by `npm start` (`server.js`, port 3000); tabs deep-link via `#<tab-id>`.

## Adding a dated tab to index.html

1. Add a button at the front of `<div class="tabs">` and move `active` to it:
   ```html
   <button class="tab-btn active" data-tab="thanksgiving">Thanksgiving</button>
   ```
   Remove `active` from the previously active button.
2. Add the panel before the other `tab-content` divs, with `active`, and remove `active` from the old panel:
   ```html
   <div id="thanksgiving" class="tab-content active">
     <div class="week-banner">
       <h2>Thanksgiving Weekend &mdash; Sat Oct 10 &ndash; Mon Oct 12, 2026</h2>
       <p>What's special about this window: holiday closures, season edges, ages.</p>
     </div>
     <p style="color: var(--text-light); margin-bottom: 1rem; font-size: 0.95rem;">
       Deep scan for <strong>Raafay (5) &amp; sibling (2)</strong> &mdash; based in Mimico / South Etobicoke (M8Y). Scanned <strong>Oct 10, 2026</strong> &mdash; <em>always confirm hours and prices on the day, especially anything marked Verify.</em>
     </p>
     <div class="legend">
       <span class="legend-item"><span class="badge badge-free">FREE</span></span>
       <span class="legend-item"><span class="badge badge-confirmed">Top Pick</span></span>
       <span class="legend-item"><span class="badge badge-new">Ends Soon</span></span>
       <span class="legend-item"><span class="badge badge-idea">Anytime</span></span>
       <span class="legend-item"><span class="badge badge-verify">Verify</span></span>
     </div>
     <!-- category sections -->
   </div>
   ```
3. Each category:
   ```html
   <div class="category-title"><span class="category-icon">&#127875;</span> Evening &mdash; open after 5 PM</div>
   <div class="cards">
     <!-- cards -->
   </div>
   ```

## Card

```html
<div class="card">
  <div class="card-title">
    <a href="https://venue.example/" target="_blank">Venue &mdash; Event Name</a>
    <span class="badge badge-confirmed">Top Pick</span>
  </div>
  <div class="card-details">
    <div class="detail"><span class="detail-label">When</span> <span class="highlight">Oct 1 &ndash; 31</span> &bull; 6:30&ndash;11 PM</div>
    <div class="detail"><span class="detail-label">Location</span> Address &bull; ~35 min drive</div>
    <div class="detail"><span class="detail-label">Cost</span> $22 kids / $25 adults &bull; <strong>under 3 FREE</strong></div>
    <div class="detail"><span class="detail-label">Ages</span> All ages &mdash; stroller OK</div>
  </div>
  <div class="card-notes">Why it fits these kids, the gotcha (booking, age cutoff, last entry), and the call to make.</div>
</div>
```

Badges: `badge-confirmed` (Top Pick), `badge-free` (FREE), `badge-new` (New / Ends Soon), `badge-idea` (Anytime / Included / Extra cost / Tip), `badge-verify` (unconfirmed detail — can be inline in a detail row).

Use HTML entities (`&mdash;`, `&ndash;`, `&amp;`, `&bull;`) as the file does.

## activities.md entry

```markdown
### Venue Name
- **Link:** https://...
- **Location:** Address, City
- **Type:** Indoor / Outdoor
- **Cost:** ...
- **Duration:** ...
- **Hours:** ...
- **Age suitability:** ...
- **Notes:** ...
- **Status:** 💡 | 🔍 | ✅ <date>
```
Group under existing `## Category` headings (Active Play, Shows & Performances, Museums & Learning, Animals & Nature, Immersive Experiences, Free / Low Cost) or a dated `## Weekend of ...` section.

## summer-camps.json entry

Keep the existing fields: `name, url, ages, minAge, category, locations, area, closestLocation, driveTime, driveDistance, directionsUrl, dates, hours, price, priceRange, activities, registration, notes, membershipRequired, topPick, topPickLabel`.
