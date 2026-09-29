# Board Devil's Advocate

**An independent AI challenger that tests every board proposal before the meeting.**

Boards rarely fail for lack of information. They fail because the hard question never gets asked: the sponsor is senior, the deck is polished, the deadline is close, and nobody wants to be the one who slows things down. Board Devil's Advocate makes that question routine. Every proposal is challenged the same way, by a reviewer with no stake in the outcome, and directors walk into the room with the questions already written.

**[Open the live demo](https://utaknablein.github.io/board-devils-advocate/)**

---

## What it does

When the board pack is locked, each proposal is run through eight fixed lenses:

| # | Lens | The question behind it |
|---|------|------------------------|
| 1 | Premise | What must be true for this to work, and which of it is asserted rather than evidenced? |
| 2 | Outside view | How do decisions of this type usually turn out, and why would this one be different? |
| 3 | Evidence | Who produced the key numbers, and are they independent of the outcome? |
| 4 | Alternatives | What options never reached the board, including doing less, later, or nothing? |
| 5 | Downside | What is the worst plausible outcome, and how reversible is the decision? |
| 6 | Incentives | Who benefits from approval, and where does the urgency come from? |
| 7 | Execution | Does the organization have the capacity, and what gets displaced? |
| 8 | Pre-mortem | Two years from now this has failed. What is the most likely story? |

Directors receive a one-page **challenge brief**: a headline naming the single most important thing to test, a finding and an "ask in the room" question for each lens, conditions a prudent board might attach, and the evidence that would change the analysis.

## Design principles

- **It never recommends the vote.** The decision belongs to the board. The product improves the quality of the question, not the answer.
- **Independent of the sponsor.** Management submits the paper but cannot edit the brief. The system prompt is published so everyone can see exactly what the challenger is told.
- **Challenges reasoning, never people.** Findings point to numbers, claims, assumptions and absences in the paper.
- **Consistent.** The same eight lenses every time, so the challenge becomes an expected part of governance rather than a personal act of dissent.
- **Honest about what it knows.** General patterns are labeled as general. The challenger does not invent facts about the company.

## Where it goes: pattern memory

The premium enterprise product keeps a private **decision ledger** for each board: every proposal, every challenge, the decision taken and, later, the outcome. Over time it can tell a board how its *own* past decisions of a given type actually turned out, for example "acquisitions approved under a seller-imposed deadline delivered about half their planned synergies." That is institutional memory most boards lose every time a director rotates off.

See [`docs/product-brief.md`](docs/product-brief.md) for positioning, buyers and roadmap.

## What's in this repo

```
index.html                           Interactive demo (GitHub Pages)
prompts/challenge-system-prompt.md   The full challenger instructions, published for transparency
docs/methodology.md                  The eight lenses, severity scale and brief format in detail
docs/product-brief.md                Product vision, buyers, trust model and roadmap
```

## Try it

The demo ships with three fictional proposals (an acquisition, an AI customer-service rollout and a market entry) with complete challenge briefs. You can also paste your own proposal. No sign-up or API key is needed:

- **Challenge instantly** runs a rules-based engine entirely in your browser. It checks the proposal against the eight lenses (unsourced figures, missing alternatives, irreversible commitments, deadline pressure, unclear ownership and more) and produces a brief in the same format. Nothing you paste leaves the page.
- **Run the full challenge in Claude** opens Claude in your own account with the challenger prompt and your proposal filled in, for a fully reasoned brief.

Please do not paste confidential board material into a public demo.

To run locally, open `index.html` in any browser. No build step.

## About

Board Devil's Advocate is a concept by **Uta Knablein**: former Chief Product Officer at iHeartMedia, Section 16 Officer at WW International, ICF PCC executive coach, and member of European Women on Boards, the Institute of Directors and FidAR. It sits alongside her work on decision quality and AI governance: see also [engine-diagnostic](https://github.com/utaknablein/engine-diagnostic).

Built with Claude.

## License

Copyright © 2026 Uta Knablein. All rights reserved. The demo code is shared for viewing and evaluation; see [LICENSE](LICENSE).

## Privacy

The demo counts page visits and button clicks with [GoatCounter](https://www.goatcounter.com), an open-source, cookie-free analytics service that collects no personal data. Text you paste into the demo is never sent anywhere.
