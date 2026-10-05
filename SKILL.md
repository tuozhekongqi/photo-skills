---
name: photo-skills-abc-user
description: Use when the user invokes this ABC photo package to process supplied photos into finished designed images. Default to normal scene grade A plus strong design B, or normal portrait grade C plus strong B. Explicit requests for only photographic correction, light design or analysis override the corresponding default.
metadata:
  version: "1.0.0"
---

# ABC 用户版统一入口

用户给照片并要求按本包处理、修图、做成品或继续生成时，默认交付 **正常底片处理 + 重 B**。不需要等用户再说“杂志”“拼贴”“加字”才开启 B。

先确定任务是不是生成：点评、诊断、方案、只分析不自动生成；单纯附件也不代表要求修图。当前用户的明确要求始终优先。

## 执行顺序

1. 在读任何子模块配方前，读 [ROUTING.md](ROUTING.md) 与 [交付契约](B-photo-zine-v5.4.0/references/delivery-contract.md)，锁定 route、底片强度、B 是否必需和 B 强度。
2. 人物是主体：读 [C-portrait-real-grade-v1.1.1/SKILL.md](C-portrait-real-grade-v1.1.1/SKILL.md)，正常 C；场景是主体：读 [A-photo-real-grade-v1.3.1/SKILL.md](A-photo-real-grade-v1.3.1/SKILL.md)，正常 A。不串联 A+C。
3. 读 [B-photo-zine-v5.4.0/SKILL.md](B-photo-zine-v5.4.0/SKILL.md) 及其决策、配方和提示词编译文件，在同一底片上完成重 B。头发、瘦身等附加要求不替代 C，也不关闭 B。
4. 先检查来源与人物真实性，再检查 B 的页面构图和叙事/层级关系。底片完成只记 base_done；最终验收通过后才记 done。
5. 工具失败或额度不足时如实记录 blocked。只能交付底片时标明“底片已完成，B 未完成”，不得冒充全部成品。

## 强度分开判断

正常 A/C：执行既有真实后期流程，按原片需要修正光影与色彩；不为平衡重 B而加强调色。

重 B：明显参与最终构图，并形成页面结构与第二个有功能的叙事/视觉层级关系；不靠堆贴纸或固定拼贴模板。

PRESERVE 与 T0–T3 只限制照片的重绘/风格化程度。**PRESERVE + T0 + strong B** 是合法组合。照片越好，越应保护它，而非取消设计。

明确“只调色/只修人像/不要设计”时只走 A 或 C；明确“轻 B”时保留 B 并降低设计强度；明确“只做设计、不要调色”时只走 B。其他模糊的“自然一点、别乱改原图”约束照片真实性，不能自行解释成取消 B。
