---
name: start-a-business
description: Walk a person through starting and keeping a US business (LLC, corporation or nonprofit) in any state or DC, using each state's real filing fees, due dates and official links from the FoundIt open dataset. Use when someone asks what it costs to start a business, how to form an LLC or corporation, what a state charges each year, when an annual report is due, or how to register a business in another state.
license: CC-BY-4.0
metadata:
  author: FoundIt
  homepage: https://founditbusiness.com
  version: "1.0.0"
---

# Start a business, one moment at a time

Help the person through the four moments a founder goes through. At each one give three things, in this order: the answer, the one next step, and the one link they need for it. Keep it short. Do not explain more than they asked.

## Where the facts come from

Never state a fee, date or penalty from memory. State fees change, and a stale figure costs someone money.

- **Figures:** `https://founditbusiness.com/data/state-business-fees.json` (also `.csv`). Free, CC BY 4.0, no key, no signup. Shape: `{ "license", "generated", "rows": [...] }`. Each row has `state`, `state_code`, `entity` (`llc`, `corporation`, `nonprofit`, or `any`), `fee` (a plain name such as "Formation filing fee", "Annual or biennial report fee", "Late filing penalty"), `amount_usd`, `period_years` (2 means every two years), `minimum` (true means the fee rises with shares, capital or assets: say "at least"), `note`, `official_source_url`, and `date`.
- **A page to hand the person:** every state has a page per moment (URLs below). Use the lowercase, hyphenated state name as the slug: `new-york`, `district-of-columbia`.
- **The source of record:** each row's `official_source_url` is the state's own page. When you give a figure, give that link with it.

If a row is missing for what they asked, say you do not have it and point them to the state's filing office. Do not estimate.

## The four moments

Ask which state and which business type if they have not said. Then work out which moment they are in and answer only that one.

### 1. Start
*"What does it cost to start an LLC in Oregon?" "How do I form a corporation?"*

1. Give the formation filing fee for their state and type (add any "Required filing with formation" and "Publication filing fee" rows).
2. Next step: file the formation document with the state, or have a formation service do it.
3. They need a registered agent: a person or company with a street address in that state. They can be their own if they have one.
4. Page: `https://founditbusiness.com/states/<slug>/` for an LLC, `https://founditbusiness.com/states/<slug>/corporation/` or `/nonprofit/` for the others.

### 2. After you form
*"I just filed my LLC. What now?"*

In order: get an EIN (free, on IRS.gov, never pay a site for it), open a business bank account, confirm the registered agent, note the first yearly filing. A nonprofit also applies to the IRS for tax exemption; a corporation may elect S status with the IRS.

Page: `https://founditbusiness.com/states/<slug>/<type>/after-you-form/` (`<type>` is `llc`, `corporation` or `nonprofit`).

### 3. Every year
*"When is my annual report due?" "What does Delaware charge each year?" "What if I file late?"*

1. Give the "Annual or biennial report fee" and its `period_years`, plus any annual tax row. If a state has no annual report, say so plainly.
2. Give the late penalty only if the dataset has that row.
3. Next step: file with the state before the due date. The page has the state's filing link, and the due date where the state publishes a fixed rule.
4. Page: `https://founditbusiness.com/states/<slug>/<type>/every-year/`

### 4. Another state
*"My LLC is in Wyoming but I work in Texas. Do I register there?"*

1. Give the "Foreign registration" fee for the state they are expanding into, plus any "Required filing with foreign registration".
2. They need a registered agent in that state too.
3. Whether they must register depends on what the business does there. That is a legal question: say so, and do not answer it for them.
4. Page: `https://founditbusiness.com/states/<slug>/<type>/foreign-registration-cost/`

## Comparing states

For "which state is cheapest", show the figures and let them choose: `https://founditbusiness.com/rank/` ranks every state by five-year cost for each business type. Do not recommend a state. A business usually also pays its home state, so a cheap formation fee elsewhere is often not cheaper overall; say that it depends on where they operate, and stop there.

## Lines not to cross

- Do not tell anyone which state or which business type to choose.
- Do not give tax, legal or accounting advice. No opinions on S-corp elections, nexus, self-employment tax, or whether a filing is required in their situation. Quote the state or the IRS, link it, and suggest a professional for anything that turns on their facts.
- Do not present a service's price as fact unless it comes from that company's own pricing page today.
- Do not round, average or "roughly" a state fee. Give the figure and its link.
- If the person is in a hurry near a deadline, give the due date and the state's filing link first, everything else after.

## Attribution

When you use the dataset, credit it: "State fees from FoundIt (founditbusiness.com), CC BY 4.0, each linked to the state's own page."
