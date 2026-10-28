# DEUS Strategic Analysis Playbook

A step-by-step guide for running a deep lookback and strategy analysis of DEUS in **Claude Code (VS Code)**, using the DEUS Company History Recap (Oct 28, 2026) as the main input.

**How to use this file:** put it in the root of your analysis folder, open the folder in VS Code, start Claude Code, and say:

> Read `PLAYBOOK.md` and `CLAUDE.md`, then run Step 0.

Then work through the steps in order, one step per session where possible. Every step saves its output to `outputs/` so later steps can build on earlier ones.

---

## 1. Folder setup

```
deus-analysis/
├── PLAYBOOK.md                 ← this file (rename from DEUS_Strategic_Analysis_Playbook.md)
├── CLAUDE.md                   ← project rules for Claude Code (copy from section 3)
├── inputs/
│   ├── DEUS_Company_History_Recap.pdf
│   ├── DEUS_GBA_Presentation_8.pdf
│   ├── Enhance_Workbench.pdf
│   ├── Potentia_Presentation_for_Parents_5.pdf
│   ├── Document.pdf            ← and any other company files you have
│   └── deus-fact-sheet.md      ← you fill this in during Step 0
└── outputs/                    ← every step writes its report here
```

The presentations matter: they show how DEUS currently pitches, which the analysis should compare against what buyers actually responded to.

---

## 2. Install the skills

Skills are what make each step rigorous instead of generic. They need to be installed in Claude Code separately from claude.ai. See the Claude Code docs for how skills and plugins are installed: https://docs.claude.com/en/docs/claude-code/overview

| Skill(s) | Where it comes from | Install note |
|---|---|---|
| `systems-thinking`, `lean-startup`, `bcg-matrix`, `mckinsey-7s`, `stp`, `pyramid-principle`, `think` | Strategy Frameworks collection: https://github.com/ironyjk/strategy-frameworks | Self-contained. Copy each skill folder into `.claude/skills/` in your project. |
| `icp-profile`, `interview-guide` | The customer research plugin (the same one that provides `feedback-analysis` and `churn-analysis` in claude.ai) | Install the plugin in Claude Code. |
| `new-venture`, `pmf`, `review` | The venture suite plugin | Install the **whole plugin**. `review` calls a devil's-advocate agent and reads files from the other modules, so single skills won't work alone. |
| `engagement-manager`, `sense-check` | The strategy consulting plugin | Install the **whole plugin**. It relies on agents and shared reference files at the plugin root. |

**Check the install:** ask Claude Code *"Which skills do you have available?"* and confirm the names above appear.

**If a skill isn't available:** each prompt below names the method it wants, so Claude Code can still follow it without the skill. The output will be less structured, so install the skill if you can.

---

## 3. CLAUDE.md (copy this into `CLAUDE.md`)

```markdown
# Project: DEUS strategic analysis

## Company context
DEUS (Human Capital and Business Solutions) is an Indonesian HR-tech company with three products:
- DEUS Discover: game-based assessment suite (personality, cognitive, neuroscience, simulation). Games built by Agate International.
- DEUS Enhance: performance management system, originally built around Delamibrands' (DKB) KPI and appraisal needs. Rebuilt by Ko Will.
- Potentia: gamified cognitive assessment for kids, acquired. Has its own website for tokens and purchases.
Current team: 5 people: founder, Ko Will (tech, Enhance), Thania (product), Audrey (marketing and sales),
Bu Sovie (data: Enhance client data cleaning and its manual steps; not psychometrics). Nobody on the team is a psychologist.
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
```

---

## 4. What the analysis needs to explain

The recap records events without interpretation. These are the recurring patterns and open questions the steps below should work through. They are questions, not conclusions.

**Recurring patterns in the history**

- **Build before validate.** Discover was built (almost Rp1 billion with Agate) without psychometric or market validation (Phase 1). Enhance grew around one client's changing requirements (Phases 3–10).
- **Network dependence.** Almost all leads came through the founder's dad's retail network, with near-zero conversion (Phases 5, 9, 11). Cold outreach only started in Phase 11.
- **One-client product.** Enhance was shaped by DKB, which "kept adding more and more features" for three to four years (Phase 10).
- **Quality → churn loop.** Bugs and slow data cleaning ran through Phases 2–8, and BCG, the biggest deal, churned (Phase 8).
- **Team turnover and role overlap.** 19 people besides the founder have worked at DEUS; 4 remain. Overlapping roles (Fizka/Bu Vera), short tenures (Fitri, 3 months), and replacements that didn't fit recur across phases.
- **Vendor dependence.** Agate's shift to the metaverse cost almost a year with Skyfy, plus extra spend to shorten the game (Phase 4).
- **Recognition without revenue.** Startup Studio Indonesia, InnovFest Singapore, and early partner MoMs produced no sales (Phases 2, 5).
- **The one clear win.** Telkom ran two years of MT recruitment with DEUS, partly because Telkom was already looking for gamification vendors (Phase 7).

**Key questions to answer**

1. Is there a buyer type that buys DEUS repeatably, and what does Telkom tell us about it?
2. Is Enhance a product the market wants, or a custom system built for DKB?
3. Can a five-person team sustain three products? Which one deserves the focus?
4. Why did warm leads from the dad's network not convert, and what did F&B, finance, and Apollo outreach reveal?
5. Were the team problems mainly hiring problems, role-design problems, or management problems?
6. What assets are genuinely strong today (game suite, rebuilt Enhance, Telkom case study, team skills)?
7. What is the honest verdict: double down, persevere, pivot, or stop, and on what evidence?

---

## 5. Model for each step

Set the model and effort at the start of each session (`/model`). The picks follow the analysis rows of the model table in `~/.claude/CLAUDE.md` (benchmarks captured 2026-10-25): Opus does the thinking, because it beats Sonnet on the strategy, finance and factual-accuracy indexes at every price and makes up far fewer facts; Sonnet 5.5 xHigh writes the final documents from checked findings; Haiku 5.5 Max only extracts from the files.

| Step | Model + effort | Why |
|---|---|---|
| 0 — Fact sheet | Haiku 5.5 Max | Extracting from the files with a source on every value; the missing ones stay "?" |
| 1 — Systems Thinking | Opus 5.5 High | Framework analysis, finding root causes |
| 2 — Lean Startup | Opus 5.5 High | Framework analysis of product decisions and experiments |
| 3 — ICP Profile | Opus 5.5 High | Judging Backed vs Assumption needs factual accuracy |
| 4 — BCG Matrix | Opus 5.5 High | Market research with citations plus a portfolio call |
| 5 — New Venture (setup) | Haiku 5.5 Max | Filling VENTURE.md from existing outputs |
| 5 — PMF | Opus 5.5 High | Diagnosis from funnel numbers |
| 6a — McKinsey 7S | Opus 5.5 High | Organisation diagnosis |
| 6b — STP | Opus 5.5 High | Choosing the beachhead segment |
| 6c — Interview Guide | Opus 5.5 Medium | Well-scoped, built from earlier outputs |
| 7 — Sense-Check | Opus 5.5 xHigh | The last check before the verdict: it steel-mans every conclusion, and whatever it misses goes straight into Step 8 |
| 8 — Venture Review | Opus 5.5 xHigh | The verdict everything feeds into: best strategy and analysis ranks |
| 9 — Executive summary | Sonnet 5.5 xHigh | Writing from the verdict: best presentation and completeness ranks |
| 10 — Master report | Sonnet 5.5 xHigh | Combining reports, no new claims |
| Alternative: engagement-manager | Opus 5.5 xHigh | One session that also frames the question and builds the final storyline and verdict |

Don't run an analysis step on Sonnet: it scores far lower on factual accuracy, so it is more likely to fill gaps with plausible numbers, which breaks the "never invent numbers" rule.

---

## Step 0 — Build the fact sheet (do this first)

The recap has almost no numbers. Without them, the PMF and Review steps will grade most areas as unknown. Fill in what you can; leave unknowns as "?" and they will show up as data gaps.

**Prompt for Claude Code:**

```
Read inputs/DEUS_Company_History_Recap.pdf and all other files in inputs/.
Create inputs/deus-fact-sheet.md using the template in PLAYBOOK.md Step 0.
Pre-fill every value you can find in the files, with the source next to it.
Leave everything else as "?". Then list the 10 missing numbers that matter most
for judging whether DEUS is viable, and ask me for them one group at a time.
```

**Fact sheet template:**

```markdown
# DEUS fact sheet

## Money
| Item | Value | Source |
|---|---|---|
| Current monthly burn | ? | |
| Cash in bank today | ? | |
| Runway (months) | ? | |
| Total invested to date | ? | |
| Agate: first Discover game | ~Rp1 billion | Recap, Phase 1 |
| Agate: cost to shorten the game | ? | |
| Agate: cost of new games (cognitive, neuro, simulation) | ? | |
| Monthly team cost | ? | |

## Revenue by client
| Client | Product | Price / contract value | Duration | Status | Source |
|---|---|---|---|---|---|
| Boga Group | Discover | ? (600 employees, "low price") | one-off | Ended | Recap, Phase 2 |
| Delamibrands (DKB) | Enhance | ? per month | ? | Ongoing | Recap, Phase 3 |
| Binacitra Group (BCG) | Enhance | ? per month | ? | Churned | Recap, Phases 3, 8 |
| Telkom Indonesia | Discover | ? per year | 2 years | ? | Recap, Phase 7 |
| Sekolah Kristen Calvin | Potentia | ? | ? | ? | Recap, Phase 9 |

## Pricing (current list prices)
| Product | Pricing model | Price |
|---|---|---|
| Discover | ? (per participant / per package) | ? |
| Enhance | ? (per user / per month) | ? |
| Potentia | ? (per token) | ? |

## Funnel by channel
| Channel | Period | Contacts / leads | Replies | Meetings | Proposals | Deals |
|---|---|---|---|---|---|---|
| Dad's network (all waves) | Phases 5–11 | ? | ? | ? | ? | ? |
| Early partners (MoMs) | Phase 2 | ? | | | | 0 |
| InnovFest / Startup Studio | Phase 5 | ? | ? | ? | ? | 0 |
| F&B cold outreach | Phase 11 | ? | "good number" | ? | ? | 0 |
| Finance cold outreach | Phase 11 | ? | "not many" | ? | ? | ? |
| Apollo (Enhance) | Phase 11 | "hundreds" | ? | 0 | 0 | 0 |

## Team
| Item | Value |
|---|---|
| Current headcount | 5 |
| People who have worked at DEUS (excl. founder) | 19 |
| Average tenure of departed staff | ? |

## Founder notes
- Why did Telkom choose DEUS over other gamification vendors? ?
- What reasons did lost leads give for not buying? ?
- What did BCG say when it churned? ?
- How satisfied is DKB today? ?
```

---

## Step 1 — Systems Thinking: why things kept happening

- **Skill:** `systems-thinking`
- **Why:** The history is a set of loops, not a list of separate mistakes. Bugs slowed data work, which hurt clients, which led to churn. Hires were replaced by hires with similar gaps. Stopgaps (Power BI, the dad's network) relieved pressure without fixing causes. This step finds those loops and the leverage points.
- **Output:** `outputs/01-systems-thinking.md`

```
Use the systems-thinking skill on DEUS. Read the recap, the fact sheet, and CLAUDE.md.
1. Build causal loop diagrams (as Mermaid) for the 3–4 most important loops in the history,
   including: product quality → data cleaning → client experience → churn;
   hiring and turnover; lead source dependence; and the Enhance feature-request cycle with DKB.
2. Match each loop to a system archetype (e.g. fixes that fail, shifting the burden,
   limits to growth, success to the successful) and explain the fit with recap evidence.
3. Identify the leverage points: where would one change have broken the loop?
4. Say which loops are still active today with the 5-person team.
Save to outputs/01-systems-thinking.md.
```

---

## Step 2 — Lean Startup: how the products were built

- **Skill:** `lean-startup`
- **Why:** Discover was built before validation; Enhance was built for one client. This step reviews the founding and product decisions through Build-Measure-Learn and checks whether the same pattern is repeating now (new games, rebrand, cold outreach).
- **Output:** `outputs/02-lean-startup.md`

```
Use the lean-startup skill. Read CLAUDE.md, the recap, the fact sheet, the product
presentations in inputs/, and outputs/01-systems-thinking.md.
1. For each product (Discover, Enhance, Potentia), reconstruct the hypotheses DEUS was
   implicitly betting on, and what evidence existed for each at the time.
2. Show where DEUS built without measuring or learning, with recap phase references.
3. Assess the current moves (expanded game suite, rebrand, F&B and finance cold outreach):
   what hypothesis does each one test, and how would DEUS know within 30–60 days?
4. Give a pivot-or-persevere framing per product, with the evidence that would change it.
5. Propose the 3 cheapest experiments DEUS could run next, each with a clear pass/fail metric.
Save to outputs/02-lean-startup.md.
```

---

## Step 3 — ICP Profile: who actually buys

- **Skill:** `icp-profile`
- **Why:** With five clients, everything depends on understanding who bought, why, and how they differ from the leads who didn't. This skill marks each claim as Backed or Assumption, which shows how much current targeting rests on guesses.
- **Output:** `outputs/03-icp-profile.md`

```
Use the icp-profile skill. Read CLAUDE.md, the recap, the fact sheet, and outputs 01–02.
Build the ideal customer profile from DEUS's five clients (Boga Group, DKB, BCG,
Telkom Indonesia, Sekolah Kristen Calvin) and the non-converting leads
(dad's retail network, F&B outreach, finance outreach, Apollo Enhance outreach).
1. Mark every line Backed (with source) or Assumption.
2. Write jobs-to-be-done statements with the four forces for the buyers who did buy.
   Pay special attention to Telkom: it was already looking for gamification vendors.
3. Show the customer DEUS has been assuming next to the customer the evidence shows.
4. Write an anti-profile: which buyers DEUS should stop chasing, with evidence.
5. Do this separately for Discover and for Enhance if the buyers differ.
6. Turn the gaps into questions I can ask real buyers.
Save to outputs/03-icp-profile.md.
```

---

## Step 4 — BCG Matrix: which product deserves the focus

- **Skill:** `bcg-matrix`
- **Why:** Five people, three products, three different markets (corporate HR assessment, performance management, schools and parents). This step forces a portfolio decision.
- **Output:** `outputs/04-bcg-matrix.md`

```
Use the bcg-matrix skill on DEUS's three products: Discover, Enhance, Potentia.
Read CLAUDE.md, the recap, the fact sheet, the product presentations, and outputs 01–03.
1. Place each product on the matrix with the evidence for its position. Where market
   growth or share data is missing, use web research for the Indonesian market and cite it,
   or mark NO DATA.
2. For each product, state the cost of keeping it (team time, vendor cost, sales effort).
3. Recommend: invest, maintain, harvest, or exit for each, and what that means for a
   5-person team in practice.
4. Test the recommendation against the ICP findings in outputs/03-icp-profile.md.
Save to outputs/04-bcg-matrix.md.
```

---

## Step 5 — New Venture + PMF: is there product-market fit?

- **Skills:** `new-venture` (once, to set up the workspace), then `pmf`
- **Why:** PMF diagnoses the core current problem: products are now "ready to sell", but responses aren't turning into deals. Run it per product if the BCG step kept more than one.
- **Output:** files inside `ventures/deus/` (created by the venture suite)

```
Use the new-venture skill to set up a venture workspace for DEUS.
Use CLAUDE.md, the recap, the fact sheet, and outputs 01–04 to fill VENTURE.md.
Set report_language to English.
```

Then:

```
Use the pmf skill on DEUS. Read VENTURE.md and outputs 01–04.
Diagnose product-market fit for the product(s) recommended in outputs/04-bcg-matrix.md.
Use the funnel numbers in the fact sheet. Explain why F&B responses did not convert,
why finance replies are low, and why Apollo produced zero meetings for Enhance.
Give a scored assessment and a measurement plan I can run in the next 30 days.
```

---

## Step 6 — Optional add-ons

Run these if the earlier steps point to them.

**McKinsey 7S — organisation and team** (`mckinsey-7s`) → `outputs/06a-mckinsey-7s.md`

```
Use the mckinsey-7s skill on DEUS. Read CLAUDE.md, the recap (including the people table),
and earlier outputs. Diagnose alignment across strategy, structure, systems, shared values,
style, staff, and skills. Focus on why 19 people came and went: role overlap, hiring
profile, management and guidance (e.g. Ghifari working "with no guidance"), and the
founder's dad's role in decisions. Recommend what the 5-person team needs to work.
Save to outputs/06a-mckinsey-7s.md.
```

**STP — choosing the target market** (`stp`) → `outputs/06b-stp.md`

```
Use the stp skill. Read CLAUDE.md, outputs/03-icp-profile.md and outputs/04-bcg-matrix.md.
Segment the Indonesian market for the focus product, evaluate F&B, finance, and other
segments (including SOEs and large corporates running MT programmes like Telkom), choose
one beachhead, and write the positioning statement. Save to outputs/06b-stp.md.
```

**Interview Guide — getting the customer's voice** (`interview-guide`) → `outputs/06c-interview-guide.md`

```
Use the interview-guide skill. The recap has no direct customer voice. Build an interview
guide for: (a) Telkom, to learn why they chose DEUS; (b) DKB, on current satisfaction;
(c) BCG and Boga Group, on why they left or didn't return; (d) F&B leads who replied but
did not buy. Include a screener, the switch timeline, the four forces, and a note
template. Save to outputs/06c-interview-guide.md.
```

Run the interviews, then add what you learn to the fact sheet before Step 7.

---

## Step 7 — Sense-Check: pressure-test the findings

- **Skill:** `sense-check`
- **Why:** Before any verdict, challenge the conclusions from Steps 1–6 for confirmation bias, cherry-picking, and weak evidence.
- **Output:** `outputs/07-sense-check.md`

```
Use the sense-check skill on all reports in outputs/ so far.
List the main conclusions, test each against the recap and fact sheet, write the
steel-man counter-argument, flag any conclusion that rests on one data point or an
assumption, and say which conclusions are strong enough to act on.
Save to outputs/07-sense-check.md.
```

---

## Step 8 — Venture Review: the verdict

- **Skill:** `review`
- **Why:** The board-meeting step. It grades every area, checks the modules for consistency, runs a mandatory devil's-advocate pass, and commits to one call: double down, persevere, pivot, or kill, with a falsifiable 30-day plan.
- **Output:** inside `ventures/deus/` (venture-review file)

```
Use the review skill on the DEUS venture. Also read every report in outputs/,
especially 07-sense-check.md. What changed since the last review: [write any new
numbers, interview results, cash or runway updates, and how the team is doing].
Give the scorecard, the top 3 risks, one committed recommendation, and the next 30 days.
```

---

## Step 9 — Pyramid Principle: communicate it

- **Skill:** `pyramid-principle`
- **Why:** To present the conclusions clearly to your dad, the team, or anyone else with a stake in the decision.
- **Output:** `outputs/09-executive-summary.md`

```
Use the pyramid-principle skill. Read the venture review and all reports in outputs/.
Write a 2-page executive summary for [audience: e.g. my dad and the team]: the answer
first, then 3 supporting arguments with evidence, then the decision and next 30 days.
Save to outputs/09-executive-summary.md.
```

---

## Step 10 — Master report

```
Combine everything in outputs/ and the venture review into one document:
outputs/10-DEUS-strategic-analysis.md, with these sections:
1. Executive summary (from step 9)
2. What happened: short timeline from the recap
3. Why it happened: loops and root causes (step 1)
4. How we built: validation review (step 2)
5. Who buys: ICP and anti-profile (step 3)
6. Where to focus: portfolio decision (step 4) and target market (step 6b, if run)
7. Product-market fit diagnosis (step 5)
8. Team and organisation (step 6a, if run)
9. Challenges to these conclusions (step 7)
10. Verdict and next 30 days (step 8)
11. Data gaps and open questions
Keep every source reference. Do not add new claims that are not in the step reports.
```

---

## Alternative path: one heavyweight consulting report

Instead of Steps 1–10, you can run **`engagement-manager`**. It runs a full consulting process (problem definition → research → sense-check → storyline → critique → Word report with source notes) and stops at five checkpoints for your approval.

```
Use the engagement-manager skill. The client is DEUS (see CLAUDE.md and inputs/).
The question: what should DEUS focus on in the next 12 months to build a repeatable
revenue engine, given its history in the recap, and which products, segments, and team
setup does that require? Use the recap, fact sheet, and presentations as client data.
```

Choose this if you want a polished document. Choose Steps 1–10 if you want faster, more hands-on thinking where you can steer each step.

**A note on `think`:** the `think` skill can auto-route a problem to frameworks. Its preferred pipeline for "fix a broken business" uses Theory of Constraints tools that come from a separate repo (https://github.com/ironyjk/toc-agents). Unless you install those, choosing the skills above directly gives you more control.

---

## Skills that don't fit (yet)

- `churn-analysis`: built for many cancellation records; DEUS has one churn (BCG).
- `feedback-analysis`: needs 20+ feedback items. Useful later if you collect survey or interview answers at scale.
- `win-loss-review` and other sales-pipeline skills: need a connected CRM with deal history.

---

## Tips for Claude Code

- **One step per session.** Use `/clear` between steps so each one starts focused. The outputs in `outputs/` carry the context forward.
- **Read each report before the next step.** Correct anything wrong in the report file itself, so later steps build on the corrected version.
- **Keep the fact sheet alive.** Every new number or interview answer goes into `inputs/deus-fact-sheet.md`.
- **Push back on Claude.** If a finding feels too soft, ask: *"What's the harshest honest reading of this evidence?"* If it feels too harsh, ask: *"What evidence would contradict this?"*

---

## Checklist

- [ ] Folder set up, files in `inputs/`
- [ ] Skills installed and confirmed
- [ ] `CLAUDE.md` created
- [ ] Step 0 — Fact sheet filled
- [ ] Step 1 — Systems Thinking
- [ ] Step 2 — Lean Startup
- [ ] Step 3 — ICP Profile
- [ ] Step 4 — BCG Matrix
- [ ] Step 5 — New Venture + PMF
- [ ] Step 6 — Add-ons (7S / STP / Interview Guide), if needed
- [ ] Step 7 — Sense-Check
- [ ] Step 8 — Venture Review
- [ ] Step 9 — Executive summary
- [ ] Step 10 — Master report
