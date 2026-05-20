# GotaGuy Landing Page - Claude Code Instructions

## What this project is
This is the gotaguy.chat multi-market landing page. It serves multiple city markets from a single Vercel deployment. There is no app, no framework, no build step. Everything is plain HTML files served statically.

## How deployment works
This project deploys directly to Vercel. Vercel watches this project folder and picks up saved changes automatically. Do not run git commands. Do not push to GitHub. Do not look for external repos. Save the file - Vercel handles the rest.

## Folder structure
All market pages live inside public/. Each market has its own subfolder:

public/
  dallas/          -> gotaguy.chat/dallas    (McKinney TX market)
  denver/          -> gotaguy.chat/denver    (Aurora CO market)
  contractors/     -> gotaguy.chat/contractors

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

## Brand and copy rules
- GotaGuy is a home repair company. Never use the words platform, marketplace, network, or system in any customer-facing copy.
- Never use em dashes or en dashes. Use hyphens, commas, colons, or periods instead.
- Contractors are described as "trusted" not "licensed."
- GotaGuy is always the subject of the sentence. Never expose the technology behind it.

## Shared assets
The GotaGuy logo file is Gotaguy_Image.jpg. It lives in public/ and is referenced by market pages as /Gotaguy_Image.jpg.

## What not to do
- Do not search the filesystem outside this project folder
- Do not run git commands
- Do not push to GitHub
- Do not rebuild pages from scratch when asked to make targeted edits
- Do not change copy, structure, or styles outside the scope of what was asked
