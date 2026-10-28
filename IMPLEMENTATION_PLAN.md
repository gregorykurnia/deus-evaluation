# DEUS strategic analysis: autorun plan

Runs Steps 1–10 of `PLAYBOOK.md` (Phases 1–3), then revises them with the founder answers (Phases 4–5), one fresh session per line, on the model picked in `PLAYBOOK.md` §5.
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
- [x] 1.4 Step 4 BCG Matrix (PLAYBOOK.md "Step 4"): outputs/04-bcg-matrix.md and the doc's Step 4 section · Opus 5.5 High: Indonesian market research with citations plus a portfolio call
- [x] 1.5 Step 5 setup with the new-venture skill (PLAYBOOK.md "Step 5", first prompt): the ventures/deus/ workspace, no doc section · Haiku 5.5 Max: fills VENTURE.md from existing outputs
- [x] 1.6 Step 5 PMF with the pmf skill (PLAYBOOK.md "Step 5", second prompt): its venture file, a copy at outputs/05-pmf.md, and the doc's Step 5 section · Opus 5.5 High: diagnosis from the funnel numbers
- [x] 1.7 Step 6a McKinsey 7S (PLAYBOOK.md "Step 6"): outputs/06a-mckinsey-7s.md and the doc's Step 6a section · Opus 5.5 High: organisation diagnosis
- [x] 1.8 Step 6b STP (PLAYBOOK.md "Step 6"): outputs/06b-stp.md and the doc's Step 6b section · Opus 5.5 High: chooses the beachhead segment
- [x] R1 Phase 1 review: check outputs 01–06b and their doc sections against CLAUDE.md rules 1–7 (sources cited, ASSUMPTION and NO DATA labels, closing sections, doc matches report) and fix what's wrong; write outputs/R1-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 2: Pressure test and verdict
- [x] 2.1 Step 6c Interview Guide (PLAYBOOK.md "Step 6"): outputs/06c-interview-guide.md and the doc's Step 6c section; the interviews themselves are an owner line at the end · Opus 5.5 Medium: well-scoped, built from earlier outputs
- [x] 2.2 Step 7 Sense-Check (PLAYBOOK.md "Step 7"): outputs/07-sense-check.md and the doc's Step 7 section; says the customer voice is missing until the interviews run · Opus 5.5 xHigh: last check before the verdict, steel-mans every conclusion
- [x] 2.3 Step 8 verdict with the venture suite's skill (PLAYBOOK.md "Step 8", using the defaults above): its venture file, a copy at outputs/08-verdict.md, and the doc's verdict section · Opus 5.5 xHigh: the call everything feeds into
- [x] R2 Phase 2 review: check 06c, 07 and 08 against CLAUDE.md rules and each other (the verdict answers the sense-check's weak points, the 30-day plan is falsifiable) and fix; write outputs/R2-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 3: Write-up
- [x] 3.1 Step 9 executive summary (PLAYBOOK.md "Step 9", audience: the founder's dad and the founder, internal): outputs/09-executive-summary.md and the doc's Executive summary section at the top · Sonnet 5.5 xHigh: writes from the verdict, adds no new facts
- [x] 3.2 Step 10 master report (PLAYBOOK.md "Step 10"): outputs/10-DEUS-strategic-analysis.md; then add a "Data gaps and open questions" section at the end of the doc and check that every section is filled · Sonnet 5.5 xHigh: combines reports, no new claims
- [x] R3 Phase 3 review: check that 09, 10 and the doc make no claim missing from the step reports and keep every source reference; fix; write outputs/R3-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 4: Revise Steps 1–6 with the founder answers (2026-10-28)
Defaults for Phases 4 and 5 (so no task stops to ask): the founder answered the Steps 1–5 questions on 2026-10-28; they
are in `inputs/deus-fact-sheet.md`, sections "Corrections to the recap and earlier steps" and "Founder answers". Each
task revises its existing report in place: apply every correction (DEUS did not buy the Phase 11 games and is one of five
Agate sales partners for Next Chapter; Telkom's buyer was its Assessment Center, reached through Agate, and stopped when
its MT intake strategy changed; BCG churned over bugs and service; the dad is the funder and will keep supporting; the
founder has the final say), re-judge every conclusion that rested on the old facts, mark answered questions as answered
and keep the rest. The founder answers are the founder's account, not buyers' words: the interviews still have not run,
so reports stay provisional. The dad's willingness to keep funding is a fact; whether a written limit is still needed is
the analysis's call (rule 3 applies). Each rerun replaces its own doc section (ids from a `read` of the doc's outline).
- [x] 4.1 Revise Step 1 Systems Thinking (PLAYBOOK.md "Step 1"): outputs/01-systems-thinking.md and its doc section; Loop 5 (build/buy) and the Telkom origin change most · Opus 5.5 High: re-judges the loops every later step reads
- [ ] 4.2 Revise Step 2 Lean Startup (PLAYBOOK.md "Step 2"): outputs/02-lean-startup.md and its doc section; also answers the founder's question "if I run Enhance as a DKB service contract, is that still fine as a business model?" in its own section · Opus 5.5 High: re-judges hypotheses with the lost-deal reasons and validation status
- [ ] 4.3 Revise Step 3 ICP Profile (PLAYBOOK.md "Step 3"): outputs/03-icp-profile.md and its doc section; the Telkom ICP becomes an assessment center reached through Agate, the logos are sub-brands of paying groups · Opus 5.5 High: Backed vs Assumption needs factual accuracy
- [ ] 4.4 Revise Step 4 BCG Matrix (PLAYBOOK.md "Step 4"): outputs/04-bcg-matrix.md and its doc section; add the Enhance server cost and the Rp30 juta Enhance quote, and re-place Discover now that the suite is a non-exclusive partnership · Opus 5.5 High: portfolio call
- [ ] 4.5 Update ventures/deus/VENTURE.md from the revised outputs 01–04 and the fact sheet's corrections; no doc section · Haiku 5.5 Max: fills a file from given files
- [ ] 4.6 Revise Step 5 PMF with the pmf skill (PLAYBOOK.md "Step 5", second prompt): its venture file, outputs/05-pmf.md and its doc section; DKB's 300–400 users and satisfaction, BCG's churn reason, the funnel's new reasons · Opus 5.5 High: diagnosis from the funnel numbers
- [ ] 4.7 Revise Step 6a McKinsey 7S (PLAYBOOK.md "Step 6"): outputs/06a-mckinsey-7s.md and its doc section; departures, no success metrics, Ko Will as key person, the founder's final say · Opus 5.5 High: organisation diagnosis
- [ ] 4.8 Revise Step 6b STP (PLAYBOOK.md "Step 6"): outputs/06b-stp.md and its doc section; the beachhead now has to account for Agate's four other partners and the assessment-center buyer · Opus 5.5 High: chooses the beachhead segment
- [ ] 4.9 Revise Step 6c Interview Guide (PLAYBOOK.md "Step 6"): outputs/06c-interview-guide.md and its doc section; drop questions the founder answered, note BCG and Boga won't engage, add Agate and Telkom's Assessment Center as interviewees · Opus 5.5 Medium: well-scoped, built from earlier outputs
- [ ] R4 Phase 4 review: check revised 01–06c and their doc sections against CLAUDE.md rules 1–7 and the fact sheet's corrections (no report still says DEUS bought the Phase 11 games, Telkom is named as its Assessment Center, BCG's churn reason matches) and fix; write outputs/R4-review.md · Opus 5.5 Medium: checks drafts against their sources

## Phase 5: Pressure test, verdict and write-up again
- [ ] 5.1 Rerun Step 7 Sense-Check (PLAYBOOK.md "Step 7"): outputs/07-sense-check.md and its doc section, from the revised 01–06c · Opus 5.5 xHigh: steel-mans every conclusion before the verdict
- [ ] 5.2 Rerun Step 8 verdict (PLAYBOOK.md "Step 8"; "what changed since the last review" = the founder answers of 2026-10-28): its venture file, outputs/08-verdict.md and its doc section; answers the founder's questions of 2026-10-28 (is Enhance as a DKB service contract a fine business model; is DEUS still worth continuing and in what way; what to do from here to make it profitable); new dates count from the rerun date · Opus 5.5 xHigh: the call everything feeds into
- [ ] 5.3 Rerun Step 9 executive summary (PLAYBOOK.md "Step 9", same audience): outputs/09-executive-summary.md and its doc section · Sonnet 5.5 xHigh: writes from the verdict, adds no new facts
- [ ] 5.4 Rerun Step 10 master report (PLAYBOOK.md "Step 10"): outputs/10-DEUS-strategic-analysis.md; replace the doc's "Data gaps and open questions" section and check every section is filled · Sonnet 5.5 xHigh: combines reports, no new claims
- [ ] 5.5 Revise Step 11 top 10 reasons (same brief as its header): outputs/11-top-10-reasons.md and its doc section, from the revised reports · Opus 5.5 High: re-ranks causes with the corrected facts
- [ ] 5.6 Revise Step 12 time-machine rerun (same brief as its header): outputs/12-time-machine-rerun.md and its doc section; the rerun's channel now includes Agate referrals · Opus 5.5 High: a judgement built on Steps 1–11
- [ ] R5 Phase 5 review: check 07–12 and the doc against CLAUDE.md rules and each other (the verdict answers the sense-check, 09–12 make no claim missing from the step reports, no stale "bought the games" or "Telkom" wording) and fix; write outputs/R5-review.md · Opus 5.5 Medium: checks drafts against their sources

## After the run (owner)
- [ ] *owner*: read the doc and comment; when happy, merge with `git push origin analysis:main`
- [ ] *owner*: run the interviews with outputs/06c-interview-guide.md, add the answers to `inputs/deus-fact-sheet.md`, then untick 5.1–5.6 and R5 and run `autorun all` again (those sessions replace their doc sections)
