# NotebookLM Learning to Notion

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

Students often need to move between lecture transcripts, textbook chapters, AI-generated explanations, and personal knowledge bases. This skill turns that process into a structured workflow that Codex can repeat consistently.

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
    └── notebooklm-learning-to-notion/
        ├── SKILL.md
        └── references/
            └── prompts.md
```

## Installation

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/notebooklm-learning-to-notion ~/.codex/skills/
```

Restart Codex after installing so the skill can be discovered.

## Example Prompt

```text
Use notebooklm-learning-to-notion.

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
