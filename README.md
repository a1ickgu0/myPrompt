# Axon Skill Templates

This repository contains SKILL templates for [Axon](https://github.com/a1ickgu0/chrAIExtension) - an AI-powered Chrome extension.

## What is a SKILL?

A SKILL is a structured prompt template that guides the AI to perform specific tasks consistently. Each SKILL is defined in a `SKILL.md` file with YAML frontmatter metadata.

## Usage

### Import in Axon Settings

1. Open Axon Settings
2. Go to **Library** > **Skills**
3. Click **Import from URL**
4. Paste one of these URLs:

**Import all skills via manifest:**
```
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/manifest.json
```

**Import by category:**
```
https://github.com/a1ickgu0/myPrompt/tree/main/reading
https://github.com/a1ickgu0/myPrompt/tree/main/project-analysis
```

**Single SKILL:**
```
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/project-analysis/SKILL.md
https://raw.githubusercontent.com/a1ickgu0/myPrompt/main/reading/SKILL.md
```

## Structure

```
myPrompt/
├── manifest.json              # SKILL Hub 清单
├── project-analysis/
│   └── SKILL.md               # 项目综合分析（PMBOK+SWEBOK+IPD+CMMI）
├── reading/
│   ├── SKILL.md               # 阅读类 Skills（自动识别内容类型）
│   ├── paper-analysis/        # 论文解读
│   ├── news-briefing/         # 新闻简报
│   └── technical-doc/         # 技术文档解读
└── references/                 # 参考模板
```

## SKILL List

| Skill | Description | Level | 框架 |
|-------|-------------|-------|------|
| 项目综合分析 | 综合运用 PMBOK、SWEBOK、IPD、CMMI 框架全面分析项目 | Advanced | 四框架整合 |
| 阅读类 Skills | 自动识别内容类型，采用最适合的分析框架 | Intermediate | 多模式 |
| 论文阅读与解读 | 系统性解读学术论文 | Intermediate | 学术框架 |
| 新闻简报生成 | 从新闻中提取核心事实 | Basic | 新闻框架 |
| 技术文档解读 | 解读技术文档和 API 文档 | Intermediate | 技术框架 |

## 项目综合分析 Skill

这是核心 Skill，整合了四大知识体系：

### PMBOK - 项目管理知识体系
十大知识领域：整合、范围、进度、成本、质量、资源、沟通、风险、采购、相关方管理

### SWEBOK - 软件工程知识体系
十五个知识领域：需求、设计、构建、测试、维护、配置管理、工程管理、工程过程、模型与方法、质量等

### IPD - 集成产品开发
六个阶段：概念 → 计划 → 开发 → 验证 → 发布 → 生命周期

### CMMI - 能力成熟度模型集成
五个等级：初始级 → 已管理级 → 已定义级 → 已量化管理级 → 优化级

## GitLab Support

This repository can also be mirrored to GitLab. Axon supports GitLab URL formats:

```
https://gitlab.com/your-username/myPrompt/-/raw/main/project-analysis/SKILL.md
https://gitlab.com/your-username/myPrompt/-/tree/main/reading
```

## Contributing

Feel free to submit issues or pull requests to add new skills or improve existing ones.

## License

MIT License
