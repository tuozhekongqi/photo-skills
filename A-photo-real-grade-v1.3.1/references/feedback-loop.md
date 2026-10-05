# User Feedback Learning Loop

This skill must treat user evaluation as training signal for the current visual system. Feedback is not a social closing step; it is part of the editing pipeline.

## 1. Enter evaluation mode

When the user is clearly reviewing an output (for example: “不错”, “还行”, “一般”, “AI味重”, “第一张更好”, or a detailed critique), do **not** generate another image unless the user explicitly asks for a redo.

In evaluation mode:
1. identify which concrete visual decisions the user is reacting to;
2. separate style-family preference from one-off execution quality;
3. update positive-image / text-only partial / cautionary rules;
4. preserve stronger earlier rules unless the new feedback explicitly overrides them;
5. turn the feedback into an actionable rule, not a vague adjective.

## 2. Feedback weights

Use this rough hierarchy:
- **Strong positive**: explicit “喜欢 / 很好 / 第一张不错 / 就按这个” -> promote the responsible decisions to strong positive references.
- **Soft positive**: “不错” -> positive reference; useful default when source-compatible.
- **Partial / neutral**: “还行” -> extract useful decisions into text only; do not keep the image unless the user later upgrades it to “不错/喜欢”.
- **Weak / cautionary**: “一般” -> diagnose what is missing; do not copy its full treatment as a default.
- **Hard negative**: “不行 / 好假 / AI味很重” -> store the concrete failure mode as a cautionary pattern and suppress recurrence.

Specific, repeated feedback outranks a single generic reaction. Recent feedback refines the default, but should not erase durable constraints such as source fidelity.

## 3. Learn principles, not screenshots

Do not overfit to one accepted output. Record the **reason** it worked: light hierarchy, amount of intervention, people handling, text scale, negative space, material texture, etc. A positive image is evidence, not a universal preset.

Likewise, a rejected image should teach a specific failure mode rather than banning an entire family unless the user says so.

## 4. Mandatory self-audit after feedback

Before the next generation, ask internally:
- What did the user reward?
- What did the user reject?
- Which part was caused by the chosen system, and which part by execution drift?
- What exact threshold should move next time?
- Is there any contradiction between the generated result and the written skill rules?

If the output violated an existing hard rule (for example changing weather in a realism-only workflow), treat that as an execution failure even if the image looks attractive.

## 5. Feedback ledger

Maintain `references/feedback-ledger.md` as the compact running record of accepted, text-only partial, cautionary, and hard-negative patterns. The ledger is authoritative for recent user taste but remains subordinate to hard fidelity constraints.
