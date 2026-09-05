# 飞书记录结构

## 默认资源

```text
飞书英语口语练习/
├── 使用说明与资源索引（飞书文档）
├── 每日练习（飞书文件夹）
│   └── YYYY-MM-DD/
│       ├── 对话记录（飞书文档）
│       └── 完整逐字稿（飞书文档）
├── 周复盘（飞书文件夹）
│   └── YYYYMMDD-YYYY（飞书文档）
├── 英语练习数据库（多维表格 Base）
│   ├── 单词本
│   └── 练习记录
└── 英语练习待办（可选飞书任务清单）
```

Keep the summary and raw transcript as separate documents. The transcript is never translated or merged into the summary. The resource-index document stores clickable links to the Base, folders, current weekly review, and optional task list.

## Daily summary document

Use this order:

1. `今日中文记录`, including a link to `完整逐字稿`
2. `练习统计`
3. `情绪标签`
4. `To-do list`, linking any created Feishu tasks
5. `本次英语反馈`
   - `今日待改进`: one-sentence summary, then `你原本说 | 问题在哪 | 错误标签 | 这里可以表达得更好`
   - `今天的进步`: one-sentence summary, then `你的原话 | 进步在哪里 | 进步标签 | 下次怎么继续保持`
6. `今日总结`

Use stable high-level error tags such as `词性`, `动词形式`, `表达简洁`, `词汇搭配`, `动名词`, and `名词复数`. Use stable progress tags such as `主动开口`, `完整表达`, `跟读复述`, `词汇应用`, and `系统表达`. Merge overlapping labels instead of creating overly fine categories.

## Vocabulary Base

Create a table named `单词本` with these stored fields:

| Field | Suggested type | Purpose |
|---|---|---|
| 单词 / 表达 | Text, primary | Word, phrase, or sentence pattern |
| 类型 / 词性 | Single select or text | Reusable language category |
| 中文 | Text | Meaning in context |
| 用法 / 例句 | Text | Example tied to the actual conversation |
| 练习日期 | Date | Session date |
| 掌握状态 | Single select | 待复习 / 学习中 / 已掌握 |
| 来源文档 | URL | Daily summary link |

Before writing, resolve the real Base token and table ID, then read the actual field structure. Upsert on the combination of `单词 / 表达` and context when practical; do not create duplicate records because of a retry.

Create a `练习记录` table with: `日期`, `主题`, `练习时长`, `新表达数量`, `情绪标签`, `待改进标签`, `进步标签`, and `对话记录链接`. Use it for weekly aggregation; do not duplicate the full transcript in Base.

## Feishu tasks

Use an optional task list named `英语练习待办`. Each task should contain a concrete action, and may include its source daily-document URL. Keep reflective notes and vague intentions in the daily summary instead of turning them into tasks.

## Weekly review document

Use this order:

1. `本周情绪`: date, emoji, mood tags, topic tags, and what helped
2. `本周英语回考`: questions first, answers clearly separated below
3. `本周英语复盘`: improvement and progress sections each use `标签 → 一句话小结 → 表格`
4. `本周 To-do check`: done, unfinished, and carry-forward action, linking Feishu tasks
5. `本周总结`: overall feeling, progress, and reflection
6. `下周两个重点`: one language focus and one life/work focus
