# ABC 用户版 v1.0 — 验证结果

已实施：场景默认正常 A + 重 B；人像默认正常 C + 重 B。A/C 既有真实后期权重保留。统一入口、设计强度独立字段、提示词、保守回退、完成状态、验收和示例已同步。

| 检查 | 结果 |
|---|---|
| 根入口与 A/B/C 四份技能元数据 | 4/4 通过 skill-creator quick_validate |
| 相对 Markdown 文件链接 | 8/8 有效 |
| 行内代码文件引用 | 100/100 可解析 |
| 关键文档契约检查 | 12/12 通过；只验证文档结构和关键条款 |
| 回归情境 | 已记录 20 项预期行为；未进行图像生成行为测试 |
| A/B/C 内容 SHA256 | 100 项重建并验证 |
| 原有图片资产 | 47/47 字节一致 |
| 原压缩包 | SHA256 一致，未改动 |

详细证据：qc/VALIDATION.json、qc/BUILD_EVIDENCE.json、qc/REGRESSION_CASES.md、qc/CHANGE_SCOPE.md。各模块 qc 清单不含自身 qc 输出；根 qc 清单覆盖全部文件，排除根清单自身的两份文件。

本次完成分发包规则修改与静态验证，未调用图片生成 API，未实测成品的视觉效果，也未安装或覆盖本机技能。实际使用请调用根入口 photo-skills-abc-user；图像生成时仍须检查身份/来源和重 B 的可见关系，不能用文档校验代替视觉验收。

## 公开分发副本（本仓库发布内容）

- 本仓库发布的是该包的**公开树**：参考图 **45 张**（A 10 张；B 35 张 = 正向 34 + 反例 1）。
- 完整包含 47 张参考图；`14_Mutianyu_Second_World.webp`、`28_On_the_Hill.webp` 因第三方官方标识 / 可辨人脸不随公开仓库发布，保留在完整包与本地 `private-assets-review/`（已 gitignore）。原图字节与此前公开审查移出的两张完全一致。
- 模块与根 `MANIFEST.csv` / `SHA256SUMS.txt` 已按公开树重新生成；`qc/VALIDATION.json`、`qc/BUILD_EVIDENCE.json`、`qc/CHANGE_SCOPE.md`、`qc/REGRESSION_CASES.md` 为**完整包（47 张）**的构建证据，按原字节保留，其计数与本公开树相差 2 张属预期。
- 除上述两张图与其派生清单计数外，业务规则文件与参考图均为本包字节级内容，未做重写或合并。

本仓库根 `qc/MANIFEST.csv` 与 `qc/SHA256SUMS.txt` 覆盖**本仓库全部已发布文件**（排除 `.git/`、已 gitignore 的 `private-assets-review/`，以及这两份清单自身）；其中 `qc/VALIDATION.json`、`qc/BUILD_EVIDENCE.json`、`qc/CHANGE_SCOPE.md`、`qc/REGRESSION_CASES.md` 为完整包构建证据，按输入包原字节保留。分发包 zip 内自带其自身的 qc 清单（不含仓库级文档）。
