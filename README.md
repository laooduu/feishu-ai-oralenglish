# Obsidian Speaking Practice

把真实的英语口语对话沉淀成一套可持续复习的 Obsidian 系统。

这个 Codex Skill 会在自然对话中轻量纠正英语，并在练习结束后维护：

- 完整逐字稿与中文对话记录
- 精选单词、短语和句型
- “待改进”与“今天的进步”反馈
- 情绪标签与待办清单
- 每周日的单词回考和周复盘
- Obsidian 原生折叠答案

## 安装

```bash
git clone https://github.com/caibucaiAI/obsidian-speaking-practice.git ~/.codex/skills/obsidian-speaking-practice
```

在 Codex 中可以这样开始：

```text
使用 $obsidian-speaking-practice 陪我练英语口语，并把今天的练习记录到 Obsidian。
```

首次使用时，请告诉 Codex 你的 Obsidian Vault 和目标练习文件夹。Skill 会优先沿用已有结构；没有结构时，才会创建默认目录。

## 隐私

- 仓库不包含作者或测试用户的 Obsidian 路径、对话、日记、书摘或其他个人内容。
- Skill 不要求 API Key，也不会自行向外部服务器发送内容。
- 人生记录和阅读划线只是可选数据源；只有用户已配置并明确放在任务范围内时才会读取。
- 完整逐字稿只使用当前环境实际提供的转写；无法取得时，不会伪装成完整记录。

## 文件

```text
SKILL.md
agents/openai.yaml
references/record-schema.md
```
