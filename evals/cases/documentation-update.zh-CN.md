[English](documentation-update.md) | [Français](documentation-update.fr.md) | [简体中文](documentation-update.zh-CN.md)

[项目 README](../../README.zh-CN.md)

<a id="evaluation-case--documentation-update"></a>
# 评估案例 - 文档更新

<a id="workflow-under-test"></a>
## 待测试的工作流

```text
prompts/documentation/update-project-doc.md
```

<a id="purpose"></a>
## 目的

评估工作流在更新技术文档时是否能准确反映变更，同时保留现有有效内容。

<a id="existing-documentation"></a>
## 现有文档

```markdown
# Example Project

## Current features

- CSV dataset loading
- Data preprocessing
- Logistic regression baseline

## Usage

Run:

python train.py

## Roadmap

- Random Forest model
- REST API
- Docker deployment
```

<a id="new-repository-state"></a>
## 新仓库状态

仓库现在包含：

```text
models/random_forest.py
tests/test_random_forest.py
```

随机森林实现已完成且测试通过。

没有 REST API。

没有 Docker 配置。

`train.py` 命令仍然有效。

<a id="expected-behavior"></a>
## 预期行为

输出应：

- 保留 CSV 加载；
- 保留预处理步骤；
- 保留逻辑回归基准模型；
- 保留有效的 `python train.py` 命令；
- 将随机森林添加到当前功能列表中；
- 从路线图中移除随机森林；
- 保留 REST API 在路线图中的位置；
- 保留 Docker 部署在路线图中的位置；
- 避免声称 API 或 Docker 功能已存在；
- 避免重写与之无关的文档。

<a id="failure-examples"></a>
## 失败示例

以下情况应降低评分：

- 记录 REST 端点；
- 添加 Docker 命令；
- 删除逻辑回归基准模型；
- 更改有效使用命令；
- 不必要的整体替换文档。
