# Diagnostic Reasoning Note — Micro Filer Ltd service pages

Run per `methodology/DIAGNOSTIC-REASONING-ENGINE.md`, Stages 1 to 5.
Two pages produced, one primary macro context each.

- Page A: `public/dormant-company-accounts-tax-return.html` -> route `/dormant-company-accounts-tax-return`
- Page B: `public/micro-company-accounts-tax-return.html` -> route `/micro-company-accounts-tax-return`

Client: Micro Filer Ltd (microfiler.co.uk). Date of source capture: 6 August 2026.

---

## STAGE 1 — Entity identification

**1.1 Entity class.** Both pages sell a *performed professional service* that discharges a
*statutory obligation*. The entity is not a product and not a subscription. It is the preparation
and delivery of two prescribed documents to two separate government bodies: annual accounts to
Companies House, and a Company Tax Return to HMRC. Attribute priority therefore follows compliance
logic (who qualifies, what gets delivered, by when, at what penalty), not e-commerce logic.

**1.2 Buyer.** The buyer is a director or sole shareholder of a UK private limited company. They
consume the service directly, but the legal duty sits on the company and personally on the
directors. The buyer is not an accountant, so the page must translate statute into plain terms
while naming the statute.

**1.3 Intent verb.** Nobody buys dormant accounts. Companies **file** them, and the Companies Act
uses the verb **deliver**. The intent verb is therefore **file**, in the forms *file, files, filing,
filed*, with *deliver* and *submit* as sourced statutory synonyms. "Buy" would create a semantic
mismatch: the search intent is "file dormant company accounts", not "buy dormant company accounts".

**1.4 Conversion endpoint.** Lead form. Micro Filer converts through a "GET STARTED" contact form,
not a checkout. Pricing is nevertheless a fixed published figure, so the page sits in the quote zone
but with **visible fixed pricing**, not guided ranges. Commercial ratio target: ~65/35.

---

## STAGE 2 — Attribute extraction

**Deliverables.** Annual accounts filed at Companies House. Company Tax Return filed at HMRC.
Accountant review and director approval before filing. Explanation of tax owed.

**Process.** Three published steps: get started form, accountant emails within 24 to 48 hours, data
shared through a secure online portal in about 30 minutes; preparation over 2 to 7 days; approval,
then direct filing with HMRC and Companies House. A 7 day turnaround is available on request.

**Cost.** £285 dormant tier. £445 micro tier (income to £40,000, assets to £90,000). £695 micro or
small tier (income to £90,000, assets to £200,000). Higher income is quoted individually.

**Risk.** Companies House late filing penalties of £150, £375, £750 and £1,500 by band, doubled
across two successive late years. HMRC Company Tax Return penalties of £200, a further £200, then
10% and a further 10% of unpaid tax, rising to £1,000 for a third consecutive late return. Failure
to deliver accounts on time is a criminal offence. A dormant company that receives a notice to
deliver must still file.

**Outcomes.** The company stays on the register in good standing. The director avoids penalty
exposure. The accounts and the return reconcile to each other because one firm prepares both.

**Proof.** The trust currency in UK accountancy is *regulatory registration*, not reviews or press.
ICAEW firm number C008709968 and ICO reference A8784539 carry weight. "Business Accountant of the
Year 2023" carries weight only if the awarding body is named, which the source does not do, so it is
flagged. Star ratings and testimonials are absent from the source and are therefore absent from the
pages.

---

## STAGE 3 — Attribute filtration

Page A (dormant):

```
PRIORITY 1 (Intro)   : What gets filed and where (two bodies, two documents)
PRIORITY 2 (Intro)   : Qualification, meaning what "dormant" means in law
PRIORITY 3 (Intro)   : Fixed cost, £285
PRIORITY 4 (Mid)     : Deadlines, penalty bands, three-step process
PRIORITY 5 (FAQ)     : Confirmation statement, audit exemption, restarting trade, VAT and PAYE
EXCLUDED             : Founding year, generic "passionate team" claims, software brand name-drops
```

Page B (micro):

```
PRIORITY 1 (Intro)   : Qualification against the three micro-entity thresholds
PRIORITY 2 (Intro)   : What is filed publicly versus what HMRC receives
PRIORITY 3 (Intro)   : Fixed cost, £445, and the £695 step up
PRIORITY 4 (Mid)     : Deadlines, Corporation Tax rates, penalty bands, process
PRIORITY 5 (FAQ)     : FRS 105 content, ineligible entities, the April 2028 P&L change
EXCLUDED             : Same exclusions as Page A
```

The critical filtration call: **qualification outranks price on both pages.** A director who does not
know whether their company is dormant or micro cannot act on a price. Cost is Priority 3, still
inside the intro, but it follows the qualification test.

---

## STAGE 4 — Language calibration

**Trust currency.** ICAEW firm number, ICO registration, chartered status, UK basing. Not reviews,
not press mentions, not awards without a named body.

**Insider terms.** Accounting reference date. Significant accounting transaction. Notice to deliver
a Company Tax Return. FRS 105. iXBRL. Nil return. Confirmation statement. Marginal relief. Audit
exemption under section 480. Balance sheet total. These are the terms a director meets in Companies
House and HMRC correspondence, so the page uses them and then defines them.

**Action-outcome verbs, split by thematic predicate as instructed.**

| Content type | Predicates used |
|---|---|
| Benefit | improve, support, protect, keep, discharge |
| Risk | reduce, expose, fail, miss, trigger |
| Cost | cost, vary, depend, estimate, compare, cover |

**Natural comparisons in this niche.** Dormant for Companies House versus dormant for Corporation
Tax. Micro-entity versus small company. Accounts versus Company Tax Return. Filing deadline versus
payment deadline. Nil return versus no return.

**Cheap versus premium.** "Cheap" here means a filing-only service with no named accountant and no
tax advice. "Premium" means a chartered firm, a named accountant with a direct line, and included
ongoing support on VAT, PAYE and Income Tax. Micro Filer's published position is the second.

---

## STAGE 5 — Structural assembly

**H1 Page A:** Dormant company accounts and company tax return
**H1 Page B:** Micro company accounts and company tax return

Both H1s were changed at the operator's instruction on 6 August 2026, from the earlier
intent-verb-plus-price form. The H1 now carries the bare entity plus attribute pair. The intent verb
"file" no longer appears in the H1; it still carries through the body at 2.08% and 1.84% density.
The `<title>` tags retain the intent verb and the price for search-result click-through.

**Tab systems.** Page A tabs divide by the two dormancy tests plus the two entry routes (never
traded, stopped trading). Page B tabs divide by qualification criterion and by filing destination.
Both use a second tab system for the FAQ.

**Cards.** The same three-tier fee card set appears on both pages, with the centerpiece rotated: the
£285 card is the centerpiece on Page A, the £445 card on Page B. The rotation keeps each page's
macro context intact.

**Centerpiece annotation.** Fee card badge, plus the penalty figures rendered as prominent numerals
in the risk section. In compliance services the number that drives the decision is the penalty, not
the discount, so the penalty band is the second centerpiece.

**FAQ tabs.** Page A: Filing, Dormant status, Cost, Deadlines and penalties, Corporation Tax, Other
services. Page B: Filing, Micro-entity status, Cost, Deadlines and penalties, Corporation Tax,
FRS 105 and 2028.

**Pricing placement.** Intro plus a dedicated fee card section, per the fixed-fee lead-form model.

**Commercialisation rhythm.** COMMERCIAL, TRUST, COMMERCIAL, RISK, PROCESS, CTA, BENEFIT, FAQ, FORM.

---

## Writing constraints applied (from the operator brief)

1. One primary macro context per page, restated as the subject of every section heading.
2. The entity plus attribute pair is preserved as the semantic anchor in every section.
3. Effort split: roughly 78% on entity relationships, semantic role clarity and retrievable facts;
   roughly 22% on readability and transitions.
4. Every section runs Start, Expand, Close.
5. Every paragraph is a 2 to 4 sentence semantic packet, one idea each.
6. Every sentence is a traceable SVO or entity-attribute-value triple.
7. Thematic predicate alignment as tabulated in Stage 4.
8. Every plural or collective noun is followed by a concrete example.
9. Active voice, third-party voice ("Micro Filer files"), plain language.
10. Missing facts carry a `[DATA NEEDED: ...]` marker at the claim location.
11. No em dash characters anywhere in either page.
12. No internal pipeline labels anywhere in either page.
