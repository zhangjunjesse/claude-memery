# 配置文件使用指南

## 配置文件概览

Claude Code 支持多层级配置，从全局到项目到本地。

## 配置层级

```
优先级（从低到高）：
全局 → 项目 → 本地
```

## 主要配置文件

### CLAUDE.md
- **位置**：项目根目录
- **作用**：项目指令和规范
- **示例**：见 `CLAUDE.md.template`

### .claude/rules/
- **位置**：`.claude/rules/`
- **作用**：模块化规则
- **支持路径作用域**

### .claude/skills/
- **位置**：`.claude/skills/`
- **作用**：可重用技能
- **格式**：`skill-name/SKILL.md`

### settings.json
- **位置**：`.claude/settings.json`
- **作用**：权限、环境变量、hooks
- **团队共享**

## 快速开始

1. 复制模板到项目
2. 修改 CLAUDE.md
3. 根据需要添加 rules
4. 提交到版本控制

## 常见问题

**Q: 配置不生效？**
A: 检查文件路径和格式，重启 Claude Code

**Q: 如何调试配置？**
A: 在对话中询问 Claude 是否读取了配置

**Q: 配置冲突怎么办？**
A: 更具体的配置优先级更高
