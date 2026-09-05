# Feishu AI Oral English

把真实的英语口语对话沉淀成一套可持续复习的飞书系统。

这个 Codex Skill 会在自然对话中轻量纠正英语，并在练习结束后维护：

- 飞书对话记录与独立完整逐字稿
- 多维表格中的单词、短语、句型和练习统计
- “待改进”与“今天的进步”反馈
- 情绪标签与明确的飞书任务
- 每周单词回考和周复盘

## 安装

```bash
git clone https://github.com/laooduu/feishu-ai-oralenglish.git ~/.codex/skills/feishu-ai-oralenglish
```

在 Codex 中可以这样开始：

```text
使用 $feishu-ai-oralenglish 陪我练英语口语，并把今天的练习记录到飞书。
```

首次使用需要完成飞书登录和相关权限授权。Skill 会优先沿用已有的飞书文档、Base 和任务清单；没有结构时，才会创建默认资源。

## 默认数据结构

- 每日总结与完整逐字稿：飞书文档
- 单词本与练习统计：飞书多维表格 Base
- 明确可执行的待办：飞书任务
- 周复盘与资源索引：飞书文档

## 隐私

- 仓库不包含用户的飞书链接、token、对话、日记或其他个人内容。
- Skill 不保存飞书密钥；认证由当前环境的飞书工具负责。
- 人生记录和阅读划线只是可选数据源，只有用户放入任务范围时才会读取。
- 完整逐字稿只使用当前环境实际提供的转写；无法取得时，不会伪装成完整记录。

## 文件

```text
SKILL.md
agents/openai.yaml
references/record-schema.md
```
