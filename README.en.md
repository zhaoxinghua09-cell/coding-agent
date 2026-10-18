# coding-agent · Background Coding Delegation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![Category](https://img.shields.io/badge/category-dev--tools-8a2be2.svg)](#)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](#)
[![llms.txt](https://img.shields.io/badge/AI--friendly-llms.txt-101E2C.svg)](llms.txt)
[![中文](https://img.shields.io/badge/%E4%B8%AD%E6%96%87-README.md-blue.svg)](README.md)

> Delegate coding work to Codex, Claude Code or OpenCode as background workers — for large refactors, PR review and long-running feature work; dispatch, execution and recovery are audited end to end on an evidence chain.

**Keywords**: 后台编码 · coding agent · 大型重构 · PR 审查 · 自动化 PR · 后台开发 · delegate coding · background coding · codex · claude code

This repository is an **Agent Skill distribution package**. The core file `SKILL.md` follows the Agent Skills spec (YAML frontmatter) and packages the method of "把长编码任务丢给后台 runner，全程可还原「谁、依据什么、改了什么」" into a skill an AI agent can load directly. Drop it into your agent's skills directory (e.g. `~/.workbuddy/skills/`).

- **Category**: 开发工具 / Dev Tools
- **Version**: 1.0.0
- **Author**: 诺声(Logos)@SynomosAI
- **License**: MIT (see [LICENSE](LICENSE))

---

## Features

- 后台长任务：大型重构、PR 审查、后台功能开发等不适合前台阻塞的任务
- 多 runner：Codex / Claude Code / OpenCode 作为后台工作进程
- 证据链审计：可还原「哪个 agent、依据什么指令、改了什么」
- 派单 → 执行 → 回收：全过程留痕，失败可回溯
- 通用方法论工具：非医疗器械 / 非医疗软件，无疗效或临床声明
- 多语种：中 / 英 / 日 / 韩 / 西 / 法 / 德 / 阿（核心 8 种）

---

## Quick Start

Prerequisite: an AI coding assistant / skill runtime that can load Agent Skills. 无独立可执行服务；本包为后台委托编排方法论.

```bash
# 1. 克隆本仓库
git clone https://github.com/zhaoxinghua09-cell/coding-agent.git
cd coding-agent

# 2. 查看技能主文件（派单格式、runner 选择、回收与审计口径）
cat SKILL.md

# 3. 把技能目录放进你的 Agent 技能目录（示例：WorkBuddy）
#    cp -r . ~/.workbuddy/skills/coding-agent/
```

Then invoke it in natural language, e.g.:

```text
「大重构能不能丢给后台跑」
「PR 能不能自动审」
「把这个后台功能开发派出去跑」
```

---

## Usage

1. Clone this repo, or copy the skill directory into your agent's skills folder.
2. Call the capability via the trigger keywords described in `SKILL.md`.
3. See `SKILL.md` for the full method, boundaries and provenance.

---

## Repository layout

```text
coding-agent/
├── README.md            # 本文件（双语）
├── README.en.md         # 英文版说明
├── SKILL.md             # 技能主文件（Agent Skills 规范 · YAML frontmatter）
├── manifest.json        # 技能元数据（名称 / 版本 / 许可 / 描述）
├── LICENSE              # MIT 许可全文
├── SECURITY.md          # 安全策略
├── CONTRIBUTING.md      # 贡献指南
├── AGENTS.md            # 给 AI Agent 的工作指引
├── llms.txt             # 给 AI 的最小索引（llms.txt 标准）
└── llms-full.txt        # 给 AI 的完整文本
```

---

## License

Released under the **MIT** license. See [LICENSE](LICENSE) for the full text. Attribution: cite this repository `https://github.com/zhaoxinghua09-cell/coding-agent` and the rights holder "赵兴华 / Steven Zhao·China". Contact: zhaoxinghua06@126.com ｜ ORCID 0009-0001-0512-1237.

---

## Security

If you find a security issue, report it privately per [SECURITY.md](SECURITY.md); do not disclose it in a public issue.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Keep the `SKILL.md` YAML frontmatter fields compatible when changing this skill.

## Disclaimer

This repository content is a **theoretical stance and tooling exploration**. It does not represent any certified, commercially delivered, or client-served claim. External standards, certifications and clause information are restatements of public sources; independently verify before formal citation. APIs, authorization codes and ambassadors are roadmap items, not yet live.
