# Missing-Information Plan — Paper 4 (Family-as-CAS Calibration)

```
Document:   MISSING_INFO_PLAN — paper 4 gap register
Purpose:    Every piece of information the draft (main.tex) needs but does not
            have, tied to the phase of oha-simulation-v2/docs/FORWARD_PLAN.md
            that produces it, with the action that closes it.
Created:    2026-06-11
Traces to:  main.tex (this folder), practicum proposal §sec:three-step-calibration,
            oha-simulation-v2 docs/FORWARD_PLAN.md (esp. Phase 7),
            docs/experiments/citation_verification.md (family set = empty)
Status:     Active. Close gaps by editing this file with evidence pointers.
```

Draft conventions: `main.tex` flags every gap-dependent statement with
**[LEAD — verify before citing: …]** (G1-class) or **[PENDING — …]** (phase-output-class).
A gap is closed when its flags can be removed with an evidence pointer.

---

## Gap register

### G1 — Verified FAD/SCORE-15 benchmark value table  *(blocks §2.2, §4.2, Table tab:targets)*

- **What's missing:** primary-source-verified values for: FAD domain-score patterns
  (distressed vs. nondistressed), clinical cutoffs, internal-consistency ranges by
  sample type, cross-informant agreement coefficients, role-linked discrepancy
  direction/magnitude (esp. parent–adolescent), SCORE-15 psychometrics, norms,
  change effect sizes / reliable-change behavior, response-format details, and
  whether any published SCORE↔FAD cross-instrument correlation exists (decides
  whether the brief-vs-comprehensive analogy is carried at Rung 2 at all — see
  draft §2.2 "deliberate non-target").
- **Leads (UNVERIFIED — verify against primary sources; do not cite from this list):**
  FAD: Miller/Bishop/Epstein-group reliability-validity and cutoff papers (mid-1980s);
  Kabacoff et al. psychometric study across psychiatric/medical/nonclinical samples
  (~1990); Byles et al. GF-12 study (~1988); later GF short-form reliability work;
  multilevel/informant-variance FAD analyses; family informant-agreement studies.
  Informant discrepancy generally: the canonical informant-discrepancy review
  literature (De Los Reyes–style, clinical assessment focus — check applicability).
  SCORE: Stratton et al. 2010 SCORE development (J Fam Ther); SCORE-15 psychometric
  + responsiveness studies and norms from the Stratton and Carr research groups
  (~2013–2017); systematic reviews of SCORE psychometrics.
- **Forward-plan anchor:** OQ-DYN-2 (SDD-DYN §7), PR-6 prerequisite (§2 item 6),
  §5 citation rule. Output lands as the **family set** in
  `oha-simulation-v2/docs/experiments/citation_verification.md`, same table format
  as the GAD-7 set.
- **When:** **start now** — pure literature work, no GPU, no Rung-1 dependency.
  Natural slot: the Phase-5/6 "writing lull" the plan already uses for D-3.
- **Done when:** citation_verification.md family set exists; Table tab:targets cells
  fillable for both branches; all \lead{} flags in §2.2 cleared or the corresponding
  target dropped.

### G2 — Family-level floors and nulls are not in FORWARD_PLAN Phase 7  *(blocks §4.3, §5.1)*

- **What's missing:** Phase 7 currently specs only the perception-off null +
  role-sensitivity sweep (SR-VAL-007/E8) and divergence decomposition (SR-ANA-010).
  It has **no** FAD/SCORE-15 contamination floors (E1 analog), no noise floor
  re-measure under family-run concurrency, no single-agent persona null (E2 analog),
  and no biography→family-channel activity gate (E5 analog).
- **Proposed Phase 7 amendment** (mirrors Phase 2 step 4, Phase 3 step 3, and the
  Phase 6 GAD-7 "channel-PASS gates the read" pattern):
  - new step 0a: re-measure C0 noise floor per family instrument at Rung-2 serving
    concurrency; register as named baselines;
  - new step 0b: C1 naive floors per architecture for FAD-class and SCORE-15-class
    signatures (distributions, discrepancy patterns, change behavior);
  - new step 0c: C2 single-agent persona null arm budgeted into every calibration
    cell matrix;
  - new step 3a: binding family-channel activity gate G (class separation over noise
    floor through the biography channel + relational encoding-fidelity margin),
    pass required before any calibration read.
- **Forward-plan anchor:** Phase 7 steps 1–5; threat T1/T2/T4 extension to Rung 2.
- **When:** spec edit now (Phase-0-style docs work); runs execute inside Phase 7.
- **Done when:** FORWARD_PLAN Phase 7 amended (PI-approved) and PR-6b carries the
  control thresholds.

### G3 — PR-6a/PR-6b not yet written  *(blocks §4.1; Appendix A is the skeleton)*

- **What's missing:** the two registrations themselves (perception/dynamics rules +
  freeze; dual-branch targets + controls + power + verdict templates).
- **Forward-plan anchor:** §2 item 6 ("written before any FAD/SCORE-15 calibration
  run"); PreregistrationGuard enforcement.
- **When:** draftable after G1 (values) and G4 (branch) resolve; rule *forms* and
  verdict templates draftable now from Appendix A.
- **Done when:** both files committed to
  `oha-simulation-v2/docs/experiments/preregistrations/` with hashes predating any
  Rung-2 cell inspection.

### G4 — Licensing requests to FAD and SCORE-15 rights holders  *(decides Branch A/B; blocks §3.6 finalization)*

- **What's missing:** identification of current rights holders / permission channels
  for FAD and SCORE-15, the requests themselves, and the recorded outcomes. The
  proposal commits to requesting permission; no request artifacts exist in-repo.
- **Forward-plan anchor:** SR-INS-004 (hash-only storage), CON-006, OQ-INS-2
  (where authorized item text lives); Phase 7 step 1.
- **When:** **start now** — longest external lead time of any gap; the dual-branch
  design means drafting is not blocked while waiting.
- **Done when:** branch declaration recorded (per §3.6 rule) before PR-6b commit.

### G5 — Family state vector, class map, bands, relational encoding checks  *(blocks final §3.2, §3.5 wording)*

- **What's missing:** v2 spec-level commitments: the TargetSystem family state
  vector (draft §3.2 carries the v1-bridge-derived working set as a proposal),
  the DiagnosticClassMap analog for family classes with pre-stated bands (ordinal-only
  where no licensed cutoff exists — D-7 precedent), and the SR-RCC-013/014 analogs
  for relational frequency/intensity texture + the validator list extension.
- **Forward-plan anchor:** Phase 7 step 2 (CSC-RCC-SYS); Phase-0-style SRS/SDD/RTM
  edits; v1 FAMILY_SYSTEM_BRIDGE.md is design-concept input only (no code reuse).
- **When:** spec edits now; independent of GPU work.
- **Done when:** SRS/SDD-RCC/SDD-DYN amended with the family analogs and RTM rows.

### G6 — Rung-1 inheritances  *(blocks §2.1 placeholders, §4.4–§4.5 constants, all of §5)*

- **What's missing:** the selected architecture (Phase 4 bake-off + PR-3), frozen
  process weights + temperature (Phase 5, PR-4/PR-5), Rung-1 register verdicts and
  the paper-3 evidence bundle (Phase 6).
- **Forward-plan anchor:** Phases 4–6 outputs, DD-DYN-001 (Rung 2 reuses the
  calibrated engine).
- **When:** automatic as the program executes; nothing paper-side to do except keep
  the placeholders honest.
- **Done when:** \pending{Phase 4/5} flags in §2.1, §4.5 replaced with frozen values
  + run IDs.

### G7 — Timeline reconciliation (proposal vs. forward plan)  *(committee-facing; blocks no section)*

- **What's missing:** a PI decision resolving the contradiction: proposal commits
  Step-2 "execution and reporting" to Summer 2026 in parallel with Step 1;
  FORWARD_PLAN sequences Rung 2 (Phase 7) strictly after the Rung-1 freeze
  (DD-DYN-001, SR-DYN-005).
- **Options:** (a) parallel-build/sequential-runs — Rung-2 engineering (G2 spec
  edits, G1 verification, G3 drafting, G4 requests, CSCI-DYN build) proceeds now,
  binding calibration runs wait for the freeze; Summer-2026 reporting covers Step-2
  *readiness*; (b) revise proposal language to match the plan sequencing.
  Recommendation: (a) — it preserves both documents' commitments with one wording
  change in committee communications.
- **When:** decide before the next committee-facing status report.

### G8 — Power/N for family cells  *(blocks PR-6b §3, §4.5 numbers)*

- **What's missing:** measured variance inputs — C0 noise floor at Rung-2
  concurrency (G2 step 0a) and between-family variance from Phase-7 pre-runs —
  plus the per-cell cost constants (c_arch from Phase 4; M, T, I from PR-6a design
  choices).
- **Forward-plan anchor:** Phase 4 noise-floor re-measure precedent (Revision 1
  item 1); PR-3 power-analysis pattern (floor-relative effect scales,
  compression-conservative effect sizes per P6).
- **When:** after Phase 4; computed during PR-6b drafting.
- **Done when:** PR-6b power section committed; §4.5 carries the formula *with*
  committed values.

### G9 — E4 / D-3 obscure-instrument decision  *(bounds §6 transfer language)*

- **What's missing:** the obscure-but-real transfer instrument decision (OQ-VAL-1,
  decision flag D-3) that caps what *any* rung may say about transfer. Paper 4's
  Discussion must not promise Rung-3 transfer language that D-3's outcome could
  retract.
- **Forward-plan anchor:** Phase 7 step 6 (sequenced there deliberately).
- **When:** Phase-6 writing lull, per plan.
- **Done when:** register entry for T3/E4 updated; §6 transfer wording checked
  against it.

---

## Sequencing summary (what can start today, in order of leverage)

1. **G1** benchmark verification → unblocks PR-6b targets and §2.2 (no dependencies).
2. **G4** licensing requests → longest external latency; decides Branch A/B.
3. **G2 + G5** spec amendments to FORWARD_PLAN Phase 7 / SRS / SDDs (docs only).
4. **G3** PR-6a rule-form + verdict-template drafting from Appendix A.
5. **G7** timeline decision before the next committee communication.
6. G6/G8/G9 close automatically as Phases 4–7 execute.

## What the draft may NOT do while gaps are open

- State any FAD/SCORE-15 numeric benchmark as established (G1).
- Declare Branch A or B (G4).
- Replace any \pending{} shell in §5 with content (G6 + Phase 7).
- Claim novelty of the multi-informant LLM-psychometrics intersection without the
  G1-adjacent novelty sweep (flagged in §2.3).
