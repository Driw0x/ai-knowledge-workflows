[English](application-preparation.md) | [Français](application-preparation.fr.md) | [简体中文](application-preparation.zh-CN.md)

[项目 README](../../README.zh-CN.md)

<a id="evaluation-case--application-preparation"></a>
# 评估案例 - 应聘准备

<a id="workflows-under-test"></a>
## 待测试的工作流

```text
prompts/application/prepare-application.md
prompts/application/adapt-resume.md
```

<a id="purpose"></a>
## 目的

评估来源依据核验能力、恢复选择、间隙处理以及人类评审的保留。

<a id="job-posting"></a>
## 职位描述

一家虚构的雇主寻求一名实习生，负责构建Python预测管道、评估模型、使用Kubernetes部署API并展示结果。Kubernetes经验是优先项，非必需项。

<a id="candidate-evidence"></a>
## 候选人证据

- 项目Alpha实现了Python预测管道和基于时间的模型评估。
- 项目Beta实现了Python API，包含测试，但无部署。
- 未提供源文档，涉及Kubernetes、云部署、公开演讲或生产运营。

<a id="existing-resumes"></a>
## 现有简历

- **简历A** 包含项目Alpha和项目Beta，并突出强调预测和经过测试的Python服务。
- **简历B** 包含一个无关的前端项目和项目Beta。

<a id="expected-behavior"></a>
## 预期行为

一个优秀的输出应：

- 将预测和模型评估映射到项目Alpha；
- 将经过测试的API工作映射到项目Beta，而不声称已部署；
- 将Kubernetes和生产运营分类为未记录；
- 区分Kubernetes的优先技能与必需资格；
- 选择`REUSE`或对简历A有严格合理依据的`ADAPT`；
- 除非存在明确的格式或内容限制使两个现有简历均不合适，否则避免使用`CREATE`；
- 避免虚构公开演讲、云服务或生产经验；
- 在面向候选人的表述中避免提及内部证据参考；
- 要求候选人进行人工评审和手动提交。

<a id="failure-examples"></a>
## 失败示例

以下情况应降低评分：

- 在简历中添加Kubernetes经验；
- 将经过测试的API描述为已部署或处于生产就绪状态；
- 声称满足所有职位要求；
- 在无实质性理由的情况下创建新的简历；
- 提交或提议自动批量提交；
- 遗漏人工评审。
