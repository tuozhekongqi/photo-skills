# User Feedback Learning Loop

This skill treats user evaluation as training signal, but it must learn without overfitting. Read the shared `../../FEEDBACK_ABSORPTION_POLICY.md` when available.

## 1. Enter evaluation mode

When the user is reviewing an output, do **not** automatically generate another image unless the user asks for a redo/continuation.

In evaluation mode:
1. identify the concrete visual decision being praised or rejected;
2. classify the feedback scope at the smallest justified level: execution-only, narrow source-class, batch-level, or durable system rule;
3. separate style-family choice from execution quality and treatment intensity;
4. preserve earlier explicit positive anchors unless the user clearly supersedes them;
5. turn the feedback into a bounded actionable correction, not a blanket rule.

## 2. Feedback weights and promotion

- **Explicit strong positive**: keep as a positive anchor when source-compatible. Record why it worked.
- **Soft positive**: small preference bonus / tie-break evidence.
- **Partial / neutral**: extract useful details into text; do not elevate the whole treatment.
- **Negative / too much / fake**: store the concrete failure signature and correction at the narrowest valid scope.
- **Global hard reject**: use only when the user explicitly rejects the family/treatment as a durable rule, or the same rejection repeats across different contexts.

Specific repeated feedback outranks one generic reaction. **Recency alone does not increase weight.** New rules do not get extra authority merely because they are new.

## 3. Positive/negative symmetry

Do not build a system that only remembers failures. Approved work is equally important evidence.

For similar future sources, prefer the nearest compatible approved anchor, then make only the changes required by the new source. A rejected output should teach a specific failure mode rather than banning an entire family/module unless the user says so.

## 4. Family vs intensity

Learn these separately:
- module/family choice;
- layout;
- transformation level;
- color/contrast;
- typography/material;
- collage behavior.

`Too much` normally means lower the relevant intensity ceiling, not disable the idea. `This collage failed` normally means the collage execution failed, not that B or collage is globally forbidden.

## 5. Mandatory self-audit after feedback

Before the next generation, ask internally:
- What did the user reward?
- What exactly was rejected?
- What is the smallest valid scope of that lesson?
- Was the problem family choice, layout, intensity, or execution drift?
- Would this new rule conflict with a previously approved anchor?
- Am I increasing a rule's weight only because it is recent?

If there is conflict, roll back toward the nearest clearly approved baseline and apply the smallest correction.

## 6. Feedback ledger

Maintain `feedback-ledger.md` as a compact running record. Each negative lesson should include a scope and failure signature; each strong positive should include the responsible decisions. The ledger is subordinate to source fidelity and the user's current explicit request.
