# Retry & Recovery Policy v5.3

## Contract-preserving recovery

Lock the route and design_strength from `delivery-contract.md` across all retries. Under-designed execution is R04_UNDER_DESIGNED: repair the actual page structure and second functional relation, not just color/type. Lower photographic T, choose PRESERVE, remove secondary effects or reduce copy when source fidelity suffers, while retaining strong page design. Simplifying layout means removing noise while keeping its required relationships.

Default bounded recovery: initial attempt plus at most two repair attempts per source for one run, unless the user explicitly requests further work. Reassess after two failed executions in one family within that same total ceiling. On exhaustion or unavailable tools/capacity, report blocked/unfinished B and keep stage flags truthful; do not deliver base-only or light B as a strong-B success.

A failed output should not trigger random prompt rewriting. Diagnose first.

---

## 1. Failure classes

### Execution failure
The selected style was good, but generation executed it badly.

Examples:
- typography too large;
- paper tear too generic;
- palette drift;
- landmark slightly altered;
- too many doodles.

Action:
- keep primary family;
- keep source fixed;
- tighten the relevant prompt block;
- optionally remove layout clutter while preserving the required composition and functional relations.

### Decision failure
The style itself was a poor choice.

Examples:
- watercolor weakened a strong architectural image;
- Second World concept feels forced;
- ticket treatment trivializes a documentary moment.

Action:
- rerun candidate scoring;
- choose runner-up or downgrade Transformability;
- change family materially.

### Source-selection failure
A weaker or redundant source was selected.

Action:
- switch to `reserved-alt` from the same angle/story group;
- do not style both unless needed.

---

## 2. Retry ceiling

After two failed executions in the same family for the same source:
- stop micro-tuning;
- reassess whether the family is wrong or transformability is too high.

Do not endlessly rephrase an unstable concept.

---

## 3. Conservative recovery

When repeated attempts keep damaging the source:
- downgrade one photographic T level without lowering design_strength;
- switch to PRESERVE where possible;
- use E / G / H / J / Clean Editorial;
- remove secondary influence;
- reduce copy.

---

## 4. User rejection parsing

When a user says `I don't like this style`, distinguish:
- family dislike;
- layout dislike;
- text dislike;
- excessive transformation;
- wrong palette;
- generic / AI-looking result.

Record the narrowest justified rejection, unless the user clearly bans the whole family.
