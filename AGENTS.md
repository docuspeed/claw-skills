# AGENTS.md

本仓库是一些可用于 OpenClaw 的有趣且实用的 skills 集合（claw-skills），由七转科技维护。

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

## 发版流程

本仓库使用日期版本号（如 `v2026.04.03`），通过 GitHub Releases 发布更新。

发版步骤：

1. 确保所有变更已提交到 `master` 分支
2. 创建日期 tag 并推送：
   ```bash
   git tag -a v2026.04.03 -m "发版说明"
   git push origin v2026.04.03
   ```
3. GitHub Actions 会自动创建 Release，并根据两个 tag 之间的 commit 记录生成更新说明。

用户可通过仓库页面 **Watch -> Custom -> Releases** 订阅发版通知。
