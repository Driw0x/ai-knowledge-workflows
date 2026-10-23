[English](prompt-engineering.md) | [Français](prompt-engineering.fr.md) | [简体中文](prompt-engineering.zh-CN.md)

[项目 README](../README.zh-CN.md)

<a id="prompt-engineering-patterns"></a>
# 提示工程模式

本仓库将提示工程作为一种软件设计实践，而非一系列孤立的指令。

<a id="1-context-decomposition"></a>
## 1. 上下文分解

提示中不应包含用户或项目的所有上下文信息。

相反：

```text
AGENTS.md
+ domain knowledge
+ task prompt
+ output template
```

这有助于复用并减少重复。

<a id="2-explicit-evidence-policy"></a>
## 2. 明确的证据政策

提示需定义什么构成证据。

示例：

```text
Do not infer competence from a technology being mentioned only once.
```

这可以减少未经支持的结论。

<a id="3-positive-and-negative-constraints"></a>
## 3. 正向与负向约束

良好的任务提示应明确说明：

- 代理应当执行什么；
- 代理必须避免什么。

示例：

```text
Preserve valid existing content.
Prefer minimal diffs.
Do not document roadmap items as implemented.
```

<a id="4-output-contracts"></a>
## 4. 输出合同

代理被赋予一个目标结构，而非开放式的请求。

示例包括：

- 项目概览；
- 实习研究报告；
- 审计表格。

这使得输出更容易比较、评审和版本控制。

<a id="5-tool-aware-prompting"></a>
## 5. 工具感知提示

研究提示需要当前来源的验证。

仓库提示在信任文档前需进行源代码检查。

因此，提示需反映完成任务所需的能力。

在仓库工作方面，当前实现和可执行测试优先于过时的文档。文档仍具参考价值，但当其与观察到的行为相矛盾时则不再可信。

<a id="6-uncertainty-handling"></a>
## 6. 不确定性处理

工作流指导代理区分：

- 已验证的事实；
- 分析；
- 建议；
- 信息缺失。

这比强制给出确定答案更可靠。

<a id="7-minimal-diff-editing"></a>
## 7. 最小差异编辑

在文档和知识库维护方面，提示明确优先考虑最小变更。

这有助于保留人工编写的内容并减少意外的回归问题。

<a id="8-privacy-aware-prompting"></a>
## 8. 隐私感知提示

可复用的公开提示与私有本地上下文分离。

工作流可以开源，而个人数据仍保留在本地。

<a id="9-versionability"></a>
## 9. 可版本化

提示以文本文件形式存储，并通过 Git 进行版本控制。

因此，变更可以像代码一样被审查：

- 发生了什么变更；
- 为何发生变更；
- 该变更影响哪些工作流行为。

<a id="10-evaluation-oriented-design"></a>
## 10. 面向评估的设计

当质量可以评估时，提示词工作流才能得到更可靠的改进。

本仓库包含：

- 稳定的评估案例；
- 共用的评分标准；
- 定性的结果报告；
- 用于比较提示词行为的回归标准。

该框架保持人工操作和轻量化。模型间比较、自动执行及重复运行一致性测试均为可选扩展，而非 v1 的必要要求。

<a id="11-success-criteria-before-execution"></a>
## 11. 执行前明确成功标准

在实质性变更之前，定义：

- 可观察的结果；
- 必须保持不变的行为和文件；
- 完成前所需的检查项。

这可以防止实现过程事后成为成功的定义。

<a id="12-diagnose-fix-and-verify"></a>
## 12. 诊断、修复和验证

一个可靠的修复工作流是：

```text
reproduce or trace the failure
    ↓
identify the root cause
    ↓
apply a targeted fix
    ↓
run a regression check
    ↓
run broader relevant checks and a smoke test
```

编写变更只是其中一步。工作流不应在相关验证运行之前报告完成。

<a id="13-grounded-generation-pipelines"></a>
## 13. 基于事实的生成管道

当输出包含关于个人、项目或系统的声明时，应使用一个明确的管道：

```text
source facts
    ↓
relevant evidence selection
    ↓
generation
    ↓
claim and output validation
```

模型可以选取、浓缩、组织和重新表述证据。它不得创建缺失的事实、指标、经验或结果。

<a id="14-human-in-the-loop-boundaries"></a>
## 14. 人工介入的边界

高影响的工作流应识别仍需由人类执行的决策。例如，应用工作流可以发现、分析和准备材料，但最终内容的审核和手动提交由候选人完成。

```text
discovery
    ↓
analysis
    ↓
preparation
    ↓
human review
    ↓
manual action
    ↓
tracking
```

<a id="15-reusable-extraction-across-repository-boundaries"></a>
## 15. 跨仓库边界可重用的提取

一个私有源可以不被复制进其中而为公共衍生品提供信息：

```text
private source evidence
    ↓
identify stable reusable rules
    ↓
remove personal and machine-specific context
    ↓
apply the smallest public change
    ↓
validate behavior, links, and privacy
```

源始终保持权威性。衍生品仅暴露外部有用的信息。保持两个仓库中无关的本地变更，绝不使用公共衍生品覆盖私有源的事实。
