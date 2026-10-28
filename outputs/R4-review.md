# R4: Phase 4 review (revised Steps 1–6c)

Date: 2026-10-28. Scope: the revised `outputs/01` to `outputs/06c` and their sections in the readable doc, checked
against CLAUDE.md rules 1–7 and the five corrections in `inputs/deus-fact-sheet.md` ("Corrections to the recap and
earlier steps"). Sources used for the check: `inputs/deus-fact-sheet.md` and the R1 method (`outputs/R1-review.md`).

**Result: Phase 4 passes after nine small fixes.** No revised report still says DEUS bought the Phase 11 games, every
report gives BCG's churn reason as the fact sheet does, and all eight closing sections are in place. The problems
were wording: seven places in the reports and two in the doc said "Telkom bought" or "Telkom paid" where the buyer was
Telkom's Assessment Center, and one derived figure did not show its working. All were fixed in this commit.

## How each check was done

| Check | How | Result |
|---|---|---|
| Correction 1: games not bought | Searched all eight reports for bought, acquired, purchase near games, Agate or Next Chapter; same search in the doc | Every hit is either a "first pass said / now" correction table or says "not bought". Pass. |
| Correction 2: Telkom's Assessment Center | Searched for "Telkom bought/paid/chose/praised/stopped" and counted "Assessment Center" per report (4 to 30 mentions each) | 7 report lines and 2 doc lines named Telkom as the buyer (fixed, below). "Telkom stopped" lines kept: the fact sheet itself says Telkom's MT intake strategy changed (Correction 3). |
| Correction 3: why Telkom stopped | Read every "stopped" and "renewal" line | All say the MT intake strategy changed and Telkom could not refer. Pass. |
| Correction 4: BCG's churn reason | Read every BCG line with churn, left or lost (about 50) | All give bugs, delivery and communication under Wulan, and that BCG won't come back; none still gives "data problems" as the reason or calls it NO DATA outside a correction table. Pass. |
| Correction 5: dad funds, founder decides | Searched for the dad as decider and for funding wording | No report says the dad decides; funding is the dad's support with no written limit. Pass. |
| Rule 1 and 2: sources, NO DATA | Every Rp figure in 01–06c compared with the fact sheet; the ones not in it checked by hand | All trace to the fact sheet, a cited web source (Step 4, W10, W10b) or are labelled derived. One derived figure lacked its working (fixed, below). |
| Rule 3: sunk cost | Read the Agate Rp1 billion mentions | Still rejected as a reason (Step 4). Pass. |
| Rule 7: closing sections | Headings and key-finding counts | All eight end with Key findings (5), Data gaps, Questions for the founder. Pass. |
| Doc matches report | Doc outline: every Step 1–6c section has its lead, exhibit, Key findings, Data gaps, Questions and a link to the right report on the `analysis` branch | Pass, after the doc fixes below. |

## Fixes made

| # | Where | Problem | Fix |
|---|---|---|---|
| 1 | 01, Loop 5 discussion | "Telkom bought the single-personality-game version" | "Telkom's Assessment Center bought …" |
| 2 | 02, D2 row | "the one Telkom bought" | "the one Telkom's Assessment Center bought" |
| 3 | 02, D6 row | "Telkom bought the single personality game" | "Telkom's Assessment Center bought …" |
| 4 | 03, section on buyers' words | "none says why Telkom bought" | "… why Telkom's Assessment Center bought" |
| 5 | 04, unit table | "this is what Telkom bought" | "… what Telkom's Assessment Center bought" |
| 6 | 04, price test row | "Telkom paid above list price" | "Telkom's Assessment Center paid …" |
| 7 | 06b, offer and price | "Anchor on what Telkom paid" | "… what Telkom's Assessment Center paid" |
| 8 | 02, DKB service-contract test | "about Rp21–23 juta a month" left after one person, working not shown | Added "(derived: Rp35 juta − Rp4 juta server − Rp8–10 juta)" |
| 9 | Doc, Step 4 key finding 2 and Step 0 key finding | "Telkom bought DEUS's own personality game"; "Telkom paid Rp380,000 per candidate" | Both now say Telkom's Assessment Center |

## Checked and left as they are

- "Telkom praised" (05): the praise on the GBA deck is signed "Telkom Group Selection", so naming the unit more
  precisely would go beyond the source.
- "Telkom stopped" lines (01, 02, 05, 06b): Telkom's MT strategy changed, which is how the fact sheet puts it.

## Left for Phase 5 (sections that 5.1–5.6 replace)

The doc sections for Steps 7, 8, 11 and the "Data gaps and open questions" section still carry first-pass wording.
They are not in this review's scope and their tasks replace them, so they were not edited here. R5 should confirm these
are gone:
- Step 7: "Agate sells the same games directly" and "Telkom bought one game"; "Don't cite 'Telkom paid above list'".
- Step 8 Data gaps and Step 11 Data gaps: "Why Telkom bought and stopped".
- Step 11, reason "Built or bought more when sales were weak" and "whether the new games were the wrong buy".
- Data gaps section: "why Telkom stopped buying" (now answered: Correction 3).

## Key findings

1. The founder's five corrections are applied in all eight revised reports; no report still says DEUS bought the
   Phase 11 games.
2. The one recurring slip was naming Telkom, not its Assessment Center, as the buyer: nine places, all fixed.
3. BCG's churn reason is the same everywhere: bugs, delivery and communication under Wulan; BCG won't come back.
4. Every Rp figure traces to the fact sheet, a cited source, or a labelled derivation.
5. Stale first-pass wording remains only in the doc sections Phase 5 will replace (Steps 7, 8, 11 and Data gaps).

## Data gaps

- No new gaps. This review added no numbers; the gaps in each report's own list stand (fact sheet, "Most important
  gaps").

## Questions for the founder

- None new from this review. Each report's open questions stand; the interviews in Step 6c are still the next source
  of buyers' own words.
