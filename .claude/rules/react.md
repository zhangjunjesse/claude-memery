# React 规则

## 组件风格

- 使用函数式组件，不使用 class 组件
- 使用 hooks 管理状态
- 组件文件使用 PascalCase 命名

## 状态管理

- 简单状态使用 useState
- 复杂状态使用 useReducer
- 全局状态使用 Context 或状态管理库

## 性能优化

- 使用 React.memo 包裹纯组件
- 使用 useMemo 缓存计算结果
- 使用 useCallback 缓存函数引用

## 示例

```tsx
// ✅ 正确
const UserProfile: React.FC<{ userId: string }> = ({ userId }) => {
  const [user, setUser] = useState<User | null>(null)

  useEffect(() => {
    fetchUser(userId).then(setUser)
  }, [userId])

  return <div>{user?.name}</div>
}

// ❌ 错误
class UserProfile extends React.Component {
  // ...
}
```
