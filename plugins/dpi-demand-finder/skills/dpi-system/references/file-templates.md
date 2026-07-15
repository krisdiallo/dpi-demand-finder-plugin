# File templates — what to create on the user's device

Create these inside a folder named for the idea (e.g. `dpi-<idea-name>/`). That folder goes **inside the project's linked folder if one is connected, otherwise in a new folder under the user's Documents** — see "Where the system lives" in `SKILL.md`. Never leave the system only in a temporary scratchpad. **Fill every `{{placeholder}}` from the conversation** — never write a file that still contains a placeholder or generic filler. Use the numeric prefixes so the files sort in reading order.

Folder layout:

```
dpi-<idea-name>/
├── 00_START_HERE.md
├── 01_thesis.md
├── 02_what-could-kill-it.md
├── 03_who-to-talk-to.md
├── 04_questions.md
├── 05_scoreboard.md
├── 06_interview-template.md
└── interviews/
```

---

## 00_START_HERE.md

```markdown
# {{Idea name}} — DPI System

Finding out whether this problem is real and burning, by honestly trying to prove it isn't. This is pre-build: we're testing the problem, not a product — and DPIs never discuss a solution.

## What you're testing
{{one-line plain thesis — a claim about a problem/persona, not a product}}

## The files
- **01_thesis** — the claim we're trying to disprove, and how it changes.
- **02_what-could-kill-it** — the ways this could be a non-starter. The heart of the system.
- **03_who-to-talk-to** — who feels the problem vs. who proves demand.
- **04_questions** — what to ask. Gets sharper after every interview.
- **05_scoreboard** — are we finding real demand yet?
- **06_interview-template** — copy this for each conversation; logged ones live in `interviews/`.

## The loop
Pick the weakest "what could kill it" → talk to the right person → log it → update the scoreboard → get 3 sharper questions for next time.

## The rule that keeps you honest
Believe it only when the idea survives honest attempts to kill it. One person saying "I'd be fine never solving this" matters more than three being polite. What people *did* counts; what they *might* do doesn't.

## Next step
{{specific: who to talk to first, and come back and say "log a DPI" after}}
```

---

## 01_thesis.md

```markdown
# Thesis — what we're trying to disprove

## Current (v1)
> {{ONE short, plain, testable sentence — ~8–16 words, fits on the head of a pin. e.g. "People are willing to get into a stranger's personal car."}}

**This is true only if:** {{what would have to hold}}
**We're trying to disprove that:** {{the parts most likely to be false}}
**Confidence right now:** {{Low / Low–Moderate / …}} — {{one line why}}

## The load-bearing part (only if the belief has real depth)
- {{at most one line naming the single sub-claim the whole thesis hangs on — keep the headline above short}}

## Evolution log
| Ver | Date | Thesis | What moved it |
|---|---|---|---|
| v1 | {{date}} | {{thesis}} | Starting point |

> Never delete an old version. Killing or revising a thesis is the system working, not failing.
```

---

## 02_what-could-kill-it.md

```markdown
# What Could Kill It

Each item is a specific way this idea could be wrong. Interviews move each from Open → Derisked (survived) or Triggered (the killer is real). One Triggered item = stop and rethink the thesis.

Status: Open · Probing · Derisked · Triggered.

### KC-1 — {{plain name}}
**The killer:** {{specific to this idea}}
**Disproved if:** {{what we'd hear}}   **Survives if:** {{what we'd hear}}
**Status:** Open   **Evidence:** —   **Interviews:** —

{{repeat KC-2 … KC-5/6/7}}

## Roll-up (update each week)
| # | Status | Evidence strength | Interviews |
|---|---|---|---|
| KC-1 | Open | — | — |

**Verdict:** {{e.g. "0 derisked, all Open — far too early. Attack KC-x and KC-y first."}}
```

---

## 03_who-to-talk-to.md

```markdown
# Who To Talk To

Match the person to what you're trying to learn. People who *feel* the problem describe it; only the person who *pays* proves demand.

## Feels the problem (1st order)
{{who}} — can tell you {{what}}; can't prove demand.

## Owns the budget / decides to pay (2nd order — primary)
{{who}} — proves the indifference and will-they-pay questions. Weight this layer highest.

## Sees many cases (3rd order)
{{who: advisors, recruiters, industry insiders}} — fastest way to learn how common and how rare.

## Which person for which killer
| What could kill it | Best person to ask |
|---|---|
| {{KC-1}} | {{layer}} |

## Roster (grow this)
| Person | Layer | Context | Status | Interview |
|---|---|---|---|---|
```

---

## 04_questions.md

```markdown
# Questions

Pull the questions for whichever "what could kill it" item is weakest right now. Not a script — a menu.

## How to ask
Don't pitch. Ask about the last time it happened, not what they'd hypothetically do. Push toward something concrete. After "would it be OK to never solve this?" — go quiet.

## Opening (stay broad)
- What's been eating most of your time lately?
- Walk me through the last couple of weeks — where did things get stuck?

{{For each KC, a short block of disconfirmation-first questions, tailored from references/question-bank.md}}

## The one question, if you only get one
{{tailored}}

## Never ask (these manufacture false yeses)
- "Would you pay for something that…" (hypothetical + leading)
- "Don't you think X is hard?" (leads the witness)
- "We're building X — would that help?" (that's a pitch)

## Sharpening log (add after every interview)
| After interview | Weakest killer | New questions added | Retired |
|---|---|---|---|
```

---

## 05_scoreboard.md

```markdown
# Scoreboard

One row per interview. As rows pile up, the tallies show whether real demand is emerging or you're collecting polite anecdotes.

| # | Date | Person (layer) | Pain raised (unprompted?) | Non-indiff /5 | Strongest evidence | Killers moved | Disconfirming? |
|---|---|---|---|---|---|---|---|

## Tallies (update weekly)
- Interviews total: 0   | by layer: —
- Killers: Derisked 0 · Triggered 0 · Probing 0 · Open {{n}}
- Behavioral (artifact-backed) evidence count: 0
- Unprompted pain mentions: 0
- Strong disconfirmations: 0
- Recurring patterns (need ≥3 to count): none yet

**Verdict:** {{plain-language read}}

## Signal phrases (tally unprompted repeats — repetition is the real proof)
| Phrase to listen for | Count | Interviews |
|---|---|---|
| {{tailored to this thesis}} | 0 | |

## How to read this
Rising behavioral evidence + repeated signal phrases + killers moving to Derisked = demand emerging. Lots of interviews but evidence stays verbal and killers stay Open = you're being flattered; ask harder.
```

---

## 06_interview-template.md

Copy the per-DPI capture template: metadata + persona layer + **source (transcript preferred / recollection — recollection lowers evidence confidence)** + context type (flag candidate/sales contexts as flattery-biased); what they raised unprompted; behaviors in last 90 days (table with strength); disconfirming evidence (table with strength); non-indifference score + evidence line; cost-of-doing-nothing; **money signals around the problem** (what they already spend in time/money/effort, who would own a budget — captured *without ever pitching a solution*); verbatim quotes tied to killers; courtesy talk set aside; killer-movement table; quality self-score (neutrality / behavioral depth / disconfirmation attempts / artifact capture / **solution never mentioned?** / transcript vs recollection); next 3 sharper questions; who they referred you to. Mirror the section order in `references/methodology.md`.
