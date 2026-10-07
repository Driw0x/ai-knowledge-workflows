# AI Knowledge Workflows

[English](README.md) | [Français](README.fr.md) | [简体中文](README.zh-CN.md)

面向研究、项目管理、技能评估和技术文档的可复用 AI Agent 工作流、提示词模式和知识库模板。

本仓库围绕一个简单原则构建：

> 将长期有效的上下文保存在版本控制文件中，让提示词专注于当前任务，并让输出足够结构化以便验证。

## 本仓库展示的内容

本项目并不是孤立提示词的集合。

它展示了一套可复用的 AI Agent 工作流架构，包括：

- 提示词拆解；
- 上下文管理；
- 显式任务约束；
- 基于证据的推理；
- 输出契约；
- 可复用模板；
- 注重隐私的本地上下文；
- 最小差异更新策略；
- 可由人工验证的研究；
- 通过 Git 对提示词进行版本管理。

这些模式适用于 Codex 等编程和研究 Agent，以及其他基于 LLM 的助手。

## 架构

```text
用户请求
    ↓
AGENTS.md
    ↓
私有 / 本地知识
    ↓
任务专用提示词
    ↓
研究或仓库检查
    ↓
结构化输出
    ↓
人工审核
    ↓
知识库更新
```

公共仓库只包含可复用的工作流。

个人上下文保留在本地。

## 仓库结构

```text
ai-knowledge-workflows/
├── README.md
├── LICENSE
├── .gitignore
│
├── agents/
│   └── AGENTS.example.md
│
├── prompts/
│   ├── application/
│   ├── career/
│   ├── project/
│   ├── knowledge/
│   ├── skills/
│   ├── documentation/
│   └── portfolio/
│
├── templates/
│
├── examples/
│
├── docs/
│
└── evals/
    ├── README.md
    ├── rubrics/
    ├── templates/
    ├── results/
    └── cases/
```

## 工作流目录

### 求职申请

`prompts/application/`

准备有来源支持的申请材料，并决定复用、调整还是创建简历。工作流保留人工审核和手动提交。

如需该工作流的独立应用实现，请参阅 [AI Job Application Workbench](https://github.com/Driw0x/ai-job-application-workbench)。

### 职业发展

`prompts/career/internship-research.md`

搜索当前实习机会，并与经过验证的候选人资料进行比较。

主要思路：

- 验证当前来源；
- 地理位置和岗位约束；
- 匹配度分析；
- 持续提取技能差距；
- 项目与岗位匹配；
- 带日期的研究报告。

### 项目

`prompts/project/`

根据仓库证据创建、更新和评估项目记录。

工作流区分：

- 已实现功能；
- 计划功能；
- 已放弃的方法；
- 已证明的技能；
- 缺乏依据的假设。

### 知识

`prompts/knowledge/`

从源材料中提取长期有效的知识，整合重叠笔记，并审计知识库中的不一致。

### 技能

`prompts/skills/`

评估现有证据真正证明了哪些技能，将技能记录与当前项目和经历同步，并分析多个项目中的能力证据。

### 文档

`prompts/documentation/`

审计或更新技术文档，并在保留隐私和正常功能的前提下，从私有来源中提取可复用的独立仓库。

### 作品集

`prompts/portfolio/synchronize-portfolio.md`

将公共作品集与经过验证的知识库同步，同时保护隐私并采用最小差异更新。

## 提示词评估

`evals/`

使用可复用案例、统一评分标准和结构化评估报告来评估提示词行为。

## 快速开始

克隆仓库：

```bash
git clone https://github.com/<your-username>/ai-knowledge-workflows.git
cd ai-knowledge-workflows
```

创建本地 Agent 指令：

```bash
cp agents/AGENTS.example.md AGENTS.md
```

创建本地私有工作区：

```text
local/
├── career-profile.md
├── projects/
├── knowledge/
└── research/
```

复制候选人资料模板：

```bash
cp templates/career-profile.md local/career-profile.md
```

`AGENTS.md`、`local/` 和 `private/` 均由 Git 忽略。

## 提示词设计原则

### 1. 将上下文与指令分离

稳定信息应保存在文件中。

提示词应专注于 Agent 当前需要完成的任务。

### 2. 明确证据要求

提示词应说明什么才算足以支持某项声明的证据。

例如：

```text
Do not infer a skill from a technology being mentioned only once.
```

### 3. 定义输出契约

提示词应明确：

- 必须生成什么；
- 应保存在哪里；
- 哪些内容不得修改；
- 如何表示不确定性。

### 4. 优先采用最小差异更新

文档和知识库工作流应保留有效信息，而不是无必要地重写整个文件。

### 5. 区分事实与分析

研究类提示词应将经过验证的信息与解释和建议分开。

### 6. 面向复用进行设计

只要可能，候选人或项目特定信息都应保留在公共提示词之外。

有关本仓库使用的提示词工程模式，请参阅 `docs/prompt-engineering.md`。

## 隐私模型

公共仓库应仅包含：

- 可复用工作流；
- 通用模板；
- 虚构或匿名化示例；
- 公共文档。

不要提交：

- 包含私人信息的简历；
- 求职申请历史；
- 私有研究报告；
- 应保持私密的内部项目笔记；
- API key；
- token；
- 密码；
- 机器特定的秘密信息。

## 当前状态

**状态：v1 已完成——持续维护，并扩展了基于证据的求职申请工作流和仓库通用化工作流。**

### 职业发展
- [x] 实习岗位研究

### 求职申请
- [x] 基于证据的申请材料准备
- [x] 简历复用 / 调整 / 创建决策

### 项目
- [x] 添加项目
- [x] 更新项目
- [x] 评估项目

### 知识
- [x] 提取知识
- [x] 整合知识
- [x] 审计知识库

### 技能
- [x] 评估已证明的技能
- [x] 将技能与项目同步
- [x] 跨项目能力分析

### 文档
- [x] 更新 README
- [x] 更新项目文档
- [x] 审计仓库文档
- [x] 将私有或本地仓库通用化

### 作品集
- [x] 作品集同步工作流

### 提示词评估
- [x] 提示词评估案例、评分标准和定性结果

## 可选扩展

以下内容为可选项，不属于 v1 范围：

- [ ] 模型间输出比较

## 许可证

[MIT License](LICENSE)
