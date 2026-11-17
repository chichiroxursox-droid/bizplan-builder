# 03 — Build the plan

**Precondition — check before anything else:** read the gate verdict in
`intake/STATE.md`. If it's missing, stop and return to `00-start-here.md` step 3. If it's
RED, only proceed under the disclosure rule (plan sections 1 and 7 open with the RED
verdict and its evidence verbatim).

Build from `intake/interview.md` and `intake/research-notes.md`. Keep every number's tag.
Use `templates/plan.md` and `templates/financial-model.md` as the shape. Write to `output/`.

## The financial model
**Existing business — reproduce the present first (rule 3):**
1. Build the model from their real levers (price × volume − COGS − fixed costs), then:
   - an **implied owner wage** line: take-home ÷ owner hours, compared to the local
     market wage for the same work (from research);
   - an **estimated tax** line (self-employment + income tax, `[BENCHMARK]` fine) so
     "take-home" means after-tax.
2. **Check it lands within ~15% of the bank-account anchor** from the interview. If it
   misses, don't project from a broken base — reconcile with the owner first. Candidate
   explanations to walk through: unbilled jobs, forgotten costs (vehicle repairs, card
   fees), optimistic volume, seasonality averaged away. The levers-vs-bank-account gap is
   often the most useful finding of the whole engagement — treat it that way, not as an
   error to paper over.
3. *Then* project forward to the Q1 outcome: what changes (volume, price, a hire, a
   second unit) and when. Name the ⭐ constraint explicitly and show the path past it.

**New idea — viability-anchored:**
1. Build from `[BENCHMARK]`/`[VERIFIED]` inputs, stating each assumption.
2. Show the break-even: how many units/customers to cover costs, and how long to get
   there. Anchor milestones to *proving* the risky assumption, not revenue fantasy.

**Existing + new offering (hybrid):** model them as **separate lines**, per the rows in
the financial-model template — the core business reproduced against its anchor, the new
offering viability-anchored with its own break-even. Never blend the new line's volume
into the core's economics.

**Every projection, all tracks:**
- If a projection adds a hire or removes owner labor, that labor is repriced at the
  researched market wage — never absorbed at $0.
- Every projected volume increase names its **acquisition channel and cost per customer**,
  tagged. A bare "marketing push" is an invented number — the thing this tool refuses.
- Every growth move gets a three-line **cash block**: upfront cash, estimated months of
  negative cash flow during ramp, worst cumulative dip — each figure
  `[BENCHMARK — stated basis]` or `[ASK]` — compared against growth capital (lever #6)
  and financing appetite. If the dip exceeds their capital, the plan must say financing
  or a smaller version. Profitable-on-paper but bankrupt-in-month-two is the worst
  possible output.

## The plan (output/plan.md)
Sections, each kept tight:
1. **The outcome** — restate Q1 in one line. This is what the plan is *for*.
2. **Where you are now** — the honest present (or, for a new idea, the starting reality).
3. **The constraint** — the one thing most in the way of the outcome (from the ⭐ answer
   + research). The plan is mostly about removing this.
4. **The market** — sized demand, competitors, the wedge — all tagged, with the Sources
   section carried over.
5. **The financial model** — link/summarize `financial-model.md`; present → projection.
6. **The path** — the sequence of moves from now to the outcome, each tied to a trigger
   (a number or event that says "now do this"), not a calendar date.
7. **Risks & honest caveats** — carry forward YELLOW risks and the fact that would have
   made it RED; state what would change the plan. Don't launder them.

Keep the owner's voice and reality in it. Plain language. Update `intake/STATE.md`, then
go to `04-action-sheets.md`.
