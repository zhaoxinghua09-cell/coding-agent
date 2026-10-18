# coding-agent · 后台编码委托

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![Category](https://img.shields.io/badge/category-dev--tools-8a2be2.svg)](#)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](#)
[![Multilingual](https://img.shields.io/badge/i18n-8%20languages-brightgreen.svg)](#)
[![llms.txt](https://img.shields.io/badge/AI--friendly-llms.txt-101E2C.svg)](llms.txt)
[![English](https://img.shields.io/badge/English-README.en.md-blue.svg)](README.en.md)

> 将编码工作委托给 Codex、Claude Code 或 OpenCode 作为后台工作进程执行——适用大型重构、PR 审查、后台功能开发等长任务；派单、执行与回收全过程按证据链审计留痕。
> Delegate coding work to Codex, Claude Code or OpenCode as background workers — for large refactors, PR review and long-running feature work; dispatch, execution and recovery are audited end to end on an evidence chain.

SynomosAI 四支柱体系：**身份（Identity）· 溯源（Traceability）· 治理（Governance）· 共生（Symbiosis）**——当 AI 进入商业，可信是唯一的硬通货。

**关键词 / Keywords**：后台编码 · coding agent · 大型重构 · PR 审查 · 自动化 PR · 后台开发 · delegate coding · background coding · codex · claude code

本仓库是一个 **Agent Skill 发布包**：核心文件 `SKILL.md` 遵循 Agent Skills 规范（YAML frontmatter），把「把长编码任务丢给后台 runner，全程可还原「谁、依据什么、改了什么」」的方法固化为可被 AI Agent 直接加载的技能。可直接放入主流 AI Agent（如 WorkBuddy）的技能目录使用。

- **分类 / Category**：开发工具 / Dev Tools
- **版本 / Version**：1.0.0
- **署名 / Author**：诺声(Logos)@SynomosAI
- **许可 / License**：MIT（详见仓库 [LICENSE](LICENSE)）

---

## ✨ 特性 / Features

- 后台长任务：大型重构、PR 审查、后台功能开发等不适合前台阻塞的任务
- 多 runner：Codex / Claude Code / OpenCode 作为后台工作进程
- 证据链审计：可还原「哪个 agent、依据什么指令、改了什么」
- 派单 → 执行 → 回收：全过程留痕，失败可回溯
- 通用方法论工具：非医疗器械 / 非医疗软件，无疗效或临床声明
- 多语种：中 / 英 / 日 / 韩 / 西 / 法 / 德 / 阿（核心 8 种）

---

## 🚀 快速开始 / Quick Start

前置：一个能加载 Agent Skill 的 AI 编码助手 / 技能运行时；无独立可执行服务；本包为后台委托编排方法论。

```bash
# 1. 克隆本仓库
git clone https://github.com/zhaoxinghua09-cell/coding-agent.git
cd coding-agent

# 2. 查看技能主文件（派单格式、runner 选择、回收与审计口径）
cat SKILL.md

# 3. 把技能目录放进你的 Agent 技能目录（示例：WorkBuddy）
#    cp -r . ~/.workbuddy/skills/coding-agent/
```

跑通后，直接用自然语言发起调用，例如：

```text
「大重构能不能丢给后台跑」
「PR 能不能自动审」
「把这个后台功能开发派出去跑」
```

---

## 📖 使用方式 / Usage

1. 克隆本仓库，或将技能目录放入 Agent 技能目录（如 `~/.workbuddy/skills/`）；
2. 按 `SKILL.md` 的描述与触发词调用对应能力；
3. 详细方法、边界与治理溯源见 `SKILL.md` 正文。

> 按 SKILL.md 的派单格式发起后台任务，并在回收时核对证据链留痕。

---

## 📁 仓库结构 / Repository layout

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

## 许可说明 · License Notice

- **权利状态**：本仓库以 **MIT 许可** 许可发布，可依该许可证条款自由使用、修改与再分发。
- **引用建议**：引用时请标注仓库名与原文链接 `https://github.com/zhaoxinghua09-cell/coding-agent`
  与权利人「赵兴华 / Steven Zhao·China」。
- **品牌状态限定**：MedXpert、SynomosAI、LGD 等为相关项目标识，
  **均未申请实体注册、未申请商标注册**；出现仅作来源标识，
  不构成对法人实体或商标权的任何主张。
- **完整条款**：见仓库根目录 [LICENSE](LICENSE)。
- **联系**：zhaoxinghua06@126.com ｜ ORCID 0009-0001-0512-1237

---

## 🔒 安全 / Security

如发现安全问题，请按 [`SECURITY.md`](SECURITY.md) 的方式私下报告，不要在公开 issue 中披露。

## 🤝 贡献 / Contributing

欢迎按 [`CONTRIBUTING.md`](CONTRIBUTING.md) 提交改进。本仓库为技能发布包，改动请保持 `SKILL.md` 的 YAML frontmatter 字段兼容（`name` / `slug` / `version` / `license` 等）。

## 免责声明

本仓库内容为**理论站位与工具化探索**，不代表任何已获认证、已商业化交付或已服务特定客户的声明；文中涉及的外部标准、认证与条款信息为公开资料转述，正式引用前请**独立核实**。API、授权码与形象大使等为路线图（roadmap）事项，尚未上线。
