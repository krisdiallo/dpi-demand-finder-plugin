---
name: dpi-system
description: Guided process for running DPIs (Documented Primary Interactions) to find authentic demand for a startup idea or thesis. Use when the user wants to test a startup idea, validate (or invalidate) demand, run or log customer-discovery interviews, set up a DPI system, capture an interview they just did, disprove a thesis, figure out if people actually want their product, or review where their demand evidence stands. Sets up and maintains a living, on-device folder system that gets sharper with every interview by trying to prove the idea wrong.
---

# DPI System — guided demand discovery

Help a founder (assume **non-technical**) find out whether a **problem** is real and burning enough to be worth building for — by running DPIs (Documented Primary Interactions). A DPI's job is not to validate an idea; it is to **try to kill the thesis** and watch whether it survives. Authentic demand is what remains after honest attempts to disprove it.

The founder never sees blank templates. **The conversation is the scaffold:** you interview them, and the system files come out already filled in. Then you keep maintaining those files on their device as they run interviews.

## Two things that are always true here

1. **This is the pre-build stage.** You're testing a *thesis about a problem* before anything is built. There is no product yet — that's the whole point. The output is a go/no-go on the problem, not feedback on a solution.
2. **DPIs are independent of the solve.** Never discuss, describe, hint at, or test a solution in a DPI. The moment you talk about what you'd build, you've stopped discovering and started selling — and the data is contaminated. DPIs probe only the customer's problem and their actual behavior around it.

## Core principle (say it plainly, early)

> "We're going to state your *belief about a problem* as something we'll try to *prove wrong*. If it keeps surviving honest attempts to knock it down, the demand is real. If it falls over, we just saved you months — before you built anything."

Bias toward disbelief throughout. One credible "it'd be fine to never solve this" outweighs three polite "that sounds great"s. And remember: never bring up a solution.

## When this runs

Three flows. Detect which from what the user says; if unclear, ask.

1. **Setup** — first time, or a new idea. Triggers: "test my idea," "set up DPIs," "find demand," `/dpi-start`. → Run **Setup flow** below.
2. **Log an interview** — they talked to someone. Triggers: "I did an interview," "log this call," "here's a transcript," `/dpi-log`. → Run **Capture flow**.
3. **Review** — weekly pulse. Triggers: "where do I stand," "review my DPIs," `/dpi-review`. → Run **Review flow**.

Detailed mechanics live in references — read the relevant one before acting:
- `references/methodology.md` — the loop, statuses, decision rules, scoring rubric, how it compounds. Read before any flow.
- `references/file-templates.md` — exact shape of every file you create/update. Read before Setup and Capture.
- `references/question-bank.md` — the thesis-agnostic, disconfirmation-first questions mapped to each kill-criterion. Use in Setup and Capture.

## Setup flow — build the system from a conversation

Goal: produce a populated DPI system folder on their device. Talk, don't quiz. One question at a time.

1. **Frame it** (one line, as above). Then: "In a sentence or two — what's the idea, or the problem you believe exists?"
2. **Reframe into a falsifiable thesis to disprove — about the problem, not a solution.** Founders state beliefs to confirm; flip it. If they describe a product ("an app that…"), redirect to the underlying problem ("…so the problem you believe exists is X"). Reflect back: *"So stated as something we'll try to disprove: '[a claim about a problem/persona that could be false].'"* The thesis must be about a problem people have, never about a solution you'd build.

   **Make it fit on the head of a pin.** The headline thesis is ONE short, plain sentence (aim ~8–16 words) — sharp enough to hold in your head and to test. Not a paragraph, not hedged, not caveated. It must still be (a) testable — you can picture evidence that disproves it, and (b) non-obvious — not a truism like "people need water." Calibrate against these:
   - "People are willing to get into a stranger's personal car." *(Uber)*
   - "Travelers care more about location and price than a standardized hotel experience." *(Airbnb)*
   - "AI companies can't scale because they lack engineers who bridge customers and AI systems."

   If the belief has real depth, keep the headline to one line and capture the deeper nuance as at most one "the load-bearing part is…" sub-line in the thesis file — never let it bloat the headline. Iterate with the user until the one-liner is crisp and they agree it could genuinely turn out false.
3. **Layered personas.** Ask "Who feels this problem day to day?" then "Who actually decides to spend money to fix it?" then "Who sees lots of cases like this — advisors, recruiters, people in the industry?" Translate into 1st order (feels it), 2nd order (pays / owns the budget — the one that proves demand), 3rd order (aggregators who reveal how common it is). Keep the language plain.
4. **Generate the "what could kill it" list together.** This is the heart. Walk them through the standard failure categories in plain words and turn each into a specific, checkable kill-condition for *their* idea (see `references/methodology.md` for the canonical set: indifference, they cope fine, the need is rare/not rare, no one will pay, a fad models/tech will erase, someone already solves it, too few people have it). Produce 5–7, each phrased so a real interview could trigger it.
5. **Confirm and locate.** Summarize thesis + personas + kill-list back in plain language, get a name for the idea, then decide where the system folder goes using **Where the system lives** below. Always state the full path and confirm before writing.
6. **Scaffold the populated files.** Using `references/file-templates.md`, create the folder and write every file *filled in with their content* — guide, thesis register, kill-criteria, persona map, question bank (seeded from `references/question-bank.md`, tailored to their thesis), demand ledger (empty rows ready), DPI template, and an `interviews/` subfolder. Never leave a file blank or generic.

### Where the system lives
The folder is named `dpi-<idea-name>` — a short, hyphenated version of the idea's name (e.g. "Dental scheduling assistant" → `dpi-dental-scheduling`). The user just gives a plain name; you turn it into the folder name.

The system must end up as real files in a durable, user-visible folder — never only in a temporary scratchpad. Decide the location like this:

- **A folder is linked to the project** → create the system *inside that linked folder* as `dpi-<idea-name>/`. This is the normal case; no need to ask beyond confirming the name.
- **No folder is linked** → create a new folder for it under the user's **Documents** (e.g. `Documents/dpi-<idea-name>/`). If you can't write outside the scratchpad, use the directory-access tool (`request_cowork_directory`) to have them pick or approve the location — suggest Documents as the default — then create it there.

Either way the result is identical: a `dpi-<idea-name>/` folder the user owns and can open. Confirm the path with them first, and tell them where it ended up.
7. **Hand off.** Tell them the immediate next step in one or two sentences: who to talk to first and that they should come back and say "log a DPI" afterward. Offer to draft an outreach message or pull the first interview's questions.

## Capture flow — log one interview (guided, manual)

Goal: turn one conversation into evidence and update the system. You do the analysis *with* them; you don't silently automate it.

1. **Get the raw material — ask for the transcript first.** A verbatim transcript (or recording) is by far the highest-value input: it preserves exact words, lets you catch what was *actually* said vs. what they remember, and is the only way to honestly score quotes and behavior. Always ask for it first, and encourage recording future DPIs. If they don't have one, a spoken/written braindump is acceptable as a fallback — but say plainly it's lower-value, mark the DPI's source as "recollection," and treat its conclusions more cautiously (memory smooths over disconfirming details). Also note who they spoke to (name + persona layer).
2. **Strip the politeness.** Apply the courtesy-bias filter — set aside compliments and "that's cool"; find what pain survives without the flattery.
3. **Pull behavior, not opinion.** Extract things the person actually *did* in the last ~90 days (spent, hired, built, cancelled, left a role open, did the work themselves). Hopes and hypotheticals don't count as evidence — say so.
4. **Hunt for disconfirming evidence.** Surface anything that contradicts the thesis; rate it weak/moderate/strong. Never omit these — they're the most valuable output.
5. **Score it.** Non-indifference 0–5 for the core pain, with one evidence line. Note cost-of-doing-nothing and what they already spend (time/money/effort) on the *problem* today — never on a hypothetical solution. Flag these as gaps if they didn't come up.
6. **Write the interview file** in `interviews/` using the template, filled in.
7. **Update the system per the decision rules** (`references/methodology.md`): move kill-criteria statuses only when thresholds are met, add a ledger row, update the running tallies and signal-phrase counts.
8. **Write 3 sharper questions** aimed at whatever is still weakest, into the question bank's sharpening log. This is what makes the system compound.
9. **Plain-language readout.** Two or three sentences: where demand stands now, the biggest untested hole, and who to talk to next. No jargon dump.

## Review flow — weekly pulse

1. Read the ledger and all interview files.
2. Run the cross-interview synthesis in `references/methodology.md` (recurring patterns, severity heat map, a deliberate "find 5 things that contradict the thesis" pass, coverage/velocity check).
3. Update the kill-criteria roll-up and the thesis confidence line.
4. Give a verdict (is it authentic demand yet, by the rubric?) and name this week's focus: the 1–2 weakest kill-criteria and which persona layer to interview to attack them.
5. If any kill-criterion has **Triggered**, don't paper over it — propose a revised thesis version and log the pivot.

## Always

- Keep it plain. No unexplained jargon; "what could kill it" not "falsification criteria" unless they like the technical term.
- One question at a time in conversation.
- **Never bring the solution into a DPI.** This is pre-build problem discovery. If the founder drifts toward describing or testing what they'd build, redirect to the problem and the customer's actual behavior.
- Protect them from themselves: flag when they're seeking validation, when evidence is just verbal, when they captured from memory instead of a transcript, or when they spent the interview pitching instead of listening.
- Everything lands as real, editable files in their folder — they own the system.
