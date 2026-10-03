# Photo Skills — A+B+C 合包（R8）

一套**真实照片后期与设计表达**的 AI Agent 技能包（Skills）。三个模块职责独立、协同运行，共享同一套路由、反馈吸收和最终质量检查逻辑。

## 模块与职责

| 模块 | 目录 | 职责 | 默认介入强度 |
|---|---|---|---|
| **A — Scene Real Grade** | [`A-photo-real-grade-v1.4/`](A-photo-real-grade-v1.4/) | 场景真实摄影基础：曝光、白平衡、局部明暗、色彩层次、环境光线一致性、真实感维护 | 最小必要改动；原片已经成立时，接近原片是有效结果 |
| **B — Photo Zine / Editorial** | [`B-photo-zine-v5.3.4/`](B-photo-zine-v5.3.4/) | 设计表达层：留白、版式、文字、纸张/印刷语言、单图 editorial、条件式 source-led 拼接 | photo-first；可以极其克制或 near-no-op |
| **C — Portrait Real Grade** | [`C-portrait-real-grade-v1.0/`](C-portrait-real-grade-v1.0/) | 人像真实处理层：人物身份、皮肤、脸部轮廓、头发、服装反应、人物局部光线与自然体态 | 仅在明确人像时加入；默认低强度 |

## 默认路由（固定）

| 输入情况 | 默认组合 |
|---|---|
| 不存在明确人像 / 人物主体 | **A + B** |
| 存在明确人像 / 人物主体 | **A + B + C** |
| 用户明确指定模块组合或关闭某模块 | 按用户明确要求执行 |

- 「有人像」指人物是清晰主体、重要主体之一，或照片明显以人物为表达核心；远处路人、很小的背景人物、仅提供尺度感的行人，不自动触发 C。
- 「只轻修」「保持真实」「只调色」「只调光影」「照片已经很好」属于**处理强度**要求，默认不改变模块组合。
- 「不要设计」视为明确关闭 B；「不要人像处理」视为明确关闭 C。

### 路由不变量：模块启用与处理强度分离

默认模块组合和每个模块的可见处理强度是两件事：

- 无人像时，A+B 默认保持激活；存在明确人像时，A+B+C 默认保持激活；
- 原片已经很好、只需轻修、只提到调色/光影、明显设计没有增益、最优结果接近原片，都**不能自动让某个模块退出默认组合**；
- 对应模块应改为 `near-no-op / 极低强度`，而不是改写默认路由；
- 只有用户明确指定模块或关闭模块，才能改变默认组合。

**启用 ≠ 必须产生明显效果。** B 激活不代表必须加字、边框、拼接或纸张；C 激活不代表必须改变脸型、皮肤或身体。

完整规则见 [`ROUTING.md`](ROUTING.md)；反馈吸收机制见 [`FEEDBACK_ABSORPTION_POLICY.md`](FEEDBACK_ABSORPTION_POLICY.md)。

## 稳定基线

1. 用户通常对原片已经满意；默认不是把照片改得更厉害，而是避免 P 过、AI 味、滤镜味。
2. 新知识扩充工具箱，不自动改变默认审美或模块权重。
3. 默认路由是职责覆盖，不是效果强度；原片质量、轻修需求或低设计增益只能降低模块强度，不能让模块自动退出默认组合；各模块都可以接近 no-op。
4. B 可以只对单张照片做克制 editorial；B 不等于拼接。
5. 批次处理不为了省事合并照片，也不靠固定风格配额制造多样性。
6. 九宫格 / 网格照片墙只是末尾硬失败检查，不参与主风格决策。

## 仓库结构

```
├── README.md
├── CHANGELOG.md                    # 版本历史
├── ROUTING.md                      # A/B/C 默认路由规则（R8）
├── FEEDBACK_ABSORPTION_POLICY.md   # 反馈吸收机制（v1.1）
├── PUBLIC_ASSET_REVIEW.md          # 参考图库公开上传审查说明
├── A-photo-real-grade-v1.4/        # 模块 A（SKILL.md / references / reference-library / qc）
├── B-photo-zine-v5.3.4/            # 模块 B（SKILL.md / references / reference-library / qc）
├── C-portrait-real-grade-v1.0/     # 模块 C（SKILL.md / references / qc）
├── audits/                         # R6–R8 审计与机器质检记录
└── golden-backup/                  # 原始 B V5.3 黄金备份（不可变，不参与运行）
```

## 快速开始（怎么用）

**① 给 AI Agent 的一句话安装（推荐）** —— 把这句话发给你的 agent（Claude Code / Codex / Cursor 等），它会自己装好：
> 请安装照片技能包：克隆 https://github.com/tuozhekongqi/photo-skills.git ，把其中 A / B / C 三个技能目录安装为你的技能（入口为各自 SKILL.md），并以 ROUTING.md 作为默认路由规则。

**② 聊天 AI 粘贴用法** —— 下载 [`quickstart/快速版提示词.md`](quickstart/快速版提示词.md)（或 Release 附件），整段粘贴给豆包 / DeepSeek 等，再发照片。默认路由：无人像 A+B；有人像 A+B+C；「不要设计 / 不要人像处理」可单独关闭对应层。

**③ 开发者** —— 入口顺序：`ROUTING.md` → 模块 `SKILL.md` → `references/`。

详细步骤（含手动安装命令与分享话术）见 [`USAGE.md`](USAGE.md)。

## 版本

- 当前稳定版：**R8**
- `golden-backup/`：原始 B V5.3 黄金备份，字节级保留，不参与运行、不允许覆盖
- `audits/`：R6 / R7 / R8 审计与 QC 记录；版本详情见 [`CHANGELOG.md`](CHANGELOG.md)

## 素材说明

参考图库（reference-library）图片已做公开上传审查；个别素材已移出公开范围，原因与清单见 [`PUBLIC_ASSET_REVIEW.md`](PUBLIC_ASSET_REVIEW.md)。

## 许可说明

本仓库暂未附带开源许可证（保留所有权利）。未经明确许可，**不得将本仓库内容用于商业用途**。
