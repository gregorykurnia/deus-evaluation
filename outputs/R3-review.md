# R3: Phase 3 review (Steps 9 and 10, and the readable doc)

Date: 2026-10-28. Scope: `outputs/09-executive-summary.md`, `outputs/10-DEUS-strategic-analysis.md`, and the doc's
Executive summary and "Data gaps and open questions" sections, checked for two things the plan asks: (1) no claim
that is missing from the step reports (01–08) or the input files, and (2) every source reference kept. Sources used
for the check: `outputs/01-…` to `outputs/08-verdict.md`, `inputs/deus-fact-sheet.md`, and the text of the four
PDFs in `inputs/`. Doc sections for Steps 0–8 were checked in R1 and R2 and are not re-reviewed here.

**Result: no invented claim, but Step 10 had dropped about 100 source references. Fixed.** Every number, date and
quote in 09 and 10 traces to a step report or an input file. Step 10 condensed many step-report rows and
paragraphs and, in doing so, cut the primary citation (recap phase, fact sheet, deck, web source, Step 3 ledger
id) while keeping only a section-level "from Step N". Those references are now restored. Three smaller fixes
are listed below.

## How it was checked

| Check | Method | Result |
|---|---|---|
| Numbers, dates, quotes (09, 10) | Every Rp amount, %, USD figure, ISO date, counted noun ("10 meetings", "19 people") and quoted phrase searched in 01–08, the fact sheet and the PDFs' text | All found. The only strings not found verbatim were the labels of 10's decision diagram (section 10.7), a new drawing of 08's decision table; one label overstated 08 (fix 2) |
| Claims in 09 | Each Fact and Interpretation line traced to its cited step | All traced, e.g. "seven people held sales or account seats" (Step 1, section on Loop 2), "15 of the 19 hired have left" (Step 6a, section 1), "Rp900 juta against Rp440 juta" (Step 7, MC3), "judgement and senior access, not lead volume" (Step 6a, key finding 3). Pass |
| Claims in 10, section 2 (the only part written from the recap directly) | 40 quotes and names (e.g. "genuinely cool", Skyfy, Komdigi, Matahari, "not extended", 600 employees) searched in the recap text; who joined and left in each phase checked against the recap's people table | All found; joins and exits match. Pass |
| Claims in 10, sections 3–11 | Each line matched to its closest step-report line; wording differences read | Condensed, no new claims. Overruled points follow the later step and say so (e.g. Step 2's price comparison withdrawn per Step 7) |
| Web sources kept (10) | Every URL in 01–08 compared with 10 | 29 of 29 present in 10's Sources. Pass |
| Source references kept (10) | For each line of 10, the citations of its matching step-report line compared with its own | About 120 lines had lost one or more primary references; after removing false matches (a source citation that backed a clause 10 does not carry), about 100 restored (fix 1) |
| Doc: Executive summary and Data gaps sections | Read in full and compared with 09 and 10 | No new claims. Test A's Rp10 juta minimum lacked its source; the Data gaps table had no sources (fix 3) |
| Closing sections | Headings and counts in 09 and 10 | Both end with Key findings (5), Data gaps, Questions for the founder. Pass |

## Fixes made

| # | Where | Problem | Fix |
|---|---|---|---|
| 1 | 10, sections 3–10 (about 100 lines: Loop write-ups, Step 2 hypothesis and ledger tables, Step 3 ledger-based cards and anti-profile, BCG and STP tables, PMF scorecard, 7S notes, Step 7 claim table and risks, interview plan, verdict scorecard, assets and options) | Primary references dropped in condensing, e.g. Step 2's D5 row lost "(Recap, Phases 5, 9, 11)", the anti-profile lost Step 3's L01–L08 and W01–W06 ids, the S5 row lost "(Recap, Phase 2; Fact sheet)", Step 7's first vulnerability lost "(Step 4, W3, W4)" | Each restored next to the claim it supports, in 10's own label style (Step 3 ledger ids bare in section 5, "Step 4, W3" for web sources elsewhere) |
| 2 | 10, section 10.7 decision diagram, "B only" box | "Discover to Agate, handed back or shut": Step 8 says offer Agate the Telkom relationship or DEUS as delivery partner, or hand the suite back; shutting it is not in 08 for that branch | "Discover offered to Agate or handed back" |
| 3 | 09 and 10 test table; doc Executive summary, test A | "minimum Rp10 juta" had no source (Step 8 cites Pitch deck, A9) | "(minimum Rp10 juta; Pitch deck, A9)" in all three |
| 4 | Doc, "Data gaps and open questions" table | No source for any row | Source line under the table: fact sheet; Step 8; Step 5, M5; Step 6c; Step 7, E3, E4 |
| 5 | 10, section 11, Telkom data gap | The search result about Telkom's 2025 openings had no source | "Step 7, W1" added |

## Not changed, with reasons

- 10's front matter says it adds no claim beyond the step reports except the recap timeline; that holds.
- Section summaries in 10 that rank or score (e.g. the STP scores row for S1) keep "Step 6b" as their source
  rather than repeating every input behind a score; the full rows with sources are in the step report.
- The decision diagram in 10 is a new exhibit, not a new claim: every other box matches Step 8's decision table.

## Key findings

1. **09 and 10 add no claims.** Every number, date and quote traces to a step report or input file; the recap
   timeline in 10 matches the recap phase by phase.
2. **10 had dropped about 100 primary source references** when condensing step reports; all are restored.
3. **One diagram label overstated Step 8** (Discover "shut" in the Enhance-only branch); corrected.
4. **The doc's Executive summary and Data gaps sections match 09 and 10**; two missing source references added.
5. **Phase 3 passes after these fixes.**

## Data gaps

- None new. Unchanged: the Data gaps in `outputs/10-DEUS-strategic-analysis.md`, section 11.

## Questions for the founder

- None new from this review. The open questions are in 10, section 11, and the doc's last section.
