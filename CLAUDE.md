# Project: DEUS strategic analysis

The steps are in `PLAYBOOK.md`; the task list `autorun` works through is `IMPLEMENTATION_PLAN.md`.

## Company context
DEUS (Human Capital and Business Solutions) is an Indonesian HR-tech company with three products:
- DEUS Discover: game-based assessment suite (personality, cognitive, neuroscience, simulation). Games built by Agate International.
- DEUS Enhance: performance management system, originally built around Delamibrands' (DKB) KPI and appraisal needs. Rebuilt by Ko Will.
- Potentia: gamified cognitive assessment for kids, acquired. Has its own website for tokens and purchases.
Current team: 5 people (founder, Ko Will, Thania, Audrey, Bu Sovie).
The full history is in inputs/DEUS_Company_History_Recap.pdf (11 phases).

## Rules for every analysis
1. Ground every claim in a source: cite the recap phase (e.g. "Recap, Phase 8") or the file name. Anything not in the files is labelled ASSUMPTION.
2. Never invent numbers. If a number is needed and missing, write "NO DATA" and add it to the "Data gaps" list at the end of the report.
3. Sunk cost is not evidence. Years spent or money spent is never a reason to continue something.
4. Be direct. Name uncomfortable patterns plainly, including ones involving the founder or the founder's family network. Be kind in tone, not vague in content.
5. Separate what happened (facts) from why it happened (interpretation) from what to do (recommendation).
6. Save each step's report to outputs/ with the step number in the file name (e.g. outputs/01-systems-thinking.md). Read earlier outputs before starting a new step.
7. End every report with: Key findings (max 5), Data gaps, Questions for the founder.
8. Write in English.
9. The readers are the founder and the founder's dad. This is internal, not for clients or investors.

## Branch
Work on the `analysis` branch: commit and push there (`git push origin analysis`) after every step.
Never push to `main`; the owner merges `analysis` into `main` after reading the results.

## Readable doc
Every step also goes into one shared doc that the owner and their dad read:
https://claude.ai/artifact/X6WnBHvCVDrT45GrKF1P97 (doc id `f3b73b06-1d7a-4b39-8b39-a909685c70ce`,
body node `e21b17b4-7db7`). Each step has a pending block waiting for it, in this reading order:

| Step | Pending block id |
|---|---|
| 9 Executive summary | `mhwn3j2n8n2.30` |
| 8 The verdict | `mhwn3j2n8n2.31` |
| 1 Systems thinking | `mhwn3j2n8n2.32` |
| 2 Lean Startup | `mhwn3j2n8n2.33` |
| 3 Ideal customer profile | `mhwn3j2n8n2.34` |
| 4 BCG matrix | `mhwn3j2n8n2.35` |
| 5 Product-market fit | `mhwn3j2n8n2.36` |
| 6a McKinsey 7S | `mhwn3j2n8n2.37` |
| 6b STP | `mhwn3j2n8n2.38` |
| 6c Interview guide | `mhwn3j2n8n2.39` |
| 7 Sense-check | `mhwn3j2n8n2.40` |
| 0 Fact sheet | `mhwn3j2n8n2.41` |

After the report is saved, fill the step's section:
- Load the docs guide first (`guide` with `topic.index`; also `topic.diagram` or `topic.charts` when the
  section has a picture), then `replace` the step's own pending block with `## <Step title>` and the body.
- The section is the readable version, not a copy of the report: first sentence = the answer, then the key
  findings, the step's main exhibit drawn (causal loops, the BCG 2x2, the funnel, the scorecard), data gaps,
  questions for the founder, and a link to the full report:
  `https://github.com/gregorykurnia/deus-evaluation/blob/analysis/outputs/<file>`. Every rule above applies.
- A step that is rerun (after interviews) replaces its existing section instead (heading and body ids from a
  `read` of the doc's outline).
- If a doc call is refused, fix it and resend once. If it still fails, finish and commit the report anyway, and
  put `DOC: not updated (<reason>)` in the final message. The doc never blocks a step.
