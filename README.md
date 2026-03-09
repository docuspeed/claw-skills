# claw-skills

OpenClaw 的 skills 集合，由 DocuSpeed 维护。

## Skills 列表

| Skill | 描述 |
|-------|------|
| [interdisciplinary-research](./interdisciplinary-research/SKILL.md) | 跨学科专家研究方法。描述如何从网上的信息去采集、分析最靠谱、最真实的数据并进行分析研究的方法论框架。 |

## 目录结构

每个 skill 是一个独立目录，基本结构如下：

```
<skill-name>/
├── SKILL.md          # 必需，skill 定义文件
├── scripts/          # 可选，辅助脚本
├── references/       # 可选，参考资料/文献
└── assets/           # 可选，图片等静态资源
```

`SKILL.md` 需包含 YAML frontmatter（`name` 和 `description` 字段）及正文内容。详见 [AGENTS.md](./AGENTS.md)。

## 安装到 OpenClaw

将本仓库中的 skill 目录复制到 OpenClaw 的 skills 路径下即可使用：

- 全局安装：复制 skill 目录到 `~/.openclaw/skills/`
- 工作区安装：复制 skill 目录到 OpenClaw 当前工作区根目录下（workspace skill，优先级高于全局和内置 skill）

例如安装 `interdisciplinary-research`：

```bash
# 全局安装
cp -r interdisciplinary-research ~/.openclaw/skills/

# 或工作区安装
cp -r interdisciplinary-research /path/to/your/workspace/
```

## 添加新 Skill

1. 创建以 skill 名称命名的目录（小写英文 + 连字符）
2. 在目录内创建 `SKILL.md`，遵循格式规范
3. 提交 PR

## License

[MIT](./LICENSE) © DocuSpeed
