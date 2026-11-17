# bizplan-builder

Turns your own Claude Code into an honest business-plan consultant for small local and service businesses. It interviews you, researches your real market with citations, runs an arithmetic viability gate that is allowed to say RED, and finishes with an adversarial review of its own work.

## Why it exists

Most AI business-plan tools fill a template with plausible numbers they made up. This one refuses to state a number it can't source, starts from the outcome you want instead of a template, and tells you plainly when an idea doesn't work.

## How it works

It is a documented workflow, not an app: one instruction file (`CLAUDE.md`), six numbered workflows, and five templates. No API keys, no server. It runs on the owner's own Claude subscription and uses Claude's web search and fetch for research.

- **Every number carries a provenance tag.** `[VERIFIED]` means a figure was quoted from a fetched page listed in Sources. `[BENCHMARK]` is an industry average standing in for the owner's real number. `[ASK]` means only the owner knows it. A number recalled from model memory can never be `[VERIFIED]`.
- **The reality gate is arithmetic, not adjectives.** The verdict (GREEN, YELLOW or RED) has to show its margin math. RED is forced when unit margin is at or below zero once the owner's own labor is priced at the local market wage, or when break-even volume exceeds all the demand evidence found. A YELLOW must name the one fact that would have made it RED. The verdict is written once and never edited.
- **Reproduce the present before projecting.** For an existing business, the financial model must recreate what the owner actually takes home today (within about 15%) before it is allowed to project anything.
- **Mandatory evidence-against pass.** Research has to hunt for disconfirming evidence (closures, saturation, failure modes for the trade) and state the strongest one found.
- **Adversarial verify in a fresh context.** A subagent that did not write the plan re-fetches every cited source and demotes any claim the page doesn't support. It also checks that the model pays the owner a real hourly rate, that each growth move can be cash-flowed, and that the plan actually reaches the stated outcome.
- **Resumable.** State is written to `intake/STATE.md` after every step, so a session that runs out of context or usage picks up where it stopped.

## Example run

[`examples/basketball-lessons/`](examples/basketball-lessons/) is the one complete engagement, run on my own youth basketball coaching side business. It produced a YELLOW verdict with two named risks (a township park ordinance that bars solo paid coaching across the advertised service area, and an outdoor-only model that dies in winter), 29 fetched sources, a three-year plan, a financial model and three quarterly action sheets.

The most useful result was the verify pass. It caught the tool's own fabricated statistic: a pair of youth-sports quit/switch percentages tagged `[VERIFIED]` that the cited page does not state. They were removed from the plan, an action sheet and the research notes. It also caught a cost per lead mislabeled as a cost per client, and a client count treated as a session count. The owner's home neighborhood and ZIP are generalized in this public copy; nothing else was changed.

## Stack

Markdown instructions and templates for [Claude Code](https://claude.com/claude-code). Nothing to install beyond Claude Code itself.

## Run it

You need Claude Code, which requires a paid Claude subscription.

```bash
git clone https://github.com/chichiroxursox-droid/bizplan-builder.git
cd bizplan-builder
claude
```

Then say "Let's build my business plan." Expect a handful of quick questions (rough answers are fine), then a long research stretch you can walk away from. Say "continue my plan" to resume later. Your answers land in `intake/` and the finished plan, model and action sheets in `output/`. Both folders are git-ignored so your business data stays local.

## Status and limits

- One complete real-world run so far (the example above). Treat it as a tested method, not a product with a support promise.
- Research prompts assume a local market. Online-only businesses work, but less well.
- Quality depends on what the web search can reach. Some sources (BLS wage tables, for example) block automated re-fetching, and the verify pass flags those rather than passing them.
- Built with Claude Code. MIT licensed.

*This is an AI-assisted planning workflow, not professional financial, legal or tax advice. Verify every source yourself before borrowing or spending against a plan.*
