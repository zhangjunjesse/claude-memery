# Claude Code 配置模板

> Claude Code 全局和项目级配置模板

## 简介

提供 Claude Code 的配置模板：
- **全局配置** (`~/.claude/`) - 个人偏好和通用规则
- **项目配置** (`.claude/`) - 项目特定的规则和工具

## 目录结构

```
.
├── global/                     # 全局配置模板 (~/.claude/)
│   ├── CLAUDE.md.template     # 全局个人偏好
│   └── .claude/
│       ├── settings.json.template
│       ├── rules/             # 通用代码规则
│       ├── commands/          # 全局命令
│       ├── skills/            # 全局技能
│       └── agents/            # 全局代理
└── project/                   # 项目配置模板 (.claude/)
    ├── CLAUDE.md.template     # 项目说明
    └── .claude/
        ├── settings.json.template
        ├── rules/             # 项目规则
        ├── commands/          # 项目命令
        ├── skills/            # 项目技能
        └── agents/            # 项目代理
```

## 使用方法

### 全局配置

```bash
# 复制到用户目录
cp global/CLAUDE.md.template ~/.claude/CLAUDE.md
cp global/.claude/settings.json.template ~/.claude/settings.json
cp -r global/.claude/rules ~/.claude/

# 根据个人偏好修改
```

### 项目配置

```bash
# 复制到项目目录
cp project/CLAUDE.md.template your-project/CLAUDE.md
cp -r project/.claude your-project/

# 根据项目需求修改
```

## Auto Memory

Claude 会自动在 `~/.claude/projects/<project-hash>/memory/MEMORY.md` 保存项目记忆。

**位置说明**：
- 不在项目目录的 `.claude/` 里
- 由 Claude 自动管理，路径基于项目哈希值
- 前 200 行自动加载到上下文

**使用方式**：
- 明确说"记住..."触发保存
- 使用 `/memory` 命令查看
- 直接编辑文件管理记忆

详见：[docs/memory-guide.md](./docs/memory-guide.md)

## 许可

MIT
