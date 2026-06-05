# Axon Skill Templates

Skill 模板库，为 [Axon](https://github.com/a1ickgu0/chrAIExtension) AI 助手提供结构化的 Prompt 能力。

## 什么是 Skill？

Skill 是一种结构化的 Prompt 模板，引导 AI 以一致的方式执行特定任务。每个 Skill 定义在一个 `skill.md` 文件中，包含 YAML frontmatter 元数据和详细的执行指令。

## 目录结构

```
skills/
├── manifest.json                    # Skill 清单（分类索引）
├── README.md                        # 本文件
│
├── reading/                         # 阅读类分类
│   ├── _category.md                 # 分类说明（不可调用）
│   ├── paper-analysis/              # 论文阅读与应用洞察
│   │   └── skill.md
│   ├── news-briefing/               # 新闻简报生成
│   │   └── skill.md
│   └── industry-intelligence/       # 行业技术情报顾问
│       └── skill.md
│
├── project/                         # 项目类分类
│   ├── _category.md                 # 分类说明
│   └── comprehensive-analysis/      # 项目综合分析
│       └── skill.md
│
└── templates/                       # 模板资源（非 Skill）
    ├── paper-note.md                # 论文阅读笔记模板
    └── project-checklist.md         # 项目管理检查清单
```

## Skill 清单

### 阅读类 Skills

| Skill | 说明 | 级别 |
|-------|------|------|
| `paper-analysis` | 从产品研发视角解读学术论文，提取技术创新与产品应用机会 | Intermediate |
| `news-briefing` | 从新闻报道中提取核心事实，生成结构化简报 | Basic |
| `industry-intelligence` | 行业报告、技术文章深度分析与咨询建议 | Advanced |

### 项目类 Skills

| Skill | 说明 | 级别 |
|-------|------|------|
| `comprehensive-analysis` | 综合运用 PMBOK、SWEBOK、IPD、CMMI 框架全面分析项目 | Advanced |

## 使用方式

### 通过 Manifest 导入全部

```
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/manifest.json
```

### 导入单个 Skill

```
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/reading/paper-analysis/skill.md
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/project/comprehensive-analysis/skill.md
```

### 导入分类

```
https://github.com/a1ickgu0/myPrompt/tree/main/reading
https://github.com/a1ickgu0/myPrompt/tree/main/project
```

## Skill 开发指南

### 文件命名规范

- **目录名**：小写字母 + 连字符，如 `paper-analysis`、`industry-intelligence`
- **文件名**：统一使用 `skill.md`（小写）
- **分类说明**：使用 `_category.md`（下划线前缀表示不可调用）

### Frontmatter 元数据

```yaml
---
name: skill-name                  # 必须与目录名一致
kind: local-skill
inputMode: page | mixed | chat    # 输入模式
description: 简短描述              # 用于 Skill 列表展示
metadata:
  level: basic | intermediate | advanced
  language: zh | en
  author: Your Name
  version: 1.0.0
  status: active | draft | deprecated
---
```

### 输入模式说明

- `page`：需要页面内容（PDF、网页等）
- `mixed`：可接受页面或对话输入
- `chat`：纯对话模式

## 模板资源

`templates/` 目录包含非 Skill 的参考资源：

- `paper-note.md`：论文阅读笔记空白模板
- `project-checklist.md`：项目管理检查清单

这些文件不可作为 Skill 调用，但可作为工作参考模板使用。

## GitLab 支持

Axon 同时支持 GitLab URL 格式：

```
https://gitlab.com/user/myPrompt/-/raw/main/reading/paper-analysis/skill.md
https://gitlab.com/user/myPrompt/-/tree/main/reading
```

## 贡献指南

欢迎提交 Issue 或 Pull Request 添加新 Skill 或改进现有 Skill。

## 许可证

MIT License