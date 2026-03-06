# Claude Code 记忆系统使用指南

## 什么是记忆系统

Claude Code 的记忆系统让 AI 能够跨会话记住项目知识、用户偏好和经验教训。

## 双记忆机制

### 1. 显式记忆（CLAUDE.md）
- 用户手动编写
- 明确的规则和指令
- 团队共享

### 2. 隐式记忆（Auto Memory）
- AI 自动生成
- 观察学习的经验
- 个人使用

## 如何使用

### 触发记忆保存

**明确触发**：
```
"记住我喜欢用 bun 而不是 npm"
"Always use single quotes"
"Never modify package.json"
```

**自动触发**：
- AI 观察重复模式
- 用户纠正 AI 错误
- 解决复杂问题后

### 查看记忆

```bash
# 在 Claude Code 中
/memory
```

### 管理记忆

- 定期审查 `~/.claude/projects/<project>/memory/MEMORY.md`
- 删除过时或错误的记忆
- 手动编辑补充重要信息

## 最佳实践

1. **明确表达偏好** - 使用"记住"、"always"、"never"等关键词
2. **定期审查** - 每周检查一次记忆内容
3. **保持简洁** - CLAUDE.md 控制在 200 行以内
4. **分离关注点** - 使用 rules 目录组织规则

## 参考

- [配置文件清单](../Claude_Code_配置文件清单.md)
- [已验证版文档](../Claude记忆系统_已验证版.md)
