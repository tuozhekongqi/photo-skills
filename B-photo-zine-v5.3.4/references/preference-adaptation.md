# Preference Adaptation Layer v5.3

Style decisions respond to explicit user taste without becoming monotonous, reactive, or overfit. Use the shared `../../FEEDBACK_ABSORPTION_POLICY.md`.

## 1. Preference scope

Every preference entry must include one scope:
- `execution_only`;
- `source_class`;
- `batch_level`;
- `system_rule`.

Default to the narrowest plausible scope. Newness is not a weight bonus.

### Global hard reject
Use only when the user clearly rejects the **family/treatment itself** as a durable rule, or when repeated feedback across different contexts establishes that scope.

Effect:
- remove that family/treatment from compatible candidate pools only at the recorded scope;
- record the concrete failure reason;
- do not recreate the same rejected visual signature under a renamed recipe.

A sentence such as `this fourth one is bad`, `this collage is ugly`, or `this one is overdone` is **not automatically a global hard reject**. It is usually an execution/intensity diagnosis.

### Strong like
An explicit favorite becomes a positive anchor and receives a modest bonus when source-compatible. It is not a template contract.

### Soft like
Accepted/repeatedly chosen behavior is a small tie-break signal only.

## 2. Preference bonus

Apply preference after source-fit/fidelity judgment.
- strong like: modest bonus;
- soft like: small tie-break bonus;
- execution-specific reject: penalize that failure signature, not the parent family;
- global hard reject: remove only within its actual scope.

A preference cannot rescue a poor source fit.

## 3. No forced diversity or favorite caps

Do not create arbitrary batch quotas from preference learning. A favorite treatment may recur when multiple photographs genuinely support it, and a different style should not be forced merely to create variety. Repetition risk is a secondary check, not a quota.

## 4. Rejection memory

Record:
- source/context;
- family/module;
- layout signature;
- transformation/intensity level;
- concrete rejection reason;
- scope;
- correction.

Keep family choice and treatment intensity separate. One failed B collage must not suppress B globally; one over-graded A image must not force all A work to become timid.

## 5. Preference / fit arbitration

Tie-break order:
1. current explicit request;
2. source preservation / identity;
3. source-specific visual fit;
4. nearest compatible approved anchor;
5. scoped negative lessons;
6. user preference bonus;
7. batch repetition check;
8. simplicity.

The photograph remains the primary authority. New preferences add options or bounded corrections; they do not displace the stable baseline simply because they are recent.

## 6. Evaluation mode

During点评/评价, learn first and do not auto-generate. Promote only the smallest useful lesson. If a new lesson conflicts with earlier explicit positive evidence, roll back toward the positive baseline and apply a bounded correction rather than overwriting the earlier preference.
