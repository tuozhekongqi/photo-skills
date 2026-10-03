# Changelog — Photo Skills（A+B+C 合包）

> 本仓库以 **R8 合包** 为主结构。各模块规则原文未做简化、重写或合并；本文件记录版本历史，详细修正内容见 `audits/`。

## R8 — 2026-10-03 · 路由不变量加固（当前稳定版）

**默认路由（固定）**
- 无人像 / 人物主体：**A + B**
- 存在明确人像 / 人物主体：**A + B + C**
- 只有用户明确指定模块组合或关闭模块，才改变组合。

**核心不变量**
- 模块启用与处理强度分离：「只轻修 / 只调色 / 只调光影 / 保持真实 / 原片已经很好」等要求只降低对应模块强度，不移除默认模块；各模块可 `near-no-op`。

**一致性修复（10 项，详见 `audits/R8_AUDIT.md`）**
1. `ROUTING.md`：显式模块覆盖与强度类请求分离，新增路由不变量；
2. B `SPLIT_POLICY.md`：移除「颜色 / 光线 / 写实类请求属于 A 单独处理」的旧规则；
3. B `batch-diversity.md`：移除强照片的 `A-only` 路径；
4. B `source-selection-engine.md`：非人像照片不再允许在 A / A+B / 原片之间自由选择，默认保持 A+B；
5. A 古建规则：B 可以 near-no-op，但不退出默认非人像路由；
6. B 古建规则：A → B 为职责顺序；B 的表达是否可见是条件式的，B 的激活不是；
7. C workflow：明确人像下 C 保持激活，可作为身份 / 真实感护栏以 near-no-op 存在；
8. 反馈策略：可修正人像主体判定、显式模块指令、模块强度或 B family 选择；A/B/C 组合不再视为可自由选择；
9. R6 / R7 审计标记为历史参考，防止旧路由措辞回流运行时；
10. golden V5.3 备份保持字节级不变。

**模块版本**：A `v1.4`（新增 `heritage-architecture-look.md`）· B `v5.3.4`（新增 `heritage-photo-foundation.md`、`batch-diversity.md`）· C `v1.0`。

## R7 — 2026-09 · 默认路由修正

- 用户要求的默认路由写入规则：有人像 A+B+C / 无人像 A+B；显式指令优先。
- 新增真实 C 模块（`C-portrait-real-grade-v1.0`）；顶层 `ROUTING.md` / `README.md` 由 A+B 措辞更新为合包路由；A 明确人物处理委托给 C；反馈词汇支持将人像反馈限定到 C。详见 `audits/R7_AUDIT.md`。

## R6 — 2026-09 · 系统性修正（反过拟合清理）

- 清理会导致「反馈过拟合 / 无脑拼接 / P 过头 / 新规则抢权重」的旧逻辑：删除固定 A/B 配额、新近反馈自动升权、单次评价全局化、数字评分、C-only 自动路径、B=拼接、强制多样性、九宫格抢权重等 29 项。详见 `audits/R6_AUDIT.md`。

## B v5.3 — 2026-09-27 · 原始黄金基线

- 原始独立版 Photo Zine Social skill；保存于 `golden-backup/B-photo-zine-v5.3-golden-backup.zip`，**字节级保留、不参与运行、不允许覆盖**（SHA-256 `c3498fd0113953f69f25715ac865f97ae7d5a4479d0e525f9fe7eec1f4b30624`）。

## 早期模块历史（摘录，非运行规则）

- **B v5.0 → v5.3.3**：Style Decision Engine（v5.0）→ Visual Behavior Archetypes / 亲和矩阵（v5.1）→ Source Selection Engine / Preference Adaptation / Series Planner（v5.2）→ Copy Engine / Prompt Compiler / Retry Policy（v5.3）→ 反馈模式与反过拟合原则、轻量化整合（v5.3.2–v5.3.3）。
- **C v1.0（2026-09-30）**：独立人像优先 C 路由加入合包，负责身份、皮肤、自然体态保护。
