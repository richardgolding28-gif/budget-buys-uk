# Trail & Tarp

An affiliate content site: budget/beginner camping gear buying guides, monetized through Amazon Associates. Built to run itself after a short one-time setup.

## One-time setup (only you can do these — tied to your identity)

1. **Create a GitHub repo.** Go to github.com/new, name it (e.g. `camp-gear-guide`), keep it public, don't initialize with a README (this folder already has one). Then from this folder:
   ```
   git remote add origin https://github.com/YOUR-USERNAME/camp-gear-guide.git
   git branch -M main
   git push -u origin main
   ```
2. **Turn on GitHub Pages.** In the repo: Settings → Pages → Source: "Deploy from a branch" → Branch: `main` / `/(root)`. Your site goes live at `https://YOUR-USERNAME.github.io/camp-gear-guide/` within a few minutes.
3. **Apply to Amazon Associates UK** at https://associates.amazon.co.uk (not the US .com program — as a UK resident with a UK bank account, the UK programme is the one that actually pays out cleanly). You'll need your live site URL from step 2 and a handful of published posts (already done — there are 4). Approval usually takes a few days; Amazon reviews the site for genuine content, which this has.
4. **Once approved**, put your Associate tag into `_config.yml`:
   ```yaml
   amazon_tag: "yourrealtag-21"
   ```
   Commit and push that one-line change. Every affiliate link on every post — past and future — updates automatically, because they all read this one value. Links point to amazon.co.uk.

That's it. Nothing else here needs your identity or a payment method tied to you personally beyond the Associates signup itself.

## What runs on its own after that

A scheduled task adds a new buying guide from `CONTENT_QUEUE.md` on a recurring basis, following the same structure as the existing posts (real, current products looked up at write time — never invented), commits it, and pushes. GitHub Pages rebuilds the live site automatically on every push. No app to keep running, no server to maintain — GitHub hosts it for free indefinitely.

## What still needs occasional human attention

- Confirming Amazon Associates payouts arrive (they pay ~60 days after the month a sale happens, direct deposit or gift card).
- Amazon Associates requires at least 3 qualifying sales within 180 days of signup or the account is closed (you re-apply if that happens — no penalty beyond re-applying).
- If a product a post links to becomes unavailable, the search-based links still work (they link to an Amazon search for the product name, not a fixed product page), so this rarely needs a fix — but a periodic skim is sensible.
- Realistic expectations: this is slow-burn SEO income. Expect $0 for the first few months while Google indexes and ranks the content, then a small amount if it ranks — not a replacement income on its own.
