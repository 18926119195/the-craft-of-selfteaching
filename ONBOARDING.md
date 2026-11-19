# 《自学是门手艺》入库指南

这是李笑来《自学是门手艺》的教学资料分支。协作者可以从章节导航进入可执行的 Python 示例，沿用现有校对流程。书籍版权与授权见 [README](README.md)，GitHub 上游为 [xiaolai/the-craft-of-selfteaching](https://github.com/xiaolai/the-craft-of-selfteaching)。本次审阅的快照为 [`master` 的 `38b0bca`](https://github.com/18926119195/the-craft-of-selfteaching/commit/38b0bcaed3743fdee25bb5b3d75f522f49a4b93f)。

## 章节入口与目录

| 入口 | 适用场景 |
| --- | --- |
| [README](README.md) 与 [前言](01.preface.ipynb) | 课程顺序、作者说明和阅读边界 |
| [JupyterLab 安装与配置](T-appendix.jupyter-installation-and-setup.ipynb) | 打开仓库根目录中的 `.ipynb`，逐段阅读和运行 |
| [Markdown 目录](markdown/README.md) | 在 GitHub 中阅读正文及定位对应章节 |
| [书稿校对流程](02.proof-of-work.ipynb) | 建立单章节、可复核的 PR |
| [读者来信与笔记](from-readers/) · [学习笔记](my-notes/) | 了解读者实践和笔记，与书稿正文区分归档 |

阅读从 Part 1 的值、流程、函数、字符串和容器进入，再视任务查 Part 2 的函数与测试、Part 3 的类与正则等专题。与 Agent 协作时，可直接提供一个章节路径、一个待查示例及期望输出。

## 开发历程与状态

| 证据时间 | 已有内容 | 边界 |
| --- | --- | --- |
| 2019-03-23，仓库 README 记载 | 增加 Markdown 阅读形式，和根目录的 notebook 章节并行。[README](README.md) · [Markdown 目录](markdown/README.md) | 双形式都可阅读，内容同步需按章节检查。 |
| 2019-06-30 作者日期，2023-05-03 提交日期 | 当前基线修改了 Markdown 字符串章节中示例的排列顺序，让变量的使用位置更清楚。此提交仅改一份文件。[提交差异](https://github.com/18926119195/the-craft-of-selfteaching/commit/38b0bcaed3743fdee25bb5b3d75f522f49a4b93f) · [对应 Notebook](Part.1.E.5.strings.ipynb) | 修改的两种章节表示是否需要对齐，由具体示例的教学意图决定。 |
| 当前基线 | 已有校对教程、读者笔记、Notebook 示例、Markdown 镜像和本地图片。离线解析 47 个 `.ipynb`，首页及 Markdown 目录中核对的 95 个本地章节链接均存在。 | 当前检索范围为默认分支目录、可见提交说明和可见 Issue。未找到此分支的 AI 协作会话，也未发现仓库级 Notebook 全量执行、双格式同步门禁或 Agent 教学产品。Notebook 执行等待按章节验证。 |

## 第一个可验收任务

1. **确定目标。** 选择字符串章节中一个具体例子，写下预期学习结果及其章节位置，为该例子保存当前 Notebook 和 Markdown 的对照片段。
2. **复核表现。** 在干净 Python kernel 运行例子及直接依赖的单元格，记录 Python 版本、预期输出、实测输出和失败位置。对比 Markdown 与 Notebook 的变量、调用顺序和旁注。
3. **控制改动范围。** 校对 PR 引用原章节位置与运行证据。涉及书稿改作或分发时，先依据 README 所列授权与维护方确认可采用的校对方式。
4. **引入反馈。** 建议验收门槛为本次涉及的相对链接全部解析、对应代码示例结果一致、人工复核通过。发现差异时保留最小可复现例，先找源头，修订后重新运行。Agent 可以提出解释和练习提示，由复核者确认书意及输出后纳入协作。

## 方法依据

本指南把总体设计落实为边界、目标和任务接口，把工程控制中的反馈落实为观测、判据和纠偏。维护者用原始协作记录、代码和固定样本共同核验定性判断与量化结果，据此决定下一轮行动。[《工程控制论》](https://openlibrary.org/books/OL49218199M/Engineering_cybernetics) · [《组织管理的技术——系统工程》](https://doi.org/10.13255/j.cnki.jusst.2011.06.020) · [《一个科学新领域——开放的复杂巨系统及其方法论》](https://cnki.istiz.org.cn/kcms/detail/detail.aspx?dbcode=CPFD&dbname=cpfd1999&filename=ZGXC199008001001)
