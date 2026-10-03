# INSTALL.md — Photo Skills 安装说明（AI Agent 版）

> **For AI agents:** follow this document to install Photo Skills (A/B/C) as your own skills, then use `ROUTING.md` as the default routing rule.
> **人类用户：** 请看 [README](README.md) / [USAGE](USAGE.md)；想让 agent 自动装，把文末的「一句话」发给它即可。

## 你将安装什么

Photo Skills R8 —— 照片处理技能包（三个模块 + 路由/反馈规则）：

- `A-photo-real-grade-v1.4/` — 真实摄影后期（最小必要改动）
- `B-photo-zine-v5.3.4/` — Photo Zine / 编辑设计层（photo-first）
- `C-portrait-real-grade-v1.0/` — 人像真实处理层
- `ROUTING.md` — 默认路由：无人像 **A+B**；有人像 **A+B+C**；仅用户显式指令可改变组合
- `FEEDBACK_ABSORPTION_POLICY.md` — 反馈吸收机制

## 安装步骤

### 1. 获取文件（按顺序尝试，任一成功即可）

1. git 可用：
   ```bash
   git clone --depth 1 https://github.com/tuozhekongqi/photo-skills.git
   ```
2. 网络受限（git 不可用）：下载 zip 并解压（解压后模块目录位于 `photo-skills-main/` 下）：
   ```bash
   curl -L -o photo-skills.zip https://codeload.github.com/tuozhekongqi/photo-skills/zip/refs/heads/main
   ```
3. 都不行：请你的用户提供仓库 zip（GitHub 页面 `Code → Download ZIP` 下载后发给你）。

### 2. 安装为你的技能

- **有技能目录**（如 Claude Code 为 `~/.claude/skills/`）：把三个模块目录**原样**复制进去（目录名保持不变）。
- **没有技能机制**：将 `ROUTING.md`、`FEEDBACK_ABSORPTION_POLICY.md` 与三个 `SKILL.md` 载入为常驻规则；`references/` 按需查阅。
- **纯对话、没有文件系统**：直接读取以下文件并遵守（把 `<路径>` 换成上面列出的文件名）：
  - `https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/<路径>`
  - 国内镜像：`https://cdn.jsdelivr.net/gh/tuozhekongqi/photo-skills@main/<路径>`

### 3. 校验

- 三个 `SKILL.md` 与 `ROUTING.md` 均可读；
- 路由确认：无人像 A+B；有人像 A+B+C；仅显式指令可改变组合；各模块可 near-no-op。

### 4. 向用户汇报

安装完成，请用户直接发照片；如实说明默认规则（最小必要改动，避免 P 过 / AI 味）。

## 注意

- 请勿修改、简化或合并模块规则文件。
- 本仓库未附开源许可证（保留所有权利）：未经许可不得商用。

## 一句话（人类复制给 agent）

> `curl -fsSL https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/INSTALL.md`，然后按该文件说明安装 Photo Skills（A/B/C）；装好后阅读各 SKILL.md 与 ROUTING.md 并开始使用。
