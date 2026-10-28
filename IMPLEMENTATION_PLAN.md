# DEUS strategic analysis: autorun plan

Runs Steps 1–10 of `PLAYBOOK.md`, one fresh session per line, on the model picked in `PLAYBOOK.md` §5.
Start it from this folder on the `analysis` branch: `autorun check`, then `autorun all`.
Every task follows `CLAUDE.md`: its rules, the `analysis` branch, and the readable doc
(https://claude.ai/artifact/X6WnBHvCVDrT45GrKF1P97). A step is done when its report is in `outputs/` and ends
with Key findings, Data gaps and Questions for the founder; its doc section is filled; and its line is ticked in
the same commit, pushed to `analysis`.

Defaults (so no task stops to ask): Steps 6a, 6b and 6c always run. The first pass has no interviews, and
Steps 7–10 say so. Step 8's "what changed since the last review" is: first review, nothing beyond the fact sheet
and the reports. Step 9's audience is the founder's dad and the founder (internal).

## Before the run
- [x] *owner*: repo stays public (owner's choice, 2026-10-28); was: make the GitHub repo private (`gh repo edit gregorykurnia/deus-evaluation --visibility private --accept-visibility-change-consequences`): the run pushes company financials and team notes
- [x] *owner*: upload the input files into `inputs/` and commit them on `analysis`: the recap PDF at least, plus any deck that isn't on the public sites listed in `CLAUDE.md`
- [x] *owner*: Step 0 by hand: a Haiku 5.5 Max session in this folder, "Read PLAYBOOK.md and CLAUDE.md, then run Step 0"; answer its number questions; it saves `inputs/deus-fact-sheet.md`, fills the doc's Step 0 section and commits

## Phase 1: Analysis
- [x] 1.1 Step 1 Systems Thinking (PLAYBOOK.md "Step 1"): outputs/01-systems-thinking.md and the doc's Step 1 section · Opus 5.5 High: framework analysis of root causes that every later step reads
- [x] 1.2 Step 2 Lean Startup (PLAYBOOK.md "Step 2"): outputs/02-lean-startup.md and the doc's Step 2 section · Opus 5.5 High: judges each product's hypotheses and designs experiments
- [x] 1.3 Step 3 ICP Profile (PLAYBOOK.md "Step 3"): outputs/03-icp-profile.md and the doc's Step 3 section · Opus 5.5 High: Backed vs Assumption needs factual accuracy
- [ ] 1.4 Step 4 BCG Matrix (PLAYBOOK.md "Step 4"): outputs/04-bcg-matrix.md and the doc's Step 4 section · Opus 5.5 High: Indonesian market research with citations plus a portfolio call
- [ ] 1.5 Step 5 setup with the new-venture skill (PLAYBOOK.md "Step 5", first prompt): the ventures/deus/ workspace, no doc section · Haiku 5.5 Max: fills VENTURE.md from existing outputs
- [ ] 1.6 Step 5 PMF with the pmf skill (PLAYBOOK.md "Step 5", second prompt): its venture file, a copy at outputs/05-pmf.md, and the doc's Step 5 section · Opus 5.5 High: diagnosis from the funnel numbers
- [ ] 1.7 Step 6a McKinsey 7S (PLAYBOOK.md "Step 6"): outputs/06a-mckinsey-7s.md and the doc's Step 6a section · Opus 5.5 High: organisation diagnosis
- [ ] 1.8 Step 6b STP (PLAYBOOK.md "Step 6"): outputs/06b-stp.md and the doc's Step 6b section · Opus 5.5 High: chooses the beachhead segment
- [ ] R1 Phase 1 review: check outputs 01–06b and their doc sections against CLAUDE.md rules 1–7 (sources cited, ASSUMPTION and NO DATA labels, closing sections, doc matches report) and fix what's wrong; write outputs/R1-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 2: Pressure test and verdict
- [ ] 2.1 Step 6c Interview Guide (PLAYBOOK.md "Step 6"): outputs/06c-interview-guide.md and the doc's Step 6c section; the interviews themselves are an owner line at the end · Opus 5.5 Medium: well-scoped, built from earlier outputs
- [ ] 2.2 Step 7 Sense-Check (PLAYBOOK.md "Step 7"): outputs/07-sense-check.md and the doc's Step 7 section; says the customer voice is missing until the interviews run · Opus 5.5 xHigh: last check before the verdict, steel-mans every conclusion
- [ ] 2.3 Step 8 verdict with the venture suite's skill (PLAYBOOK.md "Step 8", using the defaults above): its venture file, a copy at outputs/08-verdict.md, and the doc's verdict section · Opus 5.5 xHigh: the call everything feeds into
- [ ] R2 Phase 2 review: check 06c, 07 and 08 against CLAUDE.md rules and each other (the verdict answers the sense-check's weak points, the 30-day plan is falsifiable) and fix; write outputs/R2-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 3: Write-up
- [ ] 3.1 Step 9 executive summary (PLAYBOOK.md "Step 9", audience: the founder's dad and the founder, internal): outputs/09-executive-summary.md and the doc's Executive summary section at the top · Sonnet 5.5 xHigh: writes from the verdict, adds no new facts
- [ ] 3.2 Step 10 master report (PLAYBOOK.md "Step 10"): outputs/10-DEUS-strategic-analysis.md; then add a "Data gaps and open questions" section at the end of the doc and check that every section is filled · Sonnet 5.5 xHigh: combines reports, no new claims
- [ ] R3 Phase 3 review: check that 09, 10 and the doc make no claim missing from the step reports and keep every source reference; fix; write outputs/R3-review.md · Opus 5.5 Medium: checks drafts against their sources

## After the run (owner)
- [ ] *owner*: read the doc and comment; when happy, merge with `git push origin analysis:main`
- [ ] *owner*: run the interviews with outputs/06c-interview-guide.md, add the answers to `inputs/deus-fact-sheet.md`, then untick 2.2, 2.3, R2, 3.1, 3.2 and R3 and run `autorun all` again (those sessions replace their doc sections)
