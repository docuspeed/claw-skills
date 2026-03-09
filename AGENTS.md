# AGENTS.md

本仓库是 OpenClaw 的 skills 集合（claw-skills），由 DocuSpeed 维护。

## 项目结构

```
claw-skills/
├── AGENTS.md
├── LICENSE
├── README.md
├── .gitignore
└── <skill-name>/
    ├── SKILL.md          # 必需，skill 定义文件
    ├── scripts/          # 可选，辅助脚本
    ├── references/       # 可选，参考资料/文献
    └── assets/           # 可选，图片等静态资源
```

每个 skill 是一个独立目录，目录名即 skill 名称（使用小写英文 + 连字符命名）。目录内必须包含 `SKILL.md` 文件，可选包含 `scripts/`、`references/`、`assets/` 等子目录。

## SKILL.md 格式规范

每个 `SKILL.md` 必须包含 YAML frontmatter 和正文：

```markdown
---
name: skill-name
description: 简短描述该 skill 的用途
---

# Skill 标题

正文内容...
```

- `name`：与目录名一致
- `description`：一句话描述 skill 功能
- 正文：skill 的完整定义与规则

## 贡献新 Skill

1. 在仓库根目录创建以 skill 名称命名的新目录
2. 在目录内创建 `SKILL.md`，遵循上述格式规范
3. 提交 PR 并确保 frontmatter 格式正确
