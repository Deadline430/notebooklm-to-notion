# Prompt Templates

## Structured Bilingual Learning Notes

Use this template for each lesson/chapter bundle. Replace bracketed fields.

```text
You are a tutor for [COURSE_NAME]. Summarize [LESSON_NAME_OR_NUMBER] based only on the selected [TRANSCRIPT_SOURCE_DESCRIPTION] and [BOOK_CHAPTER_DESCRIPTION]. Ignore unrelated lessons and chapters except where the selected material itself explicitly refers to them.

Make a bilingual English-Chinese summary for learning and review. Follow the structure below, and keep professional terms consistent in both languages:

1. Lesson Overview (课程概述): Lesson title, main topic, and overall content arrangement. Provide English + Chinese.
2. Core Concept Glossary (核心概念): List every key term, with English term + Chinese translation + simple explanation in both English and Chinese.
3. Major Theories & Analogies (主要理论与类比): Explain all theories, hypotheses, models, mechanisms, examples, and analogies in this lesson/chapter with bilingual descriptions.
4. Defects & Discussion Points (局限与讨论点): Explain limitations, problems, open questions, and debates of the theories/analogies in both languages.
5. Study Key Points (学习要点): Concise bilingual takeaways for memorization.

Format neatly for insertion into Notion. Explain abstract professional knowledge in simple words. Only use information from the uploaded files.
```

## Chinese Deep Dive Audio Overview

Use this template for NotebookLM Studio audio generation.

```text
请基于选定材料生成一段中文 Deep Dive Audio Overview，用于课程复习和深入理解。

范围：
- 课程：[COURSE_NAME]
- 课程材料：[LESSON_NAME_OR_NUMBER]
- 阅读材料：[BOOK_CHAPTER_DESCRIPTION]

要求：
- 使用中文普通话表达。
- 只使用 NotebookLM 中已上传/选定的资料，不加入外部知识。
- 采用深入讲解风格，不要只是短摘要。
- 先说明本课主题和知识脉络，再解释核心概念、主要理论、关键例子/类比、局限与争议。
- 对抽象概念使用通俗解释，但保留英文专业术语并给出中文翻译。
- 强调考试/复习时应该记住的要点。
- 适合长时间深度学习，不要过短。
```

## Final Response Checklist

After completing the workflow, report:

- NotebookLM notebook used.
- Notion parent page used.
- Created/updated Notion page links.
- Audio artifact titles and completion status.
- Any limitations, such as audio download not verified.
