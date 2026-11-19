# 《自学是门手艺》入库指南

[一分钟定位](#一分钟定位) · [沿聊天时间线看灵感](#沿聊天时间线看灵感) · [从代码反查来由](#从代码反查来由) · [走读与维护记录](#走读与维护记录)

## 一分钟定位

这是李笑来《自学是门手艺》的教材分支。根目录有可运行的 Python Notebook，`markdown/` 有供网页阅读的章节，`from-readers/` 和 `my-notes/` 是读者来信与笔记。当前基线为 [`master` 的 `38b0bca`](https://github.com/18926119195/the-craft-of-selfteaching/commit/38b0bcaed3743fdee25bb5b3d75f522f49a4b93f)。上游和书稿授权分别见 [上游项目](https://github.com/xiaolai/the-craft-of-selfteaching) 与 [README](README.md)。

## 沿聊天时间线看灵感

**如何读状态。** 已实现表示在所列版本找到与灵感相符的代码路径。部分实现表示已有其中一段。未实现表示已查的入口尚无对应实现。证据不足时标待确认。归档与设计文稿按资料本身的状态描述。

本库默认分支、可见提交与 Issue 中未定位到仓库主人和 AI 的研发会话。下列时间来自书稿说明和 Git 提交，记录可追溯的编辑决定，原始想法的对话来源仍待确认。

| ID／时间 | 可追溯编辑决定 | 状态 | 文件证据 |
| --- | --- | --- | --- |
| <a name="idea-i01"></a>I01 · 2019-03-23 | README 记载新增 Markdown 阅读形式，读者可在网页直接看章节。[出版说明](README.md) | 已落地 | [Markdown 目录](markdown/README.md) 与 [Notebook 目录](README.md#目录) 对应。 |
| <a name="idea-i02"></a>I02 · 2021-07-04 | 字符串章节经历两个独立的校对改动，Notebook 删掉重复解释，Markdown 调整换行示例的注释摆放。[Notebook 提交](https://github.com/18926119195/the-craft-of-selfteaching/commit/9cbb4d3) · [Markdown 提交](https://github.com/18926119195/the-craft-of-selfteaching/commit/f8a8b83) | 已落地 | [字符串 Notebook](Part.1.E.5.strings.ipynb) 与 [字符串 Markdown](markdown/Part.1.E.5.strings.md) 可分开定位。 |
| <a name="idea-i03"></a>I03 · 2023-05-03 提交，作者日期为 2019-06-30 | 将示例里的字符串赋值放到同组查找调用之前，让读者一眼看到这些方法共用什么输入。[提交说明和差异](https://github.com/18926119195/the-craft-of-selfteaching/commit/38b0bcaed3743fdee25bb5b3d75f522f49a4b93f) | 已落地（该 Markdown 改动） | 当前基线只改 [字符串 Markdown](markdown/Part.1.E.5.strings.md) 的这一处，Notebook 的对应例子独立读取。 |

## 从代码反查来由

| 先看到的文件 | 能查到的来由 |
| --- | --- |
| [字符串 Notebook](Part.1.E.5.strings.ipynb) 与 [字符串 Markdown](markdown/Part.1.E.5.strings.md) | [I01](#idea-i01)–[I03](#idea-i03)。两者是同一章节的两种形式，单次改动可能只出现在其中一份。 |
| [JupyterLab 配置](T-appendix.jupyter-installation-and-setup.ipynb) 与 [校对教程](02.proof-of-work.ipynb) | 分别说明怎样启动阅读环境、怎样提交小范围校改。 |
| [读者来信](from-readers/) 与 [自学笔记](my-notes/) | 能找到读者的学习背景和练习记录。它们与书稿正文分别归档。 |

## 走读与维护记录

第一次读，从 README 进字符串章节，在 Markdown 找到 `str.find()` 的示例，再打开对应 Notebook 的同一节。最后看 [I03](#idea-i03) 的差异，确认哪一行是教学表达上的改动，哪些例子本来就已存在。

本次离线解析 47 个 Notebook 文件，检查两个首页中的 95 个本地章节链接。若发现原始会话或新的校对依据，按 I 编号补时间、章节位置与提交即可。

**指南如何更新。** 以仓库和版本划定范围，从聊天提取原始目标，再用代码与产物校正对当时决策的理解。新证据出现时，回到原编号修订记录。这种读法借鉴了钱学森的系统工程和工程控制论。 [《组织管理的技术——系统工程》](https://doi.org/10.13255/j.cnki.jusst.2011.06.020) · [《工程控制论》](https://openlibrary.org/books/OL49218199M/Engineering_cybernetics)
