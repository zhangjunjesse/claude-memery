---
paths: ["app/api/**/*.ts", "src/api/**/*.ts"]
---

# API 路由规则

## 错误处理

- 所有 API 必须有 try-catch 错误处理
- 返回统一的 JSON 格式

## 响应格式

```typescript
// 成功响应
{
  "success": true,
  "data": { ... }
}

// 错误响应
{
  "success": false,
  "error": {
    "code": "ERROR_CODE",
    "message": "错误描述"
  }
}
```

## 参数验证

- 使用 zod 验证请求参数
- 验证失败返回 400 状态码

## 示例

```typescript
import { z } from 'zod'

const schema = z.object({
  name: z.string(),
  email: z.string().email()
})

export async function POST(req: Request) {
  try {
    const body = await req.json()
    const data = schema.parse(body)

    // 处理逻辑

    return Response.json({ success: true, data })
  } catch (error) {
    return Response.json(
      { success: false, error: { message: error.message } },
      { status: 400 }
    )
  }
}
```
