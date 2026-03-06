# Claude Code 记忆系统配置模板

> 基于 Claude Code 的记忆系统和配置文件最佳实践

## 简介

这是一个 Claude Code 配置模板仓库，包含：
- 记忆系统使用指南
- 配置文件模板
- 规则文件示例
- 最佳实践

## 使用方法

### 1. 复制配置到你的项目

```bash
# 复制 .claude 目录
cp -r .claude your-project/.claude

# 复制 CLAUDE.md 模板
cp CLAUDE.md.template your-project/CLAUDE.md

# 根据项目需求修改
```

### 2. 自定义配置

编辑 `CLAUDE.md`，填入你的项目信息：
- 技术栈
- 编码规范
- 架构约定

### 3. 使用记忆系统

Claude 会自动：
- 加载 CLAUDE.md 和 rules
- 创建 Auto Memory
- 跨会话记住项目知识

## 目录结构

```
.
├── README.md                    # 本文件
├── CLAUDE.md.template          # CLAUDE.md 模板
├── .claude/
│   ├── rules/                  # 规则文件
│   │   ├── typescript.md
│   │   ├── react.md
│   │   └── api.md
│   └── skills/                 # 技能文件
│       └── best-practices/
└── docs/                       # 文档
    ├── memory-guide.md         # 记忆系统指南
    └── config-guide.md         # 配置指南
```

## 参考文档

- [Claude Code 记忆系统原理](./docs/memory-guide.md)
- [配置文件使用指南](./docs/config-guide.md)

## 许可

MIT
