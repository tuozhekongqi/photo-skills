# HISTORICAL AUDIT ONLY — NOT RUNTIME GUIDANCE

> Superseded by `ROUTING.md` and R8 routing rules. Any older A-only / optional-module wording below is historical context only.

# R6 Audit — 系统性错误已修正

本轮不是增加更多风格，而是清理会导致“反馈过拟合 / 无脑拼接 / P过头 / 新规则抢权重”的旧逻辑。

## 已修正
1. **固定 A/B 倾向**：删除任何 B≈60% / A≈40% 或其他配额。
2. **新近反馈自动升权**：禁止。新规则只扩充工具箱，默认低权重、条件式使用。
3. **单次评价全局化**：反馈默认作用于最小范围；单张失败不会封禁整个 family/module。
4. **只记错误、不记成功**：明确正向成片同样是锚点，但不冻结成模板。
5. **A 默认“必须修”**：改为先问“这张真的需要修吗？”；near-original / no-op 合法。
6. **A 电影感默认过强**：改为最小必要干预；强电影感仅在原片已有条件且当前意图支持时使用。
7. **强图自动 A-only**：旧分支已废除。当前非人像强图仍默认 A+B；通过 A/B near-no-op 保持接近原片，而不是退出 B。
8. **B = 拼接**：删除。B 可以是一张照片的单页 editorial；A+B 也不要求多图。
9. **HYBRID 默认偏置**：删除。强/满意原片默认 PRESERVE；HYBRID 条件使用；DISTILL 为明确强风格化/实验才启用。
10. **数字候选评分 / 置信阈值**：完全从运行路由移除，不再 0–100 打分、不设候选分差门槛。
11. **重型逐张候选池 / decision ledger**：移出普通批次主流程；仅失败调试时可做极简 trace。
12. **固定 9 张系列节奏**：删除。
13. **强制风格多样性**：删除。多样性只能在两个方案对当前照片同样合适时做轻微 tie-break。
14. **批次强制 multi-image / experimental**：删除。
15. **拼接作为省事捷径**：禁止。只允许 2–4 张同主体/同事件互补图，必须有 hero，不能挡主体。
16. **Prompt 对 collage 的自相矛盾**：修正为“禁止无理由 collage；有明确理由的同主体 collage 可用”。
17. **水墨/水彩整幅重画风险**：默认改为 photo-led 局部/边缘/过渡；整幅绘画化必须明确请求或强参考支持。
18. **胶片颗粒默认化**：删除。grain / cast / analog finish 都是可选项，不能自动添加。
19. **Filmstrip / Contact Sheet**：当前项目继续停用；九宫格/网格照片墙为末尾硬失败。
20. **九宫格规则过度抢权重**：明确只在最后 QC 执行，不参与前面的 A/B/风格判断。
21. **古建 A-preferred 偏置**：旧分支已废除；非人像古建默认 A+B，是否出现明显 B 设计只由当前照片实际增益决定。
22. **Series Planner 强制换布局**：删除；同一处理若适合多张可以重复。
23. **旧 numeric style-affinity / stress-test / sample scoring ledger**：从 runtime 删除，避免旧逻辑重新污染。
24. **旧 Split Policy 声称 runtime 核心 byte-for-byte 未改**：已纠正。只有顶层 golden backup 是不可变原版；当前 B runtime 是演进版。
25. **Golden backup 在合包中缺失/说明不一致**：恢复到顶层 `golden-backup/`，仅用于回退，不参与运行权重。
26. **研究资料来源描述可能成为“新资料权威”**：runtime research notes 只保留可迁移原则，不再依赖具体仓库名作为权威。
27. **内部文档过期引用 / 路径错误**：清理已删除 scoring 文件引用、修正 feedback/reference 路径。
28. **A feedback ledger 仍写“默认要明显电影感”**：改为原片满意优先、轻修优先；“过头”只退具体维度。
29. **B feedback ledger 仍可能把“多样化”变成强制换风格**：改为重复允许，只有真正适配时变化。

## 最终稳定基线
**原片第一；最小必要改动；设计只在有真实增益时出现；反馈只改最小作用域；新知识不因“新”而加权。**
