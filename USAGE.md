# 使用指南（USAGE）

本仓库是一套给 AI 用的照片处理技能包（A+B+C 合包）。三种用法，按你的情况任选。

## 一、给 AI Agent 的「一句话安装」★ 推荐

把下面这句话整段复制，发给你正在使用的 AI Agent（Claude Code / Codex / Cursor / 任何具备终端与文件能力的 agent）——它会自己完成安装：

> 请安装照片技能包：克隆 https://github.com/tuozhekongqi/photo-skills.git ，将其中的 A-photo-real-grade-v1.4、B-photo-zine-v5.3.4、C-portrait-real-grade-v1.0 三个目录安装为你的技能（各自以 SKILL.md 为入口），并阅读仓库根目录的 ROUTING.md 与 FEEDBACK_ABSORPTION_POLICY.md 作为运行规则。装好后告诉我它可以怎么用。

也可以直接执行（以 Claude Code 为例，其个人技能目录为 `~/.claude/skills/`；其他工具请让 agent 放进它自己的技能目录）：

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
