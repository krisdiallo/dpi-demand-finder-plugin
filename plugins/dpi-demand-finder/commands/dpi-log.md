---
description: Log a customer interview you just did and update your DPI system
---

Run the **Capture flow** from the `dpi-system` skill to log one DPI (Documented Primary Interaction) and update the user's system.

Before doing anything, read:
- `${CLAUDE_PLUGIN_ROOT}/skills/dpi-system/references/methodology.md`
- `${CLAUDE_PLUGIN_ROOT}/skills/dpi-system/references/file-templates.md`

First, locate the user's DPI folder — a `dpi-<idea-name>/` containing `00_START_HERE.md` and `05_scoreboard.md`. Look in the project's linked folder first, then under the user's Documents (that's where setup puts it when no folder is linked). If you can't find one, offer to run setup first.

Then: ask who they spoke to and which persona layer. **Ask for the transcript first** — a verbatim transcript or recording is the highest-value input and the default expectation; prompt them to paste it. If they don't have one, a braindump is an acceptable fallback but is explicitly lower-value: mark the DPI's source as "recollection" and treat its conclusions more cautiously. Strip politeness, pull out what the person actually *did* (last ~90 days), hunt for disconfirming evidence, score non-indifference 0–5. Remember this is solution-independent — capture money signals only as existing spend on the problem, never a reaction to a pitched solution. Write a filled-in interview file into `interviews/`. Update the "what could kill it" statuses **only** when the decision-rule thresholds are met, add a scoreboard row, update tallies and signal-phrase counts, and write 3 sharper questions into the question bank's sharpening log.

End with a 2–3 sentence plain-language readout: where demand stands, the biggest untested hole, and who to talk to next. Do not dump jargon.
