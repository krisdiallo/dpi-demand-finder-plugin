# Methodology — the loop, the rules, the rubric

Read this before any flow. It's the logic the whole system runs on. The user-facing language stays plain; this file is for you.

## Two non-negotiable framings

- **Pre-build.** DPIs happen *before* anything is built. You're testing a thesis about a problem and a persona — not a product. The deliverable is a go/no-go on the problem.
- **Solution-independent.** A DPI never discusses, describes, or tests a solution. The "will they pay" question is answered by what people *already spend* (time/money/effort) on the problem today — never by pitching something. If a solution enters the conversation, the interview is contaminated; flag it.

## The loop

```
THESIS (stated to disprove)  +  PERSONA (who can kill it)
        → pick the weakest-evidence KILL-CRITERION
        → pull its questions from the bank
        → run the interview (favor disconfirmation)
        → capture: behavior, disconfirming evidence, non-indifference score
        → update kill-criteria status + add a ledger row
        → refine thesis confidence
        → write 3 sharper questions back into the bank
        → repeat
```

The arrow back into the question bank is what makes the system intelligent: each interview rewrites the next interview's questions to attack whatever is still soft.

## Why it compounds (keep all three edges alive)

1. **Questions sharpen.** After each interview, retire questions that fell flat; add 3 aimed at the weakest kill-criterion.
2. **Criteria harden.** A criterion can't be marked safe on one nice comment — it needs repeated *behavioral* confirmation. The bar rises as evidence accumulates.
3. **Personas get specific.** Each interview teaches who actually feels the pain vs. who just talks. The persona map narrows toward a named beachhead.

## The canonical "what could kill it" categories

In Setup, turn each relevant category into a specific, checkable kill-condition for the user's thesis. Not all apply to every idea; pick 5–7 that fit.

| Category | The killer, in plain words | Disconfirms if… | Confirms (survives) if… |
|---|---|---|---|
| **Indifference** | People are fine living with the problem | they shrug, "we manage," "not a priority" | behavioral compulsion — they've acted, paid, or done it themselves |
| **They cope fine** | A good-enough workaround already exists | the workaround is genuinely OK | the workaround keeps failing and they keep patching it |
| **The thing they need isn't rare / is rare** | (idea-specific) supply is easy, or the special ingredient doesn't exist | they find/solve it in normal time | "nobody can find/do this," long waits, premiums |
| **No one will pay** | Real pain, but not buyable — no budget, won't outsource | no budget owner, "we'd never pay for that" | named budget, existing spend, a buyable shape |
| **A fad / tech will erase it** | The need evaporates as technology improves | they expect it to shrink, treat it as a stopgap | they expect it to grow |
| **Someone already solves it** | Incumbents cover this; no wedge | happily served by an existing option | existing options described as broken/absent; workarounds cobbled together |
| **Too few people have it** | Pain is real but concentrated in a handful | shows up in only 1–2 outliers | recurs across size, stage, and segment |

Every kill-criterion gets an ID (KC-1, KC-2, …), a "disconfirms if / confirms if," a status, an evidence-strength note, and the interviews touching it.

## Statuses

**Kill-criterion:** `Open` (untested) · `Probing` (some evidence, not conclusive) · `Derisked` (survived, per threshold) · `Triggered` (the killer looks real — revise the thesis).

**Evidence strength:** `Weak` (verbal/hypothetical) · `Moderate` (specific story, no artifact) · `Strong` (behavior + artifact: invoice, job req, cancelled tool, calendar block, founder doing the work).

**Non-indifference (0–5):** 0 = "fine as is" → 5 = "on fire, acting now." Below 3 across a persona = indifference = a demand problem.

## Decision rules (so the founder doesn't fool themselves)

Deliberately strict; default to *not* believing.

- **Evidence > opinion.** A claim counts only if tied to a behavior in the last ~90 days. "I would pay" is not evidence; "here's the invoice / the req we left open 5 months" is.
- **One disconfirmation is louder than three confirmations.** Any qualified "it'd be OK to not solve this" → log as strong disconfirming evidence immediately.
- **Derisked threshold:** mark Derisked only after **≥3 independent interviews** from the correct persona layer give *behavioral* confirmation, with **zero unresolved strong disconfirmations**.
- **Triggered threshold:** mark Triggered the moment **≥2 independent** qualified people give behavioral evidence the killer is real. A Triggered criterion forces a thesis revision — stop interviewing around it.
- **Buyer beats user for demand.** Users feel pain; only the economic buyer proves demand. Weight 2nd/3rd-order buyer evidence higher on anything about money.
- **Talk-time discipline.** If the founder spent >5% of the interview talking about their solution, flag it as low-quality — they were selling, not discovering.
- **Coverage honesty.** A criterion isn't tested until ≥2 *different* people have hit it. One enthusiast is an anecdote.
- **Transcript > recollection.** A verbatim transcript is the gold-standard source. A founder's after-the-fact braindump is acceptable but weaker — memory drops the disconfirming details. Record the source on each DPI; weight recollection-based evidence one notch lower and never let it alone clear the Derisked bar.

## How to run a good interview (coach the founder)

- Crime scene, not pitch — don't lead with the idea; let them say what's hot.
- Past behavior over future intent — "tell me about the last time…" beats "would you…".
- Get to an artifact — push gently toward something concrete.
- Breach, then go quiet — after "would it be OK if you never solved this?", the silence is the data.
- Solution talk under 5% of airtime.

## Synthesis prompts (for Capture and Review)

These mirror the ProFounders DPI Field Guide. After each interview: courtesy-bias filter; verbs-not-nouns (90-day actions); indifference test; painkiller-vs-vitamin; non-indifference score; disconfirming-evidence ledger; next-iteration questions. Weekly: recurring patterns of stuckness (top 5); severity × immediacy 2×2; cost-of-doing-nothing per persona; buying-mechanics roll-up; a forced "5 data points that contradict the thesis" pass; velocity & coverage; the single consolidated core insight + gaps for next cycle.

## The bar for "authentic demand"

Declare it only when: **≥3 kill-criteria Derisked (including the indifference one and the will-they-pay one), 0 Triggered, non-indifference ≥4 recurring across multiple people, and the demand evidence is behavioral, not verbal.** Until then, the honest answer is "not proven yet — here's the weakest spot."
