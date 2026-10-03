# R8 audit — routing invariant hardening

## Authoritative default route
- No clear portrait/person subject -> **A + B**.
- Clear portrait/person subject -> **A + B + C**.
- Only an explicit user module selection/disable instruction changes the combination.

## Core invariant
Module activation and intervention strength are separate decisions. “只轻修 / 只调色 / 只调光影 / 保持真实 / 原片已经很好 / visible design adds little” lower intervention strength; they do not remove a default module. Any active module may execute as near-no-op.

## Consistency fixes in R8
1. `ROUTING.md`: separated explicit module overrides from intensity/effect requests and added the routing invariant.
2. B `SPLIT_POLICY.md`: removed the old rule that simple color/light/realism requests belong to A alone.
3. B `batch-diversity.md`: removed the remaining `A-only` path for strong photographs.
4. B `source-selection-engine.md`: removed free selection among A / A+B / original for non-portrait photos; default stays A+B.
5. A heritage rules: B may be near-no-op, but does not leave the default non-portrait route.
6. B heritage rules: A -> B is now the responsibility order; visible B expression is conditional, B activation is not.
7. C workflow: C stays active for a clear portrait and may act as a near-no-op identity/realism guardrail.
8. Feedback policy: feedback may correct portrait-subject classification, explicit user overrides, module intensity, or B family choice; it no longer treats A/B/C combinations as freely selectable.
9. R6/R7 audits are marked historical-only to prevent stale routing language from regaining runtime weight.
10. Golden V5.3 backup remains byte-for-byte unchanged.
