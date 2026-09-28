# Budget Buys UK

Live at: https://richardgolding28-gif.github.io/budget-buys-uk/

An affiliate content site: budget buying guides for UK shoppers (camping/outdoor gear plus Halloween, Christmas, birthdays, and other seasonal shopping), monetized through Amazon Associates UK. Hosted free on GitHub Pages, content is kept flowing by six scheduled cloud routines — no server, no ongoing manual work required.

## Status

- Amazon Associates UK: approved, tag `trailandtarp-21` (set in `_config.yml`, every affiliate link on the site reads this one value)
- GitHub Pages: live, auto-rebuilds on every push to `main`
- Google Search Console: verified (`google_site_verification` in `_config.yml`)

## Automation (all configured as claude.ai routines — manage at claude.ai/code/routines)

| Routine | Schedule | Purpose |
|---|---|---|
| `camp-gear-guide-weekly-post` | Daily, 9am UTC | Writes one new post from `CONTENT_QUEUE.md`'s queue |
| `camp-gear-guide-trending-topics` | Weekly, Mon | Adds genuinely trending UK product topics to the top of the queue |
| `camp-gear-guide-monthly-gift-topics` | Monthly | Adds one birthday-gift and one novelty-gift topic, permanently |
| `camp-gear-guide-christmas-gift-push` | Weekly (Sep–Dec 2026 only) | Ramps gift topics up as Christmas approaches, then auto-stops |
| `camp-gear-guide-novelty-gifts-november` | One-time, 14 Nov 2026 | Secret Santa / novelty gift topic batch |
| `camp-gear-guide-monthly-audit` | Monthly | Site health check, replaces discontinued products in old posts, occasional expansion topics |

`CONTENT_QUEUE.md` is the shared queue all of these read from and write to — it's the coordination point between them.

## What still needs occasional human attention

- Confirming Amazon Associates payouts arrive (paid ~60 days after the month a sale happens, direct to UK bank account once payment details are set up).
- If a product a post links to becomes unavailable, the monthly audit job should catch and replace it — but a periodic skim is sensible.
- Realistic expectations: slow-burn SEO income. Expect little to nothing for the first few months while Google indexes and ranks the content, then a small amount if it ranks — not a replacement income on its own.
