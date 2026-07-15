---
description: Set up a new DPI demand-discovery system for a startup idea
---

Run the **Setup flow** from the `dpi-system` skill to create a new DPI (Documented Primary Interaction) demand-discovery system for the user's idea.

Before doing anything, read:
- `${CLAUDE_PLUGIN_ROOT}/skills/dpi-system/references/methodology.md`
- `${CLAUDE_PLUGIN_ROOT}/skills/dpi-system/references/file-templates.md`
- `${CLAUDE_PLUGIN_ROOT}/skills/dpi-system/references/question-bank.md`

Then talk the user through it conversationally, one question at a time, in plain language (assume non-technical). The conversation IS the scaffold — do not show blank templates. The output is a folder of files on their device, every file filled in with their own thesis, personas, and "what could kill it" list.

Key moves: reframe their belief into a claim stated to be *disproved*; map who feels the problem vs. who pays; build the "what could kill it" list together; then create the folder (ask where) and write the populated files. Finish by telling them exactly who to talk to first and to come back and say "log a DPI" afterward.

If the user already gave their idea in this message, use it and skip straight to reframing the thesis.
