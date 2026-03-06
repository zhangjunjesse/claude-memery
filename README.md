# Claude Code 记忆系统配置模板

> 基于 Claude Code 的记忆系统和配置文件最佳实践

## 简介

这是一个 Claude Code 配置模板仓库，提供：
- **全局配置模板** - 用于 `~/.claude/`
- **项目配置模板** - 用于不同类型项目
- 记忆系统使用指南
- 最佳实践

## 目录结构

```
.
├── global/                     # 全局配置模板
│   ├── CLAUDE.md.template     # 全局个人偏好
│   └── .claude/
│       └── rules/             # 通用规则
├── templates/                  # 项目配置模板
│   ├── react/                 # React 项目
│   ├── nodejs/                # Node.js 后端
│   └── python/                # Python 项目
└── docs/                      # 文档
    ├── memory-guide.md
    └── config-guide.md
```

## 使用方法

### 1. 设置全局配置（可选）

```bash
# 复制全局配置到用户目录
cp global/CLAUDE.md.template ~/.claude/CLAUDE.md
cp -r global/.claude/rules ~/.claude/rules

# 根据个人偏好修改
```

### 2. 设置项目配置

```bash
# 选择合适的模板（react/nodejs/python）
cp -r templates/react/.claude your-project/.claude
cp templates/react/CLAUDE.md.template your-project/CLAUDE.md

# 根据项目需求修改
```

### 3. 使用记忆系统

Claude 会自动：
- 加载全局和项目配置
- 创建 Auto Memory
- 跨会话记住项目知识

## 参考文档

- [Claude Code 记忆系统原理](./docs/memory-guide.md)
- [配置文件使用指南](./docs/config-guide.md)

## 许可

MIT
