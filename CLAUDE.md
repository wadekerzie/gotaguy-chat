# GotaGuy Landing Page - Claude Code Instructions

## What this project is
This is the gotaguy.chat multi-market landing page. It serves multiple city markets from a single Vercel deployment. There is no app, no framework, no build step. Everything is plain HTML files served statically.

## How deployment works
This project deploys directly to Vercel. Deploy by committing and pushing to the main branch on GitHub. Vercel is connected to the wadekerzie/gotaguy-chat repo and auto-deploys on push. Do not use vercel --prod from this directory.

## Folder structure
All market pages live inside public/. Each market has its own subfolder:

public/
  dallas/          -> gotaguy.chat/dallas    (McKinney TX market)
  denver/          -> gotaguy.chat/denver    (Aurora CO market)
  contractors.html -> gotaguy.chat/contractors  (market-neutral contractor page)

Each market folder contains:
  index.html             main landing page
  how-it-works.html      contractor-facing info page
  contractor-terms.html  contractor terms of service
  terms.html             homeowner terms
  privacy.html           privacy policy

## Market reference
When editing any page, use only the correct values for that market. Never mix market details across files.

| Market   | Folder  | City/Region              | Phone          | SMS link                                           | Domain              |
|----------|---------|--------------------------|----------------|----------------------------------------------------|---------------------|
| McKinney | dallas  | McKinney & Collin County | (469) 273-6216 | sms:+14692736216&body=Hi, I need something fixed!  | gotaguymckinney.com |
| Aurora   | denver  | Aurora & Denver Metro    | (720) 821-3271 | sms:+17208213271&body=Hi, I need something fixed!  | gotaguyaurora.com   |

## The most important rule about multi-market edits
If you make a structural or content change to one market's landing page, you must make the equivalent change to all other market landing pages. Only the market-specific values listed above should differ. Everything else - layout, section order, copy structure, styles - must stay in sync across all markets.

When adding a new market, copy the dallas/ folder as the template, rename it, and update all market-specific values throughout.

## Product facts (locked)
- Fee structure: 20% per completed job. No minimum. $300 maximum cap.
- Payment flow: when the homeowner confirms the job is complete, GotaGuy sends a payment link. Once the homeowner pays, the contractor receives their 80% on their debit card the same day. No invoices, no chasing.

## Key messaging (locked)
- Primary homeowner promise: "Get a quote in 90 seconds." On the hub a homeowner enters their ZIP; on a market page they text the market number.
- Primary contractor promise: "Show up to jobs where the homeowner already has a quote." The homeowner agrees to a quote range before the contractor is involved, and the contractor sets the final price on site.

## Pages and sync state
Six pages make up the site, and they are currently all in sync:
- public/index.html - the hub at gotaguy.chat/. ZIP router: in-area ZIPs redirect to /dallas or /denver, out-of-area shows a waitlist. Leads with "Get a quote in 90 seconds."
- public/dallas/index.html and public/denver/index.html - homeowner market landing pages. Identical to each other except market-specific values.
- public/contractors.html - market-neutral contractor page. Two-card CTA: Wade for McKinney (214) 668-7986, Aaron for Aurora (720) 749-9474.
- public/dallas/how-it-works.html and public/denver/how-it-works.html - market contractor pages. Identical to each other except the market CTA contact (Wade vs Aaron, same numbers as above).

Note: homeowner-facing market numbers (the SMS links in the Market reference table) are different from the contractor recruiting numbers above. Do not mix them.

## Brand and copy rules
- GotaGuy is a home repair company. Never expose the technology behind it. GotaGuy is always the subject of the sentence.
- Banned words: never use platform, marketplace, network, system, app, bot, AI, vetted, or tradesperson in any customer-facing copy. Use "local pros" instead of "tradespeople" and "trusted" instead of "vetted" or "licensed."
- Never use em dashes or en dashes, literal or as &mdash; / &ndash; entities. Use hyphens, commas, colons, or periods instead.

## Shared assets
The GotaGuy logo file is Gotaguy_Image.jpg. It lives in public/ and is referenced by market pages as /Gotaguy_Image.jpg.

## What not to do
- Do not search the filesystem outside this project folder
- Do not rebuild pages from scratch when asked to make targeted edits
- Do not change copy, structure, or styles outside the scope of what was asked
- Do not use vercel --prod from this directory (deploy via git push to main, see deployment section)
