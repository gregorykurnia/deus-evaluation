# R1: Phase 1 review (Steps 1–6b)

Date: 2026-10-28. Scope: `outputs/01` to `outputs/06b` and their sections in the readable doc, checked against
CLAUDE.md rules 1–7. Sources used for the check: `inputs/DEUS_Company_History_Recap.pdf`, the three decks in
`inputs/`, `inputs/deus-fact-sheet.md`, https://deushcs.com and https://deck.deushcs.com (fetched 2026-10-28).

**Result: Phase 1 passes after six small fixes.** No report invents a number; every Rp figure traces to the fact
sheet or is labelled as derived from it. The problems found were five phrases in quotation marks that no source
contains, two NO DATA items missing from their report's Data gaps list, and one doc section whose key findings
did not follow its report. All were fixed in this commit.

## How each rule was checked

| Rule | Check | Result |
|---|---|---|
| 1 Sources cited, ASSUMPTION labels | Every quoted phrase (about 400) searched in the recap, decks and fact sheet; misses checked one by one, website quotes fetched live; web links in the doc compared with each report's source list | 5 quotes not in any source (fixed, below). All doc links appear in a report's sources. |
| 2 No invented numbers; NO DATA goes to Data gaps | Every Rp figure in the reports and the doc compared with the fact sheet; every NO DATA compared with the report's Data gaps list | All figures trace to the fact sheet or are labelled "derived". 2 reports had a NO DATA missing from Data gaps (fixed). |
| 3 Sunk cost | Searched for spend or years used as a reason | The one mention (Step 4, Agate's Rp1 billion) explicitly rejects it as a reason. Pass. |
| 4 Direct | Read the leads and key findings | Founder and dad patterns named plainly in 01, 03, 06a. Pass. |
| 5 Facts / interpretation / recommendation | Looked for labelled interpretation and recommendation in each report | Every report labels its interpretation (3–12 times each). Pass. |
| 6 Saved with step number | File names | Pass. |
| 7 Closing sections | Headings; count of key findings | All seven end with Key findings (exactly 5), Data gaps, Questions for the founder. Pass. |
| Doc matches report | Each doc section's lead and key findings compared with its report; doc figures and links checked | Steps 2–6b match. Step 1's key findings differed (fixed, below). Every section has its exhibit, data gaps, questions and report link. |

## Fixes made

| # | Where | Problem | Fix |
|---|---|---|---|
| 1 | 01, sales-seat archetype | "we cannot sell" shown as a quote; not in the recap | Replaced with the recap's own sentence: "Apart from Telkom, we struggled very hard to sell anything" (Recap, Phase 7) |
| 2 | 01, same section | "similar gaps" shown as a quote; not in the recap | Reworded without quotes and labelled as interpretation from Recap, Reference: people |
| 3 | 03, anti-profile table | "friends of the family who might find it interesting" shown as a quote; not in the recap | Replaced with the recap's words: leads were "mostly retail companies and his friends" (Recap, Phase 5) |
| 4 | 03 (section 4) and 04 (section 5) | "one HR platform" quoted as if DEUS's pitch; the site never says it | Replaced with the site's actual line, "One partner to hire, develop and pay" (deushcs.com) |
| 5 | 06a, shared values | "solutions with data and deep understanding" quoted as English; the deck is in Indonesian | Quoted the Indonesian original and marked the English as a translation |
| 6 | 02 and 06b, Data gaps | NO DATA used for CAC and LTV (02) and for segment budgets and buyers' view of the positioning (06b) without a Data gaps line | Added both lines |
| 7 | Doc, Step 1 key findings | The list differed from the report's five findings (it dropped findings 1, 3 and 5), and "no lost buyer is recorded blaming the product" read as if loss reasons were recorded; they are NO DATA | Rewrote the doc list to follow the report's five findings; says plainly that no loss reason has been recorded |

## Checked and left as they are

- Quoted labels in diagrams, framework terms ("shifting the burden"), DEUS's own proposed taglines in 06b and
  hypothetical buyer lines in the questions are not presented as source quotes. Left as they are.
- 06b's two Telkom quotes are translations from the GBA deck's Success Story slide (Indonesian original found)
  and are marked "translated". Correct.
- Step 3 labels its profile lines "Backed" or "Assumption" (the ICP method's column) and uses ASSUMPTION in
  capitals in the text. That meets rule 1.
- Step 1 counts "seven people" in sales or account roles and "four" hired to fix sales. Both are right (line 84
  vs line 123 of the report); the doc now gives both.
- The doc's Data gaps lists are shorter than the reports'. That is by design (the doc is the readable version),
  and each one links to its full report.

## Key findings

1. **No invented numbers in Phase 1.** Every Rp figure in seven reports and the doc traces to the fact sheet or
   is labelled as derived from it.
2. **Five quotes were paraphrases in quotation marks** (01, 03, 04, 06a). Each now uses the source's own words or
   drops the quotation marks. Later steps that reuse these phrases should use the corrected wording.
3. **Two NO DATA items had no Data gaps line** (02, 06b). Both are added; Step 6c's interview guide covers the
   06b one.
4. **The doc matched its reports except for Step 1's key findings**, now rewritten to follow the report.
5. **No step's conclusion changes.** Every fix is to wording or sourcing; Phase 2 can build on 01–06b as they stand.

## Data gaps

No new gaps. The open gaps are the ones in the step reports and the fact sheet's "Most important gaps"; the
first three are still cash in bank, total invested, and Agate's terms for the new games (Fact sheet).

## Questions for the founder

- The website quotes in the reports were checked on 2026-10-28. If the site copy changes, should the reports
  quote the version from the day of the analysis (current practice) or the latest one?
- Are there any written customer messages (emails, WhatsApp, survey answers) not yet in `inputs/`? Phase 1 found
  that the only customer quotes are the Telkom slide in the GBA deck.
