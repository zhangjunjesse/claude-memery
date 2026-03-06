# TypeScript 规则

## 类型定义

- 所有函数必须有明确的返回类型
- 使用 interface 定义对象类型（除非需要 union 或 intersection）
- 禁止使用 any，使用 unknown 代替

## 示例

```typescript
// ✅ 正确
function getUserName(id: string): Promise<string> {
  return fetchUser(id).then(user => user.name)
}

// ❌ 错误
function getUserName(id) {
  return fetchUser(id).then(user => user.name)
}
```

## 严格模式

- 启用 strict 模式
- 启用 noImplicitAny
- 启用 strictNullChecks
