[English](project-update.md) | [Français](project-update.fr.md) | [简体中文](project-update.zh-CN.md)

[项目 README](../../README.zh-CN.md)

<a id="evaluation-case--project-update"></a>
# 评估案例 - 项目更新

<a id="workflow-under-test"></a>
## 待测试的工作流

```text
prompts/project/update-project.md
```

<a id="purpose"></a>
## 目的

评估工作流是否能正确更新项目档案，同时保留有效信息并避免提出未经支持的断言。

<a id="existing-project-profile"></a>
## 现有项目档案

```markdown
# Project Profile

## Identity

- Name: ExampleGuard
- Status: active

## Objective

Analyze game replay data to identify suspicious player behavior.

## Current state

The project parses replay files and extracts shot and hit events.

## Technologies

- Python

## Milestones

### Completed

- Replay parsing
- Shot extraction

### Planned

- Aim feature extraction
- Anomaly detection
```

<a id="new-repository-evidence"></a>
## 新仓库证据

仓库现在包含：

```text
src/features/aim.py
tests/test_aim_features.py
```

实现内容：

- 在每次射击前计算角度移动；
- 计算目标距离；
- 通过了新的单元测试。

仓库中**不包含**异常检测功能。

<a id="expected-behavior"></a>
## 预期行为

高质量的输出应：

- 保留原有的目标；
- 保留回放解析和射击提取功能；
- 增加已实现的瞄准特征提取功能；
- 在必要时提及测试结果；
- 将瞄准特征提取功能移出计划工作内容；
- 保留异常检测功能的计划；
- 避免声称异常检测功能已实现；
- 避免重写无关部分。

<a id="failure-examples"></a>
## 失败示例

以下内容应降低评分：

- 声称已实现异常检测功能；
- 删除有效的现有里程碑；
- 添加未经验证的技术；
- 不必要的重写整个档案；
- 在无证据的情况下更改项目状态。
