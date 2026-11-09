---
name: company-intelligence-en
description: Research a named company for job-search preparation, disambiguate its identity, and report business lines, historical revenue, brands, and employee headcount and investments in a user-selected region, with dated sources and uncertainty labels.
---
# Company Intelligence for Job Search (English) V1.1

## Inputs
Required: company name. Optional: target region (country, state/province, city, or explicitly defined economic region), website, ticker, parent/subsidiary, output language. Default target region: **mainland China**, explicitly shown in the report. Users may change the region at any time; refresh regional metrics without silently changing the global revenue entity. Clarify ambiguous geographic names before regional claims.

## Mandatory workflow
1. **Entity resolution**: cross-check official website, legal name, country and headquarters, parent/subsidiary structure, and ticker. If multiple plausible companies match, show a candidate table with country, official site, and evidence, then ask the user to select. Do not mix financials from different entities.
2. **Evidence collection**: prioritize annual reports, audited statements, regulatory filings, official company pages, and government disclosures; use reputable reporting as secondary evidence. For every figure, capture source URL, publication date, covered fiscal period, entity scope, and geography. If browsing is unavailable, state that current claims cannot be verified. Never invent URLs or numbers.
3. **Business lines**: distinguish primary and secondary lines, using reported segment revenue when available. Otherwise mark the distinction qualitative; never fabricate segment percentages.
4. **Historical revenue**: show the latest five verifiable *reported* fiscal years of consolidated total revenue, with fiscal year-end, original currency, units, year-on-year growth, entity scope and sources. Do not substitute market capitalization, GMV, profit or regional sales. Note restatements, accounting changes and non-comparable periods. Expand beyond five years if requested and verified.
5. **Products and brands**: summarize major products, sub-brands and their positioning, distinguishing owned, licensed and distributed brands.
6. **Target-region presence**: separately report regional employee headcount (date, employee categories, geographic boundary) and investments (project, location, amount, currency, date and completed/planned/committed status). Never use worldwide headcount as regional headcount, registered capital as realized investment, or announced commitments as completed expenditure. Distinguish mainland China from Hong Kong, Macao and Taiwan where relevant.
7. **Uncertainty**: label each disputed or missing item as Verified / Company-reported, not independently verified / Third-party estimate / Not disclosed / Unable to verify / Conflicting sources. Say what sources and periods were checked rather than guessing.
8. **Delivery**: default to English, include research date and target region, and provide direct clickable source links. Switch to Chinese when requested.

## Output template
### Company identification
Official and common names; country and headquarters; parent/subsidiary; ticker; official website; identity status; research date; target region.

### Business lines
| Category | Business line | Revenue driver / position | Source and period |
|---|---|---|---|

### Historical consolidated revenue
| Fiscal year and end date | Total revenue | Currency / units | YoY | Scope and source |
|---|---:|---|---:|---|

### Products and brands
| Product / brand | Summary | Ownership relationship | Source |
|---|---|---|---|

### Target-region operations
- Employees: figure or explicit missing-data status; as-of date; employee and geographic scope; source.
- Investments: projects, location, amounts, currency, completion/commitment status, date and sources; mark missing information explicitly.

### Job-seeker takeaways
Briefly outline relevant divisions, regional footprint and further employer due-diligence questions. Do not invent openings, salaries or hiring claims.

### Evidence gaps and sources
List conflicts, unavailable facts, dated primary links and covered periods.

## Acceptance criteria
- Ambiguous company names never produce an arbitrary profile.
- Every revenue row has fiscal period, units, currency, entity scope and evidence.
- Regional workforce and investment figures have geographic, temporal and status boundaries.
- Missing public data is never fabricated.
