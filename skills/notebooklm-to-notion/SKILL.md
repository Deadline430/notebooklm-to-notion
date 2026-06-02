---
name: notebooklm-to-notion
description: Use when turning selected NotebookLM notebook materials, course lessons, book chapters, PDFs, transcripts, or readings into structured study notes in Notion, especially when the user also wants Chinese deep dive audio overviews.
---

# NotebookLM to Notion

## Overview

Use this workflow to convert selected NotebookLM materials into reusable learning artifacts: source-grounded study notes, matching Notion lesson pages, and Chinese deep dive audio overviews.

Prefer this skill when the user provides a course, lesson number, book chapter, notebook title, source names, or a Notion parent page for organized study notes.

## Required Context

Before writing anything to Notion or generating audio, identify:

- NotebookLM notebook title or ID.
- Source materials to use, such as transcript source, PDF source, lesson number, chapter number, or selected source IDs.
- Notion parent page title or ID.
- Desired output language. Default notes are bilingual English-Chinese; default audio is Chinese.
- Whether to create new child pages or update existing lesson pages. If unclear, inspect the Notion parent page first and follow its existing structure.

## Workflow

1. **Inspect NotebookLM**
   - List or fetch the notebook if the ID is unknown.
   - List sources when source selection is unclear.
   - Restrict queries to the relevant source IDs whenever possible.

2. **Inspect Notion**
   - Fetch the parent page before editing.
   - Check whether existing pages are organized by lesson, chapter, topic, or date.
   - Preserve existing structure; create sibling lesson pages when the parent already contains lesson child pages.

3. **Generate Structured Notes**
   - Query NotebookLM using the prompt pattern in `references/prompts.md`.
   - For long outputs, use asynchronous query tools and poll until complete.
   - Keep claims source-grounded. Do not add outside knowledge unless the user explicitly asks for it.

4. **Create or Update Notion Pages**
   - Use Notion create/update tools, not browser copy-paste, when MCP tools are available.
   - Put the page title in Notion page properties, not duplicated as the first heading.
   - Use the existing page style. For lesson pages, the default structure is:
     - `### 1. Lesson Overview (课程概述)`
     - `### 2. Core Concept Glossary (核心概念)`
     - `### 3. Major Theories & Analogies (主要理论与类比)`
     - `### 4. Defects & Discussion Points (局限与讨论点)`
     - `### 5. Study Key Points (学习要点)`

5. **Generate Chinese Deep Dive Audio**
   - Use NotebookLM Studio audio generation when available.
   - Create one audio overview per lesson/chapter bundle unless the user requests a combined episode.
   - Title artifacts consistently, for example:
     - `Week 3 Lecture + Textbook Chapter 4 中文 Deep Dive Audio`
     - `Research Paper + Lecture Notes 中文 Deep Dive Audio`
   - Prompt for Chinese, long-form, source-grounded discussion with clear explanations and review emphasis.
   - Poll status until completed or error. Report artifact URLs/status in the final response.

6. **Verify**
   - Fetch the Notion parent page after writing and confirm new pages are linked under the parent.
   - Fetch each created/updated page enough to confirm content exists.
   - Check NotebookLM audio artifact status before claiming completion.

## Output Rules

- Keep Notion pages useful for review, not just summaries.
- Keep professional terms consistent: English term first, Chinese translation in parentheses.
- Explain abstract cognitive science or technical concepts in simple language.
- Keep citations from NotebookLM if returned, but do not invent citation numbers.
- If audio cannot be downloaded because of authentication or signed URL restrictions, still report the completed NotebookLM artifact URL/status and say download was not verified.

## Common Failure Modes

- **Wrong lesson/chapter:** rewrite the prompt to explicitly ignore unrelated lessons and chapters.
- **Notion page mismatch:** fetch the parent and existing lesson pages before creating anything.
- **Overwriting content:** use create child pages or append/update targeted sections; avoid replacing entire parent pages.
- **NotebookLM timeout:** use async query start/status tools for large notebooks.
- **Audio language drift:** explicitly request Mandarin Chinese and a deep dive style in the Studio prompt.

## References

- Read `references/prompts.md` when writing NotebookLM query or audio prompts.
