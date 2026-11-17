# 02 — Research (real, cited) + the gate verdict

Goal: replace guesses with verified facts, and compute an honest verdict on whether this
works. Use your web search/fetch. Write findings to `intake/research-notes.md`.

## Tag discipline (rule 2, enforced here)
- `[VERIFIED — source, date]` is legal ONLY for a fact you fetched **in this session**.
  Every `[VERIFIED]` gets a numbered entry in a **Sources** section at the bottom of
  `intake/research-notes.md`: the URL + the figure as quoted on the fetched page. The
  inline tag stays short; the Sources section carries the receipt.
- A number you recall from training memory is NOT verified — tag it
  `[BENCHMARK — model estimate, unverified]` at best.
- Found only an industry average? `[BENCHMARK — source]`. Found nothing usable?
  `[ASK — owner]`.

## What to verify (chase the numbers the plan will need)
- **Demand / market size** — real, sized demand in their area? Census (population,
  businesses, income), industry reports, search-trend signals. For a new idea, this is
  the make-or-break number.
- **Labor / wages** — what a hire costs locally (BLS wage data by occupation + metro, or
  local job postings). Also fetch the local market wage for the owner's *own* trade —
  the model prices their labor with it.
- **Competitors** — who else does this locally, how many, what they charge, what they're
  weak at. Actually search the local market; pull real prices where listed.
- **Materials / COGS reality** — sanity-check their cost answer against real supplier or
  market pricing.
- **Regulatory basics** — licensing, permits, insurance the business legally needs. Flag
  anything that's a wall for a small operator.
- **If demand-bound** (from the ⭐ fork): local customer-acquisition cost signals —
  Google Ads CPC / Local Services Ads pricing for this trade and metro `[BENCHMARK]`.

For a NEW idea, aim your sharpest research at the "one assumption that sinks it."

## The evidence-AGAINST pass (mandatory — do not skip)
Before any verdict, actively search for disconfirming evidence: businesses like this
that closed or churn locally, saturation arithmetic (competitor count vs. demand),
common failure modes for this trade. The verdict paragraph must state the **single
strongest disconfirming fact you found** — if you found none, say what you searched.

## The gate conditions (compute, don't vibe)
Do the arithmetic and show it. These conditions force the verdict:

- **Forced RED:** unit margin ≤ 0 at the owner's price and benchmark costs — *including
  the owner's labor priced at the local market wage for that work*.
- **Forced RED:** break-even volume exceeds all demand evidence found.
- **Forced YELLOW:** required license/equipment/capital exceeds stated growth capital →
  the plan must include a financing path (lever #6 is "not a commitment"; loans are a
  normal path — a capital gap alone is never RED).
- **Cap at YELLOW:** the core margin or demand number is still `[ASK]` — no GREEN on an
  unknown core number. (YELLOW still builds the full plan, with the gap named.)
- Owner currently earning under the local median wage is a **stated fact** in the
  verdict, never an automatic downgrade.

Write the verdict block at the top of `intake/research-notes.md`:
- **GREEN / YELLOW / RED**, the margin arithmetic that produced it (numbers, not
  adjectives), the 2–3 driving facts, the strongest disconfirming fact.
- **YELLOW must name the specific fact that would have made it RED.**

Then return to `00-start-here.md` step 3 (the reality gate), record the dated verdict in
`intake/STATE.md`, and proceed per the gate. **Report the verdict the arithmetic
produced** — a YELLOW dressed as GREEN, or a RED softened into a plan, defeats the entire
purpose of this tool.
