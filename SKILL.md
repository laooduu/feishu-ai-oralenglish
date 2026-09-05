---
name: feishu-ai-oralenglish
description: Run English speaking practice and maintain durable daily records, transcripts, vocabulary review, tasks, and weekly recaps in Feishu.
---

# Feishu AI Oral English

Use this skill when a user wants to practice spoken English through real conversation and keep a review system in Feishu. It covers daily practice records, vocabulary capture, feedback, explicit tasks, and weekly review—not generic translation or unrelated Feishu administration.

## Connect the Feishu system

Before reading or writing, load the relevant `lark-shared`, `lark-doc`, `lark-base`, and, when needed, `lark-task` skills and follow their current authentication, permission, formatting, and confirmation rules. Operate the user's resources as the user identity unless they explicitly request bot identity.

Locate the existing practice documents, vocabulary Base, and optional task list before creating anything. Preserve an existing structure when present. If none exists, initialize the layout in [record schema](references/record-schema.md). Save the returned document URLs, Base token, table ID, and task-list ID for later sessions; never guess identifiers from names.

Optional life-journal or reading-highlight sources may make the daily closing more personal. Read only recent, relevant information that the user has put in scope. Never invent personal history, quotations, or reading connections.

## During the conversation

- Let the user finish thoughts. Correct only important, reusable issues; do not treat pauses, stutters, or normal oral repair as mistakes.
- Quietly collect words, phrases, and sentence patterns the user explicitly asks about or clearly struggles to use. If the user says “record it now,” update the vocabulary Base immediately; otherwise batch the capture at the end.
- Prefer one primary English expression for one Chinese request unless alternatives are needed for meaning or register.
- Be proactive about recording requested language without making the user repeat the instruction.

## Recording mode

When the user says they are recording, rehearsing for a video, or clearly switches into a scripted take, enter recording mode. Do not interrupt, correct, collect vocabulary, or write any of that take into the practice system. Resume normal capture only when the user says the recording is over or explicitly asks to save material from it. If intent is unclear, keep listening rather than guessing that the take belongs in the record.

## Close a daily session

Create or update the day's summary document and separate raw-transcript document, upsert the session's reusable vocabulary into Base, create only the Feishu tasks the user clearly intended as actionable to-dos, and link the artifacts to the current weekly review.

- Preserve the raw transcript exactly as available. Do not translate, polish, remove repetition, or turn English into Chinese. If an exact transcript is unavailable, say so and do not label a reconstruction as complete.
- Structure the daily summary in the order defined by [record schema](references/record-schema.md).
- Begin every improvement and progress section with one concise summary sentence, followed by its supporting table.
- Use emotion tags only when supported by the conversation, including a clearly evident motivational state.
- Keep vocabulary selective when a session is mostly Chinese: store only expressions actually discussed and worth reusing.
- Treat a conversational idea as a Feishu task only when the user clearly states an action or asks to track it. Do not create duplicate tasks on retries; retain the returned task GUID and URL.

## Weekly review

When the user asks to begin a weekly review, open or create the corresponding Feishu document. Put the mood timeline first, then vocabulary retest, English feedback tags, task check, weekly reflection, and two priorities for next week. Generate retest questions from that week's Base records. Place answers in collapsed sections when supported by the document format; otherwise put them under a clearly separated answer section without claiming they are hidden.

Read [record schema](references/record-schema.md) before creating or materially changing the Feishu documents, Base, or task-list structure.
