# Changelog

## 5.4.0 — 2026-10-05 user package

Add a locked normal-base/strong-B delivery contract. Separate photographic T from page strength; retain source/person protection and existing grade priority. Update routing, prompts, recovery, completion gates and examples. Normalize SKILL.md discovery metadata. Earlier entries below describe historical versions, not the current default contract.

## v5.3.4

- Added Explicit-B activation floor for `B`, `A+B`, and `C+B` routes.
- Prevents B from collapsing into plain photo + border + caption.
- Explicit B now requires one major design relationship plus one supporting relationship.
- Does not force collage: dense/strong photos may use restrained editorial structure.
- New rule is conditional and does not receive elevated weight merely because it is new.


## v5.0

- Added a formal Style Decision Engine.
- Added Visual Profile fields that describe how a photo behaves visually, not only what it depicts.
- Added T0-T3 Transformability levels.
- Added weighted Candidate Scoring, penalties, and confidence thresholds.
- Added primary vs secondary style logic and tie-break rules.
- Added batch rebalancing for local-fit + global-rhythm optimization.
- Added style fit / contraindication matrix for all 12 families.
- Added 18 decision counterexamples to prevent shallow subject-to-style routing.
- Added layout signatures and layout repetition control.
- Added evaluation protocol and redo diagnosis codes.
- Extended batch ledger to store strongest behavior, candidate scores, confidence, layout, and batch role.

## v5.1

- Added 12 Visual Behavior Archetypes as an intermediate layer between image analysis and style choice.
- Added a numeric Style Affinity Matrix to make candidate generation less subjective.
- Added correction rules for high color value, low Second World potential, low negative space, low detail value, and low text tolerance.
- Added a Great Wall stress test showing deduplication + varied style routing within one destination.
- Added a sample decision ledger.
- Fixed main SKILL section numbering after v5 decision-engine insertion.

## v5.2

- Added Source Selection Engine: near-duplicate and visual-story redundancy are now separate culling layers.
- Added selection scoring for quality, uniqueness, coverage, style opportunity, and narrative value.
- Added explicit `reserved-alt` and `skipped-visual-redundancy` states.
- Added Preference Adaptation Layer with bounded bonuses for likes and hard rejection memory.
- Added Series Planner for sequence roles, visual intensity, color rhythm, orientation rhythm, and text rhythm.
- Decision pipeline now includes output intent / preference before scoring and series placement after scoring.

## v5.3

- Added Copy Engine with no-text, handwritten, editorial, archival, and ticket copy modes.
- Added Prompt Compiler with explicit source lock, visual behavior, transformability, style, layout, copy, and negative blocks.
- Added Retry & Recovery Policy separating execution failure, decision failure, and source-selection failure.
- Added retry ceiling and conservative fallback behavior.
- Added a complete decision-to-compiled-prompt example.


## v5.3.3

- Added explicit evaluation / feedback mode:点评 does not auto-trigger generation.
- Added feedback learning loop and running feedback ledger.
- Added anti-overfitting rule: accepted layouts are principles, not universal templates.
- Added source-fidelity check for design-driven weather / light repainting.
- Added current user preference notes for restrained photo-first editorial treatment.


## 5.3.2 — lightweight feedback consolidation
- Removed runtime research-image archive after extracting useful principles into text.
- Removed nested golden backup from runtime; preserved it as a separate immutable ZIP.
- Standardized image memory to a positive-only library; “还行/一般” ratings now remain text-only.
- Added approved `Red Wall, Soft Sky` and `Beijing / City Notes` references.
- Added explicit anti-template guidance from recent user feedback.
