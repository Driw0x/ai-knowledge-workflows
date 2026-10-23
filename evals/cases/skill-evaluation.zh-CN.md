[English](skill-evaluation.md) | [Français](skill-evaluation.fr.md) | [简体中文](skill-evaluation.zh-CN.md)

[项目 README](../../README.zh-CN.md)

<a id="evaluation-case--skill-evaluation"></a>
# 评估案例 - 技能评估

<a id="workflows-under-test"></a>
## 待测试的工作流

主要:

```text
prompts/skills/evaluate-skills.md
```

可选:

```text
prompts/skills/cross-project-competency-analysis.md
```

<a id="purpose"></a>
## 目的

评估工作流是否能够区分强、集中、弱和无依据的技能证据。

<a id="evidence"></a>
## 证据

<a id="project-alpha"></a>
### 项目Alpha

- Python应用程序
- PyTorch模型训练
- 数据预处理的单元测试
- 记录的训练结果

<a id="project-beta"></a>
### 项目Beta

- Python应用程序
- scikit-learn分类流水线
- 特征工程
- 交叉验证评估

<a id="project-gamma"></a>
### 项目Gamma

- TypeScript前端
- React组件
- 无后端部署

<a id="skills-to-assess"></a>
## 需评估的技能

- Python
- PyTorch
- scikit-learn
- 机器学习
- React
- Docker
- Kubernetes

<a id="expected-behavior"></a>
## 预期行为

一个强输出应得出大约如下结论：

<a id="python"></a>
### Python

在多个独立项目中均有强有力证据。

<a id="machine-learning"></a>
### 机器学习

在Alpha和Beta项目中均有强有力且分散的证据。

<a id="pytorch"></a>
### PyT及

来自Alpha项目的强有力但集中证据。

<a id="scikit-learn"></a>
### scikit-learn

根据具体评分标准，来自Beta项目的中等或较强但集中的证据。

<a id="react"></a>
### React

已展示，但主要集中在Gamma项目中。

<a id="docker"></a>
### Docker

无支持证据。

<a id="kubernetes"></a>
### Kubernetes

无支持证据。

<a id="failure-examples"></a>
## 失败示例

以下情况应降低评分：

- 因项目为软件项目而声称Docker支持；
- 在无证据情况下声称Kubernetes支持；
- 将列出的每项技术视为同等强度；
- 忽略Python和机器学习的跨项目证据；
- 将PyTorch评为在多个项目中分布。
