# Audit status

Tracks when each published post's product links were last verified as real, current, and still sold — and logs the monthly site health check. The monthly audit job works through posts oldest-checked-first (a post that's never been checked counts as the oldest), auditing a batch each run so the whole site gets cycled through over time rather than trying to check everything at once.

## Posts

- _posts/2026-09-27-best-budget-tents-under-150.md — last audited: 2026-10-01
- _posts/2026-09-27-best-budget-backpacking-sleeping-bags.md — last audited: 2026-10-01
- _posts/2026-09-27-best-led-headlamps-for-camping.md — last audited: 2026-10-01
- _posts/2026-09-27-best-budget-coolers-for-camping.md — last audited: 2026-10-01
- _posts/2026-09-28-best-budget-camp-stoves-under-50.md — last audited: 2026-10-01
- _posts/2026-09-28-best-halloween-costumes-for-kids.md — last audited: 2026-10-01
- _posts/2026-09-28-best-adult-halloween-costumes-under-30.md — last audited: 2026-10-01
- _posts/2026-09-28-best-pumpkin-carving-kits-and-tools.md — last audited: 2026-10-01
- _posts/2026-09-28-best-outdoor-christmas-lights.md — last audited: 2026-10-01
- _posts/2026-09-28-best-advent-calendars-for-kids-and-adults.md — last audited: 2026-10-01
- _posts/2026-09-28-best-artificial-christmas-trees-under-100.md — last audited: 2026-10-01
- _posts/2026-09-28-best-stocking-fillers-under-10.md — last audited: 2026-10-01
- _posts/2026-09-28-best-electric-blankets.md — last audited: 2026-10-01
- _posts/2026-09-28-best-hot-water-bottles.md — last audited: 2026-10-01
- _posts/2026-09-28-best-thermal-base-layers-for-winter.md — last audited: 2026-10-01
- _posts/2026-09-29-best-halloween-garden-and-window-decorations.md — last audited: 2026-10-01
- _posts/2026-09-30-best-halloween-sweets-and-treats-for-trick-or-treaters.md — last audited: 2026-10-01

## New posts

Whenever the daily posting job creates a new post, it should add a line for it here too (last audited: never), so the monthly audit picks it up eventually. If a post exists in `_posts/` but isn't listed here, treat it as never audited.

## Site health log

(most recent entry first — the monthly audit job appends here)

- 2026-10-01: indexing check -- Google site: search returned 0 results for site:richardgolding28-gif.github.io/budget-buys-uk. Bing site: search not separately obtainable (WebSearch tool has no Bing-specific engine option, so no clean isolated read). Buyer-query test: not found for any tested query ('best budget camping tents under £150 UK', 'best pumpkin carving kits UK', 'best stocking fillers under £10 UK') -- site did not appear in results for any of them.
- 2026-10-01: site health check unavailable (richardgolding28-gif.github.io is blocked by this environment's network egress policy, both via curl and WebFetch — see note below); amazon_tag and CONTENT_QUEUE.md structure both OK; daily job last posted 0 days ago (2026-10-01 post seen mid-run); audited 17 posts, replaced 6 discontinued/unverifiable products across 5 posts (GSD Colorado 8ft tree -> HOMCOM Snow-Flocked 8ft tree, JOYIN 50in hanging combo -> JOYIN skeleton/reaper hanging set, BON BAG sweets pouch -> MyCandyShop jelly sweets, Pumpkin Masters Masters Collection kit -> OWUDE Professional kit, Pumpkin Masters Party kit -> Nabance kit, Regatta Premium base layer -> Regatta Professional base layer); added 4 expansion topics to queue (air fryers, wireless earbuds, dehumidifiers, winter slippers). Network block on the live-site check should be resolved by widening this environment's egress allowlist to include github.io.
