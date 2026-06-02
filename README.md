# NotebookLM to Notion

English | [中文](#中文)

A reusable Codex skill for turning selected NotebookLM course materials into structured Notion study pages and Chinese deep dive audio overviews.

## What This Project Does

This project packages a repeatable learning workflow:

1. Select a NotebookLM notebook and specific sources, such as lecture transcripts and book chapters.
2. Generate source-grounded bilingual English-Chinese study notes.
3. Organize the notes under the matching Notion course page.
4. Generate Chinese deep dive audio overviews in NotebookLM Studio.
5. Verify that the Notion pages and audio artifacts were created.

The skill was designed around real coursework workflows such as:

- `Lesson 7 + Thagard Chapter 8`
- `Lesson 8 + Thagard Chapters 9-10`
- `Lesson 9 + Thagard Chapters 11-12`

## Why It Is Useful

Students often move between lecture transcripts, textbook chapters, AI explanations, and personal knowledge bases. This skill turns that process into a structured workflow that Codex can repeat consistently.

It is especially useful for:

- Graduate course review
- Bilingual learning notes
- Structured Notion knowledge bases
- NotebookLM source-grounded summaries
- Chinese audio review material

## Repository Structure

```text
.
├── README.md
├── examples/
│   └── cs6795-workflow.md
└── skills/
    └── notebooklm-to-notion/
        ├── SKILL.md
        └── references/
            └── prompts.md
```

## Installation

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/notebooklm-to-notion ~/.codex/skills/
```

Restart Codex after installing so the skill can be discovered.

## Example Prompt

```text
Use notebooklm-to-notion.

In my NotebookLM notebook "CS6795 Intro to Cog Science", use the course transcript and Thagard book sources.

Create structured bilingual learning notes and Chinese deep dive audio overviews for:
- Lesson 7 + Chapter 8
- Lesson 8 + Chapters 9-10
- Lesson 9 + Chapters 11-12

Save the notes under my Notion page "CS6795 Intro to Cog Science" as lesson child pages.
```

## Tech Stack

- Codex skills
- NotebookLM MCP / NotebookLM Studio
- Notion MCP
- Markdown-based study note generation

## Resume-Friendly Summary

Built a reusable AI workflow skill that integrates NotebookLM and Notion to automate source-grounded learning material generation. The project supports selected-source summarization, bilingual study note creation, Notion knowledge-base organization, and Chinese deep dive audio overview generation.

---

## 中文

一个可复用的 Codex Skill，用于把 NotebookLM 中选定的课程材料转换为结构化 Notion 学习页面，并生成中文 Deep Dive Audio Overview。

## 项目功能

这个项目把学习资料整理流程封装成可重复调用的工作流：

1. 选择 NotebookLM notebook 和指定 sources，例如课程 transcript、PDF、教材章节。
2. 生成基于来源材料的中英双语学习笔记。
3. 将笔记整理到对应的 Notion 课程页面下。
4. 在 NotebookLM Studio 中生成中文 Deep Dive Audio Overview。
5. 回读验证 Notion 页面和音频 artifact 是否创建成功。

这个 Skill 的设计来自真实课程学习场景，例如：

- `Lesson 7 + Thagard Chapter 8`
- `Lesson 8 + Thagard Chapters 9-10`
- `Lesson 9 + Thagard Chapters 11-12`

## 为什么有用

学生经常需要在课程 transcript、教材章节、AI 解释和个人知识库之间来回整理。这个 Skill 将这套流程标准化，让 Codex 可以稳定地重复执行。

它特别适合：

- 研究生课程复习
- 中英双语学习笔记
- Notion 知识库整理
- NotebookLM source-grounded 总结
- 中文音频复习材料生成

## 仓库结构

```text
.
├── README.md
├── examples/
│   └── cs6795-workflow.md
└── skills/
    └── notebooklm-to-notion/
        ├── SKILL.md
        └── references/
            └── prompts.md
```

## 安装方式

将 skill 文件夹复制到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R skills/notebooklm-to-notion ~/.codex/skills/
```

安装后重启 Codex，新的 skill 才会被自动发现。

## 示例 Prompt

```text
Use notebooklm-to-notion.

在我的 NotebookLM notebook "CS6795 Intro to Cog Science" 中，使用课程 transcript 和 Thagard 教材 sources。

为以下内容生成结构化中英双语学习笔记和中文 deep dive audio overview：
- Lesson 7 + Chapter 8
- Lesson 8 + Chapters 9-10
- Lesson 9 + Chapters 11-12

把学习笔记保存到我的 Notion 页面 "CS6795 Intro to Cog Science" 下，作为 lesson 子页面。
```

## 技术栈

- Codex skills
- NotebookLM MCP / NotebookLM Studio
- Notion MCP
- Markdown 学习笔记生成

## 简历描述

构建了一个可复用的 AI 学习工作流 Skill，集成 NotebookLM 与 Notion，用于自动化生成基于来源材料的学习内容。项目支持指定材料总结、中英双语笔记生成、Notion 知识库组织，以及中文 Deep Dive Audio Overview 生成。
