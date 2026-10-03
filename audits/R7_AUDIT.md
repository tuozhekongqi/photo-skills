# HISTORICAL AUDIT ONLY — NOT RUNTIME GUIDANCE

> Superseded by `ROUTING.md` and `R8_AUDIT.md`.

# R7 audit — default routing correction

## User-requested routing now encoded
- Clear portrait/person subject -> **A + B + C by default**.
- No portrait/person subject -> **A + B by default**.
- Explicit user instruction overrides default routing.

## Consistency fixes
1. Added a real C module (`C-portrait-real-grade-v1.0`) so the package no longer references an undefined portrait layer.
2. Updated top-level `ROUTING.md` and `README.md` from A+B-only wording to A+B+C combined routing.
3. Updated A to clarify that it can run together with B and delegates person-specific retouch to C.
4. Updated B to clarify that default activation can be extremely restrained and never implies collage.
5. Updated feedback policy vocabulary so portrait feedback can be scoped to C without disabling A or B.
6. Preserved anti-overfitting rule: default module activation controls coverage, not strength.
7. Preserved the V5.3 golden backup unchanged.
