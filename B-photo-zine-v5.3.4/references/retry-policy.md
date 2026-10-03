# Retry & Recovery Policy v5.3.4

A failed output should not trigger random prompt rewriting or a full style-system reset. Diagnose the smallest cause first.

## 1. Failure classes

### Execution failure
The direction is sound, but rendering executed it badly.

Examples:
- typography too large;
- paper edge too generic;
- palette drift;
- landmark altered;
- too many doodles;
- source image accidentally repainted.

Action:
- keep the successful idea;
- keep the correct source fixed;
- correct only the failing block;
- simplify rather than add complexity.

### Intensity failure
The family may be correct, but the treatment is too strong or too weak.

Examples:
- A/A-lite pushed color or relighting too far;
- B typography/material dominates;
- watercolor/print effect covers too much of the photo.

Action:
- adjust the failing intensity dimension first;
- do not switch family unless the direction itself is wrong.

### Decision failure
The treatment family itself is a poor fit for this source.

Examples:
- watercolor weakens architectural precision;
- Second World concept feels forced;
- ticket treatment trivializes a documentary moment.

Action:
- return to the qualitative decision engine;
- compare the nearest plausible alternative against PRESERVE/do-less;
- choose the simpler source-led option.

### Source-binding failure
The wrong source was used, a source was substituted, or multiple sources were merged unintentionally.

Action:
- discard the output;
- rebind the intended source;
- do not continue the batch until source identity is reliable.

## 2. Retry ceiling
After two failed executions of the same idea on the same source:
- stop micro-tuning;
- reassess whether the family/intensity/source binding is wrong;
- prefer a simpler PRESERVE/A-lite/B-light recovery.

## 3. Conservative recovery
When repeated attempts keep damaging the source:
- reduce transformation level;
- remove secondary influence;
- reduce copy/material treatment;
- return to the closest approved baseline;
- preserve more of the original photograph.

## 4. User rejection parsing
When a user dislikes a result, distinguish:
- family mismatch;
- layout mismatch;
- text mismatch;
- excessive transformation;
- wrong palette/light;
- source repaint/AI look;
- source-binding/merge error.

Record the narrowest justified lesson. Do not globalize it unless the user explicitly establishes a durable rule.
