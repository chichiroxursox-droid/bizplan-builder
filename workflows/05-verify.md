# 05 — Verify (adversarial review, fresh eyes)

**Entry check:** confirm `output/plan.md`, `output/financial-model.md`, and
`output/action-sheets/` exist. If not, return to the missing step.

**Run this review in a fresh context:** spawn a subagent whose only inputs are the files
in `output/` and `intake/` — it must not inherit this conversation, so it can't re-assert
your own claims back to you. If subagents aren't available, fall back automatically to
reviewing in-context (never ask the owner to perform a fresh-session ritual).

Attack the plan as a skeptic whose job is to find what's wrong. Fix what you find, then
report what you checked.

## The checklist
1. **Untagged numbers.** Scan the plan, model, and action sheets for any figure without a
   `[VERIFIED]` / `[BENCHMARK]` / `[ASK]` tag. Every bare number is a bug — source it or
   tag it `[ASK]`.
2. **Re-fetch every `[VERIFIED]` source.** For each entry in the Sources section, fetch
   the URL. Dead URL, or the page doesn't state the quoted figure → **demote the claim to
   `[ASK]`** and fix everything downstream of it. This check is mechanical — no judgment
   calls, no "it's probably fine."
3. **Does the model reproduce the present?** (existing business) Re-check it lands within
   ~15% of the bank-account anchor recorded in `intake/interview.md`. If not, the base is
   broken.
4. **Does the model pay the owner?** At what implied hourly rate, and is that stated
   against the local market wage? Is there a tax line? A model that pays the owner $0 is
   the plausible-numbers lie this tool exists to kill.
5. **Can they cash-flow each move — not just profit from it?** Check every growth move's
   cash block against stated capital and financing appetite.
6. **Does the plan reach the outcome?** Trace present → Q1 outcome. If the numbers don't
   actually get there, say so and fix the plan (or the outcome).
7. **Was the reality gate honest?** Read the verdict recorded in `intake/STATE.md`. Did
   the gate arithmetic actually force this verdict? Did any forced condition get quietly
   ignored, or a real risk buried to make the plan look nicer? Restore the honesty.
8. **Arithmetic.** Spot-check the math. Break-even, margins, projections, the cash blocks.
9. **Is it actionable?** Could the owner actually *do* the next action tomorrow?

## Then
Update `intake/STATE.md` (done). Give the owner a short, plain summary: what the plan
concludes, the 2–3 numbers it hinges on and where they came from, the biggest risk, and
the single first action. Point them to the `[ASK]` items — the real numbers that would
sharpen the plan most if they fill them in.
