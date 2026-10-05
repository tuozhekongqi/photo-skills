# INSTALL.md — Photo Skills 安装说明（AI Agent 版）

> **For AI agents:** follow this document to install Photo Skills (ABC user package) as your own skills, then use the root `SKILL.md` + `ROUTING.md` as the entry and default routing rule.
> **人类用户：** 请看 [README](README.md) / [USAGE](USAGE.md)；想让 agent 自动装，把文末的「一句话」发给它即可。

## 你将安装什么

Photo Skills **R9 — ABC 用户版**（统一入口 + 三个模块 + 路由/反馈规则）：

- `SKILL.md`（根目录）— 统一入口技能，技能名 `photo-skills-abc-user`：先读它，再依路由读子模块
- `A-photo-real-grade-v1.3.1/` — 正常场景真实底片处理（既有后期权重保留）
- `B-photo-zine-v5.4.0/` — Photo Zine / 编辑设计层；**默认重 B**；照片重绘程度与设计强度分离
- `C-portrait-real-grade-v1.1.1/` — 正常人像底片与明确授权的局部修整
- `ROUTING.md` — 默认路由：场景主角 **正常 A + 重 B**；人物主角 **正常 C + 重 B**；**不串联 A+C**；仅用户显式指令可改变
- `FEEDBACK_ABSORPTION_POLICY.md` — 反馈吸收机制

## 安装步骤

### 1. 获取文件（按顺序尝试，任一成功即可）

1. git 可用：
   ```bash
   git clone --depth 1 https://github.com/tuozhekongqi/photo-skills.git
   ```
2. 网络受限（git 不可用）：下载 zip 并解压（解压后文件位于 `photo-skills-main/` 下）：
   ```bash
   curl -L -o photo-skills.zip https://codeload.github.com/tuozhekongqi/photo-skills/zip/refs/heads/main
   ```
3. 都不行：请你的用户提供仓库 zip（GitHub 页面 `Code → Download ZIP` 下载后发给你）。

### 2. 安装为你的技能

- **有技能目录**（如 Claude Code 为 `~/.claude/skills/`）：把根目录 `SKILL.md` 与三个模块目录**原样**复制进去（目录名保持不变）。根 `SKILL.md` 是统一入口；若你的环境要求每个技能独占一个目录，则新建一个目录（建议 `photo-skills-abc-user/`）放入根 `SKILL.md`、`ROUTING.md` 与三个模块目录。
- **安装后必须显式调用入口**：在支持本地技能的环境里，显式调用 `photo-skills-abc-user`（或在运行配置中把它设为本包的入口）。**只把四个目录放进技能目录，不保证统一入口被优先选中。**
- **没有技能机制**：将根 `SKILL.md`、`ROUTING.md`、`FEEDBACK_ABSORPTION_POLICY.md` 与三个模块 `SKILL.md` 载入为常驻规则；`references/` 按需查阅。
- **纯对话、没有文件系统**：直接读取以下文件并遵守（把 `<路径>` 换成上面列出的文件名）：
  - `https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/<路径>`
  - 国内镜像：`https://cdn.jsdelivr.net/gh/tuozhekongqi/photo-skills@main/<路径>`

### 3. 校验

- 根 `SKILL.md` 与三个模块 `SKILL.md`、`ROUTING.md` 均可读；
- 路由确认：场景主角默认 **A+B（正常 A + 重 B）**；人物主角默认 **C+B（正常 C + 重 B）**；**不串联 A+C**；
- 强度确认：`PRESERVE + T0 + strong B` 合法；「只调色 / 不要设计 / 轻 B / 只分析」按例外执行；
- 完成判据确认：只完成底片时不得标成 B 已完成。

### 4. 向用户汇报

安装完成，请用户直接发照片；如实说明默认规则（正常底片 + 重 B，避免 P 过 / AI 味）。

## 注意

- 请勿修改、简化或合并模块规则文件。
- 本仓库未附开源许可证（保留所有权利）：未经许可不得商用。

## 一句话（人类复制给 agent）

> `curl -fsSL https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/INSTALL.md`，然后按该文件说明安装 Photo Skills（ABC 用户版）；装好后读根目录 SKILL.md 与 ROUTING.md 并开始使用。
