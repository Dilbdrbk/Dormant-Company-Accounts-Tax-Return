# Source Verification — Micro Filer Ltd service pages

Covers both deliverables:

- `public/dormant-company-accounts-tax-return.html` (Page A) -> route `/dormant-company-accounts-tax-return`
- `public/micro-company-accounts-tax-return.html` (Page B) -> route `/micro-company-accounts-tax-return`

**Rule applied:** every fact, figure, price, threshold, deadline, penalty, credential and statutory
reference on either page traces to a source below. Nothing on either page is estimated, inferred or
invented. Gaps carry an on-page `[DATA NEEDED: ...]` marker and are listed in section 9.

Source capture date: **6 August 2026**.

---

## 0. Editorial policy applied on 6 August 2026 (operator instruction)

Three changes were made to how sourced facts are *presented*. None of them changes what is sourced,
and every claim below still traces to the same source.

**0.1 On-page attribution removed.** Earlier drafts wrote "GOV.UK states that ..." and "Micro Filer's
FAQs state that ..." inline. The pages now assert the fact directly and clarify it within its own
section. GOV.UK is no longer named anywhere in either page, including the schema. **This table is now
the only record of where each fact came from, so it carries more weight than before, not less.** Two
supports remain on-page: the footer links to legislation.gov.uk and the relevant guidance pages, and
statutory references are still cited by section number in the body copy (section 1169, section 480,
section 384, section 384B, section 386, section 453, section 476, section 481).

**0.2 One service price per page.** Each page now shows only its own fee. Page A shows £285 and no
other Micro Filer price. Page B shows £445 and no other Micro Filer price. The £695 tier and the
opposite page's fee were removed from body copy, fee cards, FAQs, footer service lists, and the
`Offer` nodes in the schema. Where the old copy compared tiers, it now points to a quote instead.
Section 3 below still verifies all three published fees, because the source publishes all three and a
reviewer may need to reinstate one. Statutory figures (penalty bands, size thresholds, Corporation
Tax rates) are unaffected by this rule.

**0.3 Voice.** Copy now mixes first person plural ("we file", "our fixed fee") with the third-party
form ("Micro Filer Ltd is a chartered accountants firm registered with the ICAEW"). The third-party
form is retained wherever the sentence states a registration, a legal identity, or a credential, so
those claims still read as statements of record.

**0.4 FAQ schema regenerated.** The `FAQPage` answers are now extracted programmatically from the
visible accordion text, so the structured data and the rendered page cannot drift apart. Nine
question and answer pairs per page. Verified byte-identical at build time.

---

## 1. Source index

| ID | Source | URL | Type |
|---|---|---|---|
| S1 | Micro Filer homepage | https://www.microfiler.co.uk/ | Client site (operator-provided) |
| S2 | Micro Filer FAQs page | https://www.microfiler.co.uk/our-services | Client site |
| S3 | Micro Filer blog, "How to File a CT600: Documents, Deadlines and Penalties", 3 August 2026 | https://www.microfiler.co.uk/blog | Client site |
| S4 | Micro Filer blog, "How to File Micro-Entity Accounts in the UK: Complete 2026 Guide", 22 July 2026 | https://www.microfiler.co.uk/blog | Client site |
| S5 | GOV.UK, Dormant companies: dormant for Corporation Tax | https://www.gov.uk/dormant-company/dormant-for-corporation-tax | Primary (HMRC) |
| S6 | GOV.UK, Dormant companies: dormant for Companies House | https://www.gov.uk/dormant-company/dormant-for-companies-house | Primary (Companies House) |
| S7 | GOV.UK, Prepare annual accounts: micro-entities, small and dormant companies | https://www.gov.uk/annual-accounts/microentities-small-and-dormant-companies | Primary (Companies House) |
| S8 | GOV.UK, Late filing penalties | https://www.gov.uk/government/publications/late-filing-penalties/late-filing-penalties | Primary (Companies House) |
| S9 | GOV.UK, Company Tax Returns: penalties for late filing | https://www.gov.uk/company-tax-returns/penalties-for-late-filing | Primary (HMRC) |
| S10 | Companies Act 2006, section 1169 | https://www.legislation.gov.uk/ukpga/2006/46/section/1169 | Primary (statute) |
| S11 | Companies Act 2006, section 480 | https://www.legislation.gov.uk/ukpga/2006/46/section/480 | Primary (statute) |
| S12 | Micro Filer brand stylesheet and logo asset | `e1ee2429_home_withFlex_1.min.css`; `lirp.cdn-website.com/e1ee2429/dms3rep/multi/opt/logo-1920w.png` | Client site assets |

---

## 2. Brand, identity and contact (both pages: header, trust bar, form, footer, schema)

| Claim on page | Source | Verbatim source text / value |
|---|---|---|
| Legal name "Micro Filer Ltd" | S1 | "Micro Filer Ltd is a limited company registered in England and Wales" |
| Companies House number 12273247 | S1 | "registered number 12273247" |
| ICAEW firm number C008709968 | S1 | "Registered with the ICAEW under firm number C008709968." |
| ICO reference A8784539 | S1 | "Registered with the ICO under reference number A8784539." |
| "Chartered accountants" / "a Chartered Accountants firm based in the UK" | S1 | "we are a Chartered Accountants firm based in the UK"; "Chartered accountants" |
| Address: International House, 64 Nile Street, London N1 7SR | S1 | "International House / 64 Nile Street / London / N1 7SR" |
| Email info@microfiler.co.uk | S1 | "info@microfiler.co.uk" |
| "We are UK based!" rendered as "UK based team" | S1 | "We are UK based!" |
| "No commitment", "No hidden charges" | S1 | "No commitment"; "No hidden charges" |
| "Ongoing support (VAT, PAYE, Income Tax, advice)" | S1 | "Ongoing support (VAT, PAYE, Income Tax, advice)" |
| "Business Accountant of the Year 2023" | S1 | "BUSINESS ACCOUNTANT OF THE YEAR 2023" — **awarding body not stated in source; flagged on page** |
| Logo image URL | S12 | `https://lirp.cdn-website.com/e1ee2429/dms3rep/multi/opt/logo-1920w.png` |
| Brand colours #21cbdc, #6dadbd, #395860, #16394e, #71b8ca | S12 | Extracted from the live page stylesheet (`#21cbdc` is the most-used brand colour, 12 occurrences) |
| Fonts Montserrat (headings) and Roboto (body) | S12 | `font-family:Roboto` (12 occurrences), `font-family:Montserrat` (5 occurrences) on the live site |
| Nav and footer links (Home, Blog, FAQs, Contact us) | S1 | `/`, `/blog`, `/our-services`, `/#Contactus` |
| Form fields: name (full name and title), email, telephone, company name, comment | S1 | Exact field labels from the homepage contact form |
| "PLEASE CHECK YOUR JUNK MAIL if you don't receive an email" (paraphrased on page) | S1 | "One of our accountants will send you an email in the next few working hours... PLEASE CHECK YOUR JUNK MAIL if you don't receive an email." |

**No testimonials, star ratings, review counts or customer numbers appear on either page.** The source
contains none, so no proof section was invented. This is a deliberate omission, not an oversight.

---

## 3. Pricing (both pages: hero, fee cards, FAQ, schema Offer)

| Claim on page | Source | Verbatim source text |
|---|---|---|
| £285 covers dormant accounts and company tax return | S1 | "£285 / - dormant accounts / - company tax return" |
| £285 scope: dormant companies or minimal trading, max 10 low value transactions | S1 | "for dormant companies or companies with minimal trading (maximum of 10 low value transactions)" |
| £445 covers micro company accounts and company tax return | S1 | "£445 / - micro company accounts / - company tax return" |
| £445 scope: total income up to £40,000, total assets up to £90,000 | S1 | "for companies with total income up to £40,000 and total assets up to £90,000" |
| £695 covers micro or small company accounts and company tax return | S1 | "£695 / - micro or small company accounts / - company tax return" |
| £695 scope: total income up to £90,000, total assets up to £200,000 | S1 | "for companies with total income up to £90,000 and total assets up to £200,000" |
| Higher income is quoted individually | S1 | "if your income is higher, please get in contact for a quote" |

**Unverified:** VAT treatment of all three fees. Not stated anywhere in the source. Flagged on both
pages.

---

## 4. Process and turnaround (both pages: hero, trust bar, process section, form)

| Claim on page | Source | Verbatim source text |
|---|---|---|
| "GET STARTED" form provides basic details | S1 | "'GET STARTED' will provide us with some basic details." |
| Designated accountant emails usually within 24 to 48 hours | S1 | "Your designated accountant will email you to request the information they need usually within 24 to 48 hours." |
| Data shared through a secure online portal, about 30 minutes | S1 | "You can then share your data via our secure online portal. This should only take about 30 minutes of your time." |
| Micro Filer calculates tax and prepares accounts | S1 | "we will get to work calculating your tax and preparing your accounts!" |
| Accountant's direct line for queries | S1 | "You'll have your accountant's direct line should you have any queries." |
| Preparation normally takes 2 to 7 days | S1 | "This will normally take between 2-7 days unless you have requested a speedy turnaround." |
| 7 day turnaround available upon request | S1 | "7 day turnaround available upon request" |
| Accounts and return sent for approval, tax explained, then filed directly with HMRC and Companies House | S1 | "We send the accounts and tax return to you for your approval! We explain what tax is owed and answer any questions you have, then we file directly with HMRC and Companies House. All done with minimal fuss!" |
| Software integration is optional | S1 | "We integrate with the following software (and more) / if you don't use any software this is also fine!" |

**Unverified:** the names of the integrated software packages. The homepage shows them as logo images
with no alt text, so no names could be read. Flagged on both pages.

---

## 5. Page A only — dormancy law and dormant filing

| Claim on page | Source | Verbatim source text |
|---|---|---|
| A company is dormant during any period in which it has no significant accounting transaction | S10 | "For the purposes of the Companies Acts a company is 'dormant' during any period in which it has no significant accounting transaction." |
| A significant accounting transaction is one that section 386 requires to be entered in the accounting records | S10 | "A 'significant accounting transaction' means a transaction that is required by section 386 to be entered in the company's accounting records." |
| Disregarded items: memorandum subscriber shares; registrar fees for change of name; for re-registration; for registration of a confirmation statement; section 453 penalties | S10 | Section 1169 exception list, quoted in full at the source |
| GOV.UK plain-terms list: filing fees paid to Companies House, penalties for late filing of accounts, money paid for shares when the company was incorporated | S6 | "Filing fees paid to Companies House / Penalties for late filing of accounts / Money paid for shares when the company was incorporated" |
| Companies House calls a company dormant if it had no significant transactions in the financial year | S6 | "Your company is called dormant by Companies House if it's had no 'significant' transactions in the financial year." |
| A dormant company must still send a confirmation statement and annual accounts | S6 | "Confirmation statement (previously annual return) / Annual accounts" |
| Dormant companies that qualify as small do not need to be audited | S7 | "Dormant companies that qualify as 'small' do not need to be audited." |
| Section 480 exempts a company dormant since formation, or dormant since the end of the previous financial year subject to conditions | S11 | s.480(1)(a) and (1)(b), quoted in full at the source |
| The s.480(2) conditions: entitled to prepare accounts under the small companies regime (ss.381 to 384), or would be but for being a public company or member of an ineligible group; and not required to prepare group accounts | S11 | s.480(2)(a)(i), (a)(ii) and (b) |
| Section 480 has effect subject to s.475(2)-(3), s.476 and s.481 | S11 | "This section has effect subject to — section 475(2) and (3)...; section 476 (right of members to require audit), and section 481 (companies excluded from dormant companies exemption)." |
| Dormant for Corporation Tax: stopped trading and no other income, for example investments | S5 | "has stopped trading and has no other income, for example investments" |
| Also dormant for CT: new company not yet trading; unincorporated association or club owing less than £100 CT; flat management company | S5 | Listed at source |
| Trading includes buying, selling, renting property, advertising, employing someone or getting interest | S5 | "Trading includes buying, selling, renting property, advertising, employing someone or getting interest." |
| A company that has filed a Company Tax Return or received a notice to deliver one must still file online | S5 | "You'll still need to file a Company Tax Return online - this will show HMRC that your company is dormant for this period." |
| A director can tell HMRC the company is dormant for Corporation Tax | S5 | "tell HMRC that it's dormant for Corporation Tax" |
| Dormant for Corporation Tax and dormant for Companies House are two different tests; a company can meet one and not the other | S3 | "Dormant for Corporation Tax and dormant for Companies House are two different tests. A company can meet one and not the other, so check both separately rather than assuming." |
| A dormant nil return is a normal CT600 with every figure at zero; no separate nil-return form exists | S3 | "That return is a normal CT600 with every figure at zero, known as a nil return. There's no separate nil-return form." |
| If HMRC has confirmed dormancy and issued no notice, no filing is needed; the confirmation is the trigger | S3 | "If HMRC has confirmed your company is dormant and hasn't issued a notice, you don't need to file. That confirmation is the trigger, not your own assumption that nothing happened." |

**Deliberately omitted:** form AA02. The form is not named in any operator-provided source, and the
GOV.UK pages checked do not reference it. The page says "dormant accounts" instead, which S7 does
support ("you may be able to file dormant accounts instead").

---

## 6. Page B only — micro-entity law and micro filing

| Claim on page | Source | Verbatim source text |
|---|---|---|
| Micro-entity if any 2 of: turnover £1,000,000 or less; £500,000 or less on the balance sheet; 10 employees or less | S2, S7 | S2: "a turnover of £1,000,000 or less / £500,000 or less on its balance sheet / 10 employees or less". S7: same three figures. |
| Micro-entities prepare simpler accounts meeting statutory minimum requirements and send only the balance sheet with less information to Companies House | S2, S7 | "prepare simpler accounts that meet statutory minimum requirements and send only your balance sheet with less information to Companies House" |
| Homepage three-question test (turnover under £1,000,000; balance sheet less than £500,000; fewer than 10 employees; "Yes" to 2 or more) | S1 | "1 - Turnover under £1,000,000? / 2 - Balance sheet less than £500,000? / 3 - Less than 10 employees? / 'Yes' to 2 or more - please get in touch!" |
| Thresholds increased for periods starting on or after 6 April 2025 from £632,000 turnover and £316,000 balance sheet | S4 | "For periods starting on or after 6 April 2025, the government increased thresholds from the previous £632,000 turnover and £316,000 balance sheet limits." |
| Small company: any 2 of turnover £15 million or less; £7.5 million or less on the balance sheet; 50 employees or less; audit exemptions and abridged accounts available | S7 | Listed at source |
| First year qualifies if conditions met that year; subsequent years require the conditions in that year and the year before | S2 | "a company qualifies as a micro-entity in its first financial year if it fulfils the conditions in that year. In any subsequent years a company must fulfil the conditions in that year and the year before." |
| A company that stops meeting the criteria may continue the exemptions the next year; reverting continues the exemption uninterrupted | S2 | "it may continue to claim the exemptions available in the next year... the exemption will continue uninterrupted." |
| Two consecutive years framing | S4 | "meets at least 2 of these 3 criteria for two consecutive years" |
| Excluded entities: limited/qualifying partnership, PLC, overseas company, unregistered company, s.1040 company, charitable company, s.384 exclusion, s.384B exclusion | S2 | Full list quoted at source |
| Also excluded: investment company, financial institution (insurance, banking), part of an ineligible group | S4 | "A public company / A charity / An investment company / A financial institution (insurance, banking, etc.) / Part of an ineligible group" |
| Under FRS 105, Companies House accounts contain only a cover page, a simplified balance sheet signed by a director, and four mandatory footnotes | S4 | "Cover page with company name and registration number / Simplified balance sheet (signed by a director) / Four mandatory footnotes" |
| The four footnotes: number of employees; called-up share capital not paid; off-balance sheet arrangements (if any); statement that accounts are prepared under the micro-entities regime | S4 | Listed at source |
| Balance sheet must carry a prominent statement above the director's signature and printed name that the accounts follow the micro-entity provisions, in the original and the Companies House copy | S2 | Quoted at source |
| Companies House sees the balance sheet only; HMRC receives full financial information via the CT600 | S4 | "While Companies House only sees your balance sheet, HMRC receives full financial information through your CT600 Company Tax Return" |
| HMRC accepts iXBRL accounts with just the balance sheet because the CT600 supplies the profit and income figures | S4 | Quoted at source |
| Micro-entity accounts submit to HMRC automatically with the CT600; the same iXBRL balance sheet attaches; no separate upload needed | S4 | "The same iXBRL balance sheet is attached to your CT600 / No separate upload to HMRC is needed" |
| A CT600 filing is three documents: the CT600 form, iXBRL statutory accounts, and an iXBRL Corporation Tax computation | S3 | "A CT600 filing is three documents submitted together: the CT600 form, iXBRL accounts, and an iXBRL tax computation." |
| Filing only to HMRC without Companies House is a common mistake; both require accounts | S4 | "Filing only to HMRC without Companies House—both require accounts" |
| Reasons to consider an alternative standard (creditor detail, FRS 102 group consolidation, voluntary P&L disclosure, exceeding thresholds next year) | S4 | Listed at source under "When Micro-Entity Accounts Aren't Right" |
| From April 2028, micro-entities must file P&L accounts with Companies House, with an opt-out from publishing on the public register; small companies cannot file abridged accounts | S4 | Listed at source under "Important Changes Coming in 2028" |
| Corporation Tax is payable annually based on profit; profit includes a deduction for salaries paid but excludes dividends paid | S2 | "Corporation Tax is payable annually and based on the profit that your company makes. Your profit will include a deduction for salaries paid but exclude dividends paid." |
| Rates: 19% on profits up to £50,000, 25% above £250,000, marginal relief between | S3 | "Current Corporation Tax rates are 19% on profits up to £50,000 and 25% above £250,000, with marginal relief tapering the rate for profits in between." |
| Computation method: start from accounting profit, add back disallowable costs such as depreciation and entertainment, deduct capital allowances, apply losses | S3 | Quoted at source (Step 2) |
| Worked example: £68,000 profit, £4,000 depreciation added back, £6,000 capital allowances, £66,000 taxable profit, marginal relief to an effective rate in the low 20s | S3 | Quoted verbatim at source |
| A company must file even at a loss or with no Corporation Tax to pay | S2 | "Your company must file a Company Tax Return even if you make a loss or have no Corporation Tax to pay." |
| Losses carry forward only if HMRC has a record of them | S3 | "Reported losses can be carried forward against future profits, but only if HMRC has a record of them." |
| Salaries and dividends are subject to Income Tax; salary paid net of Income Tax via PAYE unless criteria are met not to register, then via Self Assessment | S2 | Quoted verbatim at source |
| Amendment window: within 12 months of the filing deadline; overpayment relief may apply afterwards | S3 | Quoted at source |
| At six months late HMRC issues a tax determination that cannot be appealed | S3 | "If you're six months late, HMRC issues a 'tax determination,' its own estimate of what you owe, and you can't appeal it." |
| Worked date: period ending 31 January 2025 must be filed with Companies House by 31 October 2025 | S4 | "If your accounting period ends 31 January 2025, you must file with Companies House by 31 October 2025." |

---

## 7. Deadlines and penalties (both pages)

| Claim on page | Source | Verbatim source text |
|---|---|---|
| Accounts normally due 9 months from the accounting reference date for a private company | S2 | "the time normally allowed for delivering accounts to Companies House is 9 months from the accounting reference date for a private company" |
| First accounts covering more than 12 months: 21 months from incorporation or 3 months from the accounting reference date, whichever is longer | S2 | Quoted verbatim at source |
| Failure to deliver accounts on time is a criminal offence, and the law imposes a late filing penalty on the company | S2 | "Failure to deliver accounts on time is a criminal offence. In addition, the law imposes a penalty for late filing of accounts on the company." |
| Companies House penalties: £150 / £375 / £750 / £1,500 by band | S8 | "Not more than 1 month → £150; More than 1 month but not more than 3 months → £375; More than 3 months but not more than 6 months → £750; More than 6 months → £1,500" |
| Penalty doubled if accounts are filed late in 2 successive financial years beginning on or after 6 April 2008 | S8 | "The late filing penalty will be doubled if accounts are filed late in 2 successive financial years (beginning on or after 6 April 2008)." |
| Company Tax Return due 12 months after the end of the accounting period | S2 | "The deadline for your tax return is 12 months after the end of the accounting period it covers." |
| Corporation Tax payable 9 months and one day after the end of the accounting period | S2 | "It's usually 9 months and one day after the end of the accounting period." |
| HMRC penalties: £200 at 1 day; a further £200 at 3 months; 10% of unpaid tax at 6 months; a further 10% at 12 months | S9 | "1 day → £200; 3 months → Another £200; 6 months → 10% of unpaid tax; 12 months → Another 10% of unpaid tax" |
| Three consecutive late returns raise the £200 penalties to £1,000 each | S9 | "If your tax return is late 3 times in a row, the £200 penalties are increased to £1000 each." |
| HMRC closed its free Company Accounts and Tax Online service on 31 March 2026; from 1 April 2026 commercial software or an accountant is required | S3 | Quoted verbatim at source |

**Cross-check performed:** the client's own blog (S3) states HMRC late-filing penalties of £200 /
£200 / 10% / 10% and £1,000 for three consecutive late returns. These were independently confirmed
against GOV.UK (S9) and match exactly. No client figure was carried onto the page without a primary
check where a primary source exists.

---

## 8. Conflict found in the client's own material (needs client sign-off)

Page B does not assert either side of this conflict. Both source statements are reported on the page
in the terms their own source uses, and the point is escalated here rather than resolved by guessing.

| Source | Statement |
|---|---|
| S2 (FAQs) | "A micro-entity is required to **prepare** accounts that contain the following elements: ... A directors' report ... An auditors report, **unless the company is claiming exemption from audit as a small company**". S2 then adds: "Micro-entities do not have to **deliver** a copy of the directors' report or the profit and loss account to Companies House." |
| S4 (blog) | "You are exempt from **filing**: Profit and loss account (not publicly disclosed) / Director's report / Auditor's report (**micro-entity accounts are audit-exempt**)" |

The prepare-versus-deliver distinction reconciles most of the difference. It does not reconcile the
audit point: S2 makes audit exemption conditional on claiming the small company exemption, while S4
states flatly that micro-entity accounts are audit-exempt. **A partner at Micro Filer should confirm
which statement they stand behind before either page goes live.** Page B currently carries neither
formulation in its body copy, so no incorrect claim is published in the meantime.

---

## 9. NEEDS SOURCE — every unverifiable claim, flagged on-page and left blank

| # | Location | What is missing | Page |
|---|---|---|---|
| 1 | Hero price block | Whether the £285 fee is inclusive or exclusive of VAT | A |
| 2 | Hero price block | Whether the £445 fee is inclusive or exclusive of VAT | B |
| 3 | Trust bar | The awarding body and category behind "Business Accountant of the Year 2023" | A, B |
| 4 | "What Micro Filer files" table | Whether the £285 fee includes filing the confirmation statement, or whether that is charged separately | A |
| 5 | Minimal trading tab | The monetary ceiling that makes a transaction "low value" at the £285 tier | A |
| 6 | Process section | The names of the accounting software packages Micro Filer integrates with (homepage shows logos only, no alt text) | A, B |
| 7 | Cost FAQ | VAT treatment of the fee, and whether Companies House or HMRC disbursements are charged separately | A, B |
| 8 | Filing FAQ | Confirmation of whether the confirmation statement filing sits inside the fee | A |

Each item above appears on the relevant page as a visible `[DATA NEEDED: ...]` marker at the exact
claim location. **All markers must be resolved or removed before publication.**

---

## 10. Items deliberately excluded rather than invented

| Element a template would add | Why it is absent |
|---|---|
| Testimonials and customer quotes | No reviews exist in any operator-provided source. Fabricating them is prohibited. |
| Star rating and `aggregateRating` schema | No rating data exists in the source, so the schema property was omitted rather than populated. |
| "Trusted by X companies" / client counts | No figure exists in the source. |
| Named founders / team members | The client site names no individuals, so no `founder` property appears in the Organization schema. |
| Client logos or case studies | None published by the client. |
| Telephone number | The client site publishes an email address and a contact form only. No number was invented; the form field for telephone comes from the client's own form. |
| Form AA02 | Not named in any source checked. Omitted in favour of the sourced term "dormant accounts". |
| Turnaround guarantee wording | The source says a 7 day turnaround is "available upon request", so no guarantee is claimed. |

---

## 11. Sign-off

- [ ] Micro Filer confirms VAT treatment of all three fees
- [ ] Micro Filer confirms the "Business Accountant of the Year 2023" awarding body
- [ ] Micro Filer confirms confirmation-statement scope at the £285 tier
- [ ] Micro Filer defines "low value transaction" for the 10-transaction rule
- [ ] Micro Filer resolves the audit-exemption wording conflict in section 8
- [ ] Micro Filer supplies the integrated software package names
- [ ] Senior reviewer confirms every `[DATA NEEDED]` marker is resolved or the claim removed
- [ ] Final URLs confirmed before the internal cross-links and canonical tags go live
