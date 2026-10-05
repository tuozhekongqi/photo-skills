# R9 审计 — ABC 用户版分发包

**日期**：2026-10-05 · **发布**：tag `r9`（上一稳定版 `r8`）
**输入包**：`photo-skills-combined-ABC-user-v1.0-2026-10-05.zip`
（SHA-256 `0d8830f4e9adf5ce2a7db77af48468aba2c1bc9724b29d8d91a709162cfa6fbd`，ZIP CRC 通过，119 文件）
**公开分发 zip**：`photo-skills-combined-ABC-user-v1.0-public-2026-10-05.zip`（排除 2 张不公开素材）

## 一、本次交付内容

- 统一入口：根 `SKILL.md`（技能名 `photo-skills-abc-user`）；模块版本 **A 1.3.1 · B 5.4.0 · C 1.1.1**。
- 默认路由变化：R8「无人像 A+B / 有人像 A+B+C」→ R9「**场景主角正常 A + 重 B** / **人物主角正常 C + 重 B**」，**不再串联 A+C**。
- 强度分离：照片重绘程度（`T0–T3` / `PRESERVE`）与页面设计强度（`design_strength`）拆为独立字段；`PRESERVE + T0 + strong B` 合法。
- 新增交付契约 `B-photo-zine-v5.4.0/references/delivery-contract.md`、完成判据（`base_done` ≠ `done`；只交付底片必须标注 B 未完成）、20 项回归情境记录。
- 例外保留：显式「只调色 / 只真实后期 / 不要设计 / 轻 B / 只分析」按用户指令执行。

## 二、与 R8 的差异（可追溯）

- 旧模块目录 `A-photo-real-grade-v1.4/`、`B-photo-zine-v5.3.4/`、`C-portrait-real-grade-v1.0/` 随本次发布由新版本目录取代；**内容仍完整保留在 git 历史中**（R8 提交 `35dee4e`、`f7ccca4`），可随时回溯取回。
- 本次输入包不包含以下 R8 文件，按用户指示**以本次输入包为准、不从远端旧规则回填**：
  - `A/references/heritage-architecture-look.md`
  - `B/references/heritage-photo-foundation.md`、`B/references/batch-diversity.md`
  - `B/reference-library/positive/37_Wall_and_Heaven_approved.webp`
- A / B / C 的业务规则文件与参考图均为本次包的**字节级内容**（仅在公开副本中修改了 B 的 reference-index 公开数量与 QC/清单计数）；A、C 模块与输入包逐字节一致。

## 三、公开素材处理

- 公开 **45 张**（A 10 张；B 35 张 = 正向 34 + 反例 1）。
- 移出 **2 张**（不公开）：`B-photo-zine-v5.4.0/reference-library/positive/14_Mutianyu_Second_World.webp`、`…/28_On_the_Hill.webp` —— 与该两张此前移出的文件**字节完全一致**（SHA-256 `fb489059…`、`62f2349f…`），沿用既有处理结论。
- 与上一版公开树全量 SHA-256 对比：**新增 0 张、变更 0 张**，无需重复审查。
- 文件保留在本地 `private-assets-review/`（`.gitignore` 已排除），未删除。详见 `PUBLIC_ASSET_REVIEW.md`。

## 四、校验结果

| 项目 | 结果 |
|---|---|
| 输入完整包 SHA-256 | 与用户提供值一致；ZIP CRC 通过；119 文件 |
| 公开副本清单自校验（根 + A/B/C） | 0 失败（逐文件 SHA-256 复核） |
| 敏感信息扫描（72 个文本文件） | 无 Key/Token/密码/.env/本机用户名/本地绝对路径/聊天缓存 |
| `golden-backup` SHA-256 | `c3498fd0113953f69f25715ac865f97ae7d5a4479d0e525f9fe7eec1f4b30624` 未变 |
| 远端 main / tag / Release 资产 | 见发布后核验记录 |
| 图像生成 API | 未调用；本次未实测成品视觉效果（仅发布已完成分发包） |

历史档案说明：`audits/PACKAGE_SHA256SUMS.txt`、`audits/R6–R8_*` 为对应版本的原始记录，按当时的图片数量与规则书写，与本版公开树不一致属预期。
