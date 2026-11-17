# 00 — Start here (orchestration)

Run these in order. Tell the owner where they are. Don't skip the reality gate.

**State discipline:** after finishing any step, update `intake/STATE.md` (copy
`templates/STATE.md` on first use): current step, verdict if issued, next action, open
`[ASK]` items. If a session ever starts and STATE.md exists, resume from the step it
names — never re-ask what `intake/interview.md` already answers.

## The flow

1. **Interview** → `workflows/01-interview.md`
   Produces `intake/interview.md`. Advance when you know: new / existing / existing-plus-
   new-offering, the outcome, the bank-account anchor (existing), and rough numbers for
   the levers (or `[ASK]` tags where you don't).

2. **Research** → `workflows/02-research.md`
   Produces `intake/research-notes.md` with a Sources section and a **viability verdict**
   (GREEN / YELLOW / RED) computed by the gate conditions below.

3. **⚑ REALITY GATE** (do not skip — this is rule 4)
   Apply the gate conditions from `02-research.md` exactly as written. The verdict must
   show the margin arithmetic, not adjectives. When issued, write a dated verdict block
   into `intake/STATE.md`: the verdict, the 2–3 facts that drove it, and (for YELLOW) the
   specific fact that would have made it RED.

   - **GREEN — viable, proceed.** Real demand, real margin, a plausible wedge, no forced
     conditions tripped. → Step 4.
   - **YELLOW — viable with named risks, or a core number still `[ASK]`.** Tell the owner
     the risks plainly, get a nod, then build the plan *with those risks baked in*.
     YELLOW is not a stall — it still produces the full plan, with the gap named. → Step 4.
   - **RED — the arithmetic doesn't work.** Say so gently and clearly, with the evidence —
     never dress a doomed idea in a nice plan. For an existing business, the wording rule:
     *"this growth move doesn't pencil out — your current business is the asset we build
     from"* — never words that condemn the business itself. Then **reframe**:
       - Point out what they *do* have (skill, customers, location, equipment, a real
         sub-niche inside the crowded one).
       - Brainstorm 2–3 **adjacent** directions that reuse those assets and dodge what
         killed the first idea.
       - When they pick one, **carry `intake/interview.md` forward** — prices, costs,
         capacity, capital, and the constraint mostly survive a pivot. Ask only the 2–4
         questions that actually change, then rejoin at step 2.
     A red verdict is not a failure of the exercise — catching it *is* the value.

   **If the owner insists on a plan after RED:** build it — but plan sections 1 and 7
   must open with the RED verdict and its evidence verbatim, and the verdict record in
   STATE.md is never edited. You may be overruled on building; never on the verdict.

4. **Build the plan** → `workflows/03-build-plan.md`
   Precondition: a GREEN or YELLOW verdict recorded in STATE.md (or RED + the disclosure
   rule above). Produces `output/plan.md` and `output/financial-model.md`.

5. **Action sheets** → `workflows/04-action-sheets.md`
   Produces `output/action-sheets/`.

6. **Verify** → `workflows/05-verify.md`
   Adversarial review in a fresh context. Fix what it finds, then you're done.

## Posture throughout
Honest consultant, not a cheerleader. One question at a time. Every number tagged.
The owner's outcome is the north star — if a step doesn't move them toward it, say so.
