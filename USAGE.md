# 使用指南（USAGE）

本仓库是一套给 AI 用的照片处理技能包（**ABC 用户版**）。三种用法，按你的情况任选。默认交付是**正常底片处理 + 重 B**。

## 一、给 AI Agent 的「一句话安装」★ 推荐

把下面这句整段复制，发给你正在使用的 AI Agent（Claude Code / Codex / Cursor / 任何有联网能力的 agent）——它会**拉取安装说明、自己完成安装**：

> `curl -fsSL https://raw.githubusercontent.com/tuozhekongqi/photo-skills/main/INSTALL.md`，然后按该文件的说明把 Photo Skills（ABC 用户版）安装为你的技能；装好后读根目录 SKILL.md 与 ROUTING.md 并开始使用。

（安装说明文件 [INSTALL.md](INSTALL.md) 内含各工具的落盘方式与网络兜底；国内网络打不开 raw.githubusercontent.com 时，换用 jsDelivr 镜像：`curl -fsSL https://cdn.jsdelivr.net/gh/tuozhekongqi/photo-skills@main/INSTALL.md`。）

**手动方式（备选）**——以 Claude Code 为例（个人技能目录 `~/.claude/skills/`；其他工具请让 agent 放进它自己的技能目录）：

```bash
git clone --depth 1 https://github.com/tuozhekongqi/photo-skills.git
mkdir -p ~/.claude/skills/photo-skills-abc-user
cp photo-skills/SKILL.md photo-skills/ROUTING.md ~/.claude/skills/photo-skills-abc-user/
cp -r photo-skills/A-photo-real-grade-v1.3.1 photo-skills/B-photo-zine-v5.4.0 photo-skills/C-portrait-real-grade-v1.1.1 ~/.claude/skills/photo-skills-abc-user/
```

安装完成后：直接把照片发给它即可。默认路由——**场景主角正常 A + 重 B，人物主角正常 C + 重 B**（不串联 A+C）。记得显式调用入口 `photo-skills-abc-user`，否则统一入口不一定被选中。

> 如果 agent 无法访问 GitHub（网络受限）：先在本页 `Code → Download ZIP` 手动下载，把 zip 发给 agent 让它自行安装。
> 如果 agent 没有「技能」机制：让它把根 `SKILL.md`、`ROUTING.md` 与 A/B/C 的 `SKILL.md` 作为常驻规则载入（写入它的项目规则 / 记忆文件均可）。

## 二、用聊天 AI（没有 Agent：粘贴即用）

1. 打开 [`quickstart/快速版提示词.md`](quickstart/快速版提示词.md)，或到 [Releases](https://github.com/tuozhekongqi/photo-skills/releases) 下载它的 txt 附件；
2. 全文复制，粘贴给任意 AI（豆包 / DeepSeek / ChatGPT / 通义等）作为对话开头；豆包可保存为「智能体」长期使用；
3. 直接发照片。默认：场景正常 A + 重 B、人物正常 C + 重 B；说「只调色」「不要设计」「轻 B」可改变设计强度。

## 三、直接读规则 / 集成开发

- 入口顺序：根 `SKILL.md` → `ROUTING.md` → 各模块 `SKILL.md` → `references/`；
- 交付契约与完成判据：`B-photo-zine-v5.4.0/references/delivery-contract.md`；
- 版本与审计：`CHANGELOG.md`、`audits/`；文件清单与哈希：`qc/`；
- 黄金备份：`golden-backup/`（B V5.3 原始备份，不参与运行，不可覆盖）。

## 分享话术（复制即用）

> 一套给 AI 用的照片处理规则（场景正常修 + 重设计，人物正常修 + 重设计，默认不做假）。
> 仓库：https://github.com/tuozhekongqi/photo-skills
> 用法：把你的 AI 接上这个仓库（或使用「快速版提示词」），然后发照片就行。
