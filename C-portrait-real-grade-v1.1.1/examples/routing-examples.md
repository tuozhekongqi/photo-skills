# C routing examples — entry context matters

| Source / request | Entry context | Main subject | Route | Base | Design |
|---|---|---|---|---|---|
| close selfie, process with ABC | combined-user | person | C+B | normal C | strong B |
| full-body night/back-view portrait, smooth hair and slim naturally | combined-user | person | C+B | normal C + authorized local extras | strong B |
| portrait + magazine page | combined-user | person | C+B | normal C | strong B |
| landscape with tiny walkers, process with ABC | combined-user | scene | A+B | normal A | strong B |
| architecture + editorial layout | combined-user | scene | A+B | normal A | strong B |
| scene, explicitly design only/no grading | combined-user | scene | B | none | strong B |
| portrait, explicitly only natural retouch/no design | combined-user | person | C | normal C | off |
| portrait, explicitly light B | combined-user | person | C+B | normal C | light B |
| portrait, only critique/diagnose | combined-user | person | analysis-only | no generation | no generation |
| close selfie, standalone C | standalone-c | person | C | normal C | off unless requested |

Hair/body extras do not replace the C workflow or suppress B. Main-subject classification selects A versus C, not whether the final design layer exists.
