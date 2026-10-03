# 使用指南（USAGE）

本仓库是一套给 AI 用的照片处理技能包（A+B+C 合包）。三种用法，按你的情况任选。

## 一、给 AI Agent 的「一句话安装」★ 推荐

把下面这句整段复制，发给你正在使用的 AI Agent（Claude Code / Codex / Cursor / 任何有联网能力的 agent）——它会**拉取安装说明、自己完成安装**：

> `curl -fsSL https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/INSTALL.md`，然后按该文件的说明把 Photo Skills（A/B/C）安装为你的技能；装好后阅读各 SKILL.md 与 ROUTING.md 并开始使用。

（安装说明文件 [INSTALL.md](INSTALL.md) 内含各工具的落盘方式与网络兜底；国内网络打不开 raw.githubusercontent.com 时，换用 jsDelivr 镜像：`curl -fsSL https://cdn.jsdelivr.net/gh/tuozhekongqi/photo-skills@main/INSTALL.md`。）

**手动方式（备选）**——以 Claude Code 为例（个人技能目录 `~/.claude/skills/`；其他工具请让 agent 放进它自己的技能目录）：

```bash
git clone --depth 1 https://github.com/tuozhekongqi/photo-skills.git
mkdir -p ~/.claude/skills
cp -r photo-skills/A-photo-real-grade-v1.4 photo-skills/B-photo-zine-v5.3.4 photo-skills/C-portrait-real-grade-v1.0 ~/.claude/skills/
```

安装完成后：直接把照片发给它即可。默认路由——**无人像 A+B，有人像 A+B+C**。

> 如果 agent 无法访问 GitHub（网络受限）：先在本页 `Code → Download ZIP` 手动下载，把 zip 发给 agent 让它自行安装。
> 如果 agent 没有「技能」机制：让它把 A/B/C 的 `SKILL.md` 与 `ROUTING.md` 作为常驻规则载入（写入它的项目规则 / 记忆文件均可）。

## 二、用聊天 AI（没有 Agent：粘贴即用）

1. 打开 [`quickstart/快速版提示词.md`](quickstart/快速版提示词.md)，或到 [Releases](https://github.com/tuozhekongqi/photo-skills/releases) 下载它的 txt 附件；
2. 全文复制，粘贴给任意 AI（豆包 / DeepSeek / ChatGPT / 通义等）作为对话开头；豆包可保存为「智能体」长期使用；
3. 直接发照片。默认路由同上；说「不要设计」「不要人像处理」可单独关闭对应层。

## 三、直接读规则 / 集成开发

- 入口顺序：`ROUTING.md` → 各模块 `SKILL.md` → `references/`；
- 版本与审计：`CHANGELOG.md`、`audits/`；
- 黄金备份：`golden-backup/`（B V5.3 原始备份，不参与运行）。

## 分享话术（复制即用）

> 一套给 AI 用的照片处理规则（无人像 A+B、有人像 A+B+C，默认最小必要改动）。
> 仓库：https://github.com/tuozhekongqi/photo-skills
> 用法：把你的 AI 接上这个仓库（或使用「快速版提示词」），然后发照片就行。
