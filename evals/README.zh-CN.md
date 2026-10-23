[English](README.md) | [Français](README.fr.md) | [简体中文](README.zh-CN.md)

[项目 README](../README.zh-CN.md)

<a id="prompt-evaluation-benchmarks"></a>
# 提示评估基准

本目录定义了本仓库中提示工作流的轻量级评估案例。

目标是使提示变更可审查且可量化，而不是仅依赖主观感受。

<a id="evaluation-flow"></a>
## 评估流程

```text
Prompt
  ↓
Evaluation case
  ↓
Agent / model output
  ↓
Evaluation rubric
  ↓
Evaluation report
  ↓
Comparison with previous prompt version
```

<a id="what-can-be-evaluated"></a>
## 可以评估什么？

示例包括：

- 项目更新提示；
- 技能评估提示；
- 文档更新提示；
- 职业研究提示；
- 知识库维护提示。

<a id="directory-structure"></a>
## 目录结构

```text
evals/
├── README.md
├── rubrics/
│   └── prompt-evaluation-rubric.md
├── templates/
│   └── evaluation-report.md
├── cases/
│   ├── application-preparation.md
│   ├── project-update.md
│   ├── skill-evaluation.md
│   └── documentation-update.md
└── results/
    ├── application-preparation.md
    ├── project-update.md
    ├── skill-evaluation.md
    └── documentation-update.md
```

<a id="evaluation-principles"></a>
## 评估原则

<a id="use-representative-tasks"></a>
### 使用代表性任务

评估案例应反映真实工作流中的失败情况或反复出现的任务。

不要创建比实际使用更容易的人为测试。

<a id="keep-evaluation-inputs-stable"></a>
### 保持评估输入稳定

在比较不同提示版本时，尽可能使用相同的案例。

同时改变提示和测试案例会使比较变得不具参考价值。

<a id="separate-prompt-quality-from-model-capability"></a>
### 将提示质量与模型能力分开

记录每次运行所使用的模型。

更强模型产生的更好结果，并不必然说明提示得到了改进。

<a id="penalize-unsupported-claims"></a>
### 惩罚不支持的断言

如果答案流畅但编造了信息，则不能认为是好的答案。

可验证性是核心标准。

<a id="prefer-behavioral-evaluation"></a>
### 优先进行行为评估

评估输出实际行为：

- 是否遵循约束？
- 是否保留了正确内容？
- 是否避免了不支持的断言？
- 是否生成了请求的结构？

<a id="running-an-evaluation"></a>
## 运行评估

1. 选择一个要评估的提示。
2. 在 `evals/cases/` 下选择匹配的案例。
3. 使用案例输入运行提示。
4. 使用 `evals/rubrics/prompt-evaluation-rubric.md` 评分输出。
5. 使用 `evals/templates/evaluation-report.md` 记录结果。
6. 如有可用的先前版本，与之进行比较。

<a id="comparing-prompt-versions"></a>
## 比较提示版本

提示变更应理想情况下在一项或多项维度上得到改善，同时不会在其他地方引发退化。

示例：

```text
Prompt v1
vs
Prompt v2
```

或：

```text
with AGENTS.md
vs
without AGENTS.md
```

或：

```text
Model A
vs
Model B
```

<a id="regression"></a>
## 退化

当新版本提示在现有评估案例上表现显著变差时，即发生退化。

示例：

- 引入了不支持的断言；
- 忽略了之前被尊重的约束；
- 不必要的重写文件；
- 丢失了必需的输出结构；
- 遗漏了重要证据。

<a id="current-benchmark-scope"></a>
## 当前基准范围

当前的手动基准集包括以下案例和定性结果：

- 应用准备和简历决策；
- 项目更新；
- 技能评估；
- 文档更新。

可能的额外案例可涵盖：

- 实习研究；
- 知识提取；
- 投资组合同步；
- 仓库泛化；
- 跨项目能力分析。

<a id="optional-automation"></a>
## 可选自动化

该框架故意设计为手动且轻量级。`evals/results/`中的报告应用了共享的评分标准，但不声称对模型性能的测量或跨模型可重现性。

可能的未来扩展：

```text
evals/
├── scripts/
└── datasets/
```

只有在评估标准和案例在反复的手动运行中被证明有用之后，才应添加自动化。
