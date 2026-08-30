# 记录结构

## 默认目录

```text
英语口语练习/
├── INDEX.md
├── 待办清单.md
├── 单词本/
│   ├── INDEX.md
│   └── YYYY-MM-DD.md
├── 对话记录/
│   └── YYYY-MM-DD/
│       ├── 对话记录.md
│       └── 完整逐字稿.md
└── 周复盘/
    ├── INDEX.md
    └── YYYYMMDD-YYYY.md
```

Keep the daily summary and raw transcript as separate files. The raw transcript is never translated or merged into the summary.

## Daily `对话记录`

Use this order:

1. `今日中文记录`, with a link to `完整逐字稿`
2. `练习统计`
3. `情绪标签`
4. `To-do list`
5. `本次英语反馈`
   - `今日待改进`: one-sentence summary, then a table: `你原本说 | 问题在哪 | 错误标签 | 这里可以表达得更好`
   - `今天的进步`: one-sentence summary, then a table: `你的原话 | 进步在哪里 | 进步标签 | 下次怎么继续保持`
6. `今日总结`

Use stable high-level error tags such as `#英语待改进/词性`, `动词形式`, `表达简洁`, `词汇搭配`, `动名词`, and `名词复数`. Merge overlapping labels rather than creating overly fine categories.

Use stable progress tags such as `#英语进步/主动开口`, `完整表达`, `跟读复述`, `词汇应用`, and `系统表达`.

## Vocabulary notebook

Each date is a table:

`单词 / 表达 | 类型 / 词性 | 中文 | 用法 / 例句`

The master index is reverse chronological. Record words, phrases, and sentence patterns. Keep the translation and example tied to the actual situation in which the user met the expression.

## Weekly review

Use a compact date-range file name. Begin in this order:

1. `本周情绪`: date, emoji, mood tags, topic tags, and what helped.
2. `本周英语回考`: questions first; answers as separate collapsed callouts (`> [!answer]- …`) below the table.
3. `本周英语复盘`: both improvement and progress sections use `标签 → 一句话小结 → 表格`.
4. `本周 To-do check`: done, unfinished, and carry-forward action.
5. `本周总结`: overall feeling, progress, and reflection.
6. `下周两个重点`: one language focus and one life/work focus.

Use mood emoji in weekly review only when they make scanning easier; daily records can use text tags alone.
