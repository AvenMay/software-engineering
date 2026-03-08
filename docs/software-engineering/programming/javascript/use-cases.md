# Use-Cases

## Web-Browser

- [Web Browser](/internet-system/application-system/web-client/web-browser/)

## Server/Desktop

### Runtimes

- [Node.js](https://nodejs.org/)
    - npm
    - pnpm
    - yarn
- [Bun](https://bun.com/)
- [Deno](https://deno.com/)

------

### CLI/TUI Programming

- Commander.js
- yargs

- TUI
    - Blessed
    - Inquirer
    - Ora
    - Prompt Toolkit
    - Terminal Kit

------

### GUI Programming

- Electron
- NW.js
- React-Native

------

### Network Programming

- [Node.js Docs](https://nodejs.org/docs/latest/api/)
- [深入浅出Node.js.pdf]({{ files_server }}/software-engineering/programming/javascript/%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BANode.js.pdf)

------

### Web/API Application Server

- Auth
    - Auth0
    - Kinde Auth
    - NextAuth.js
    - Passport.js

- ORM
    - Drizzle-ORM

- Frameworks
    - Express.js
    - Koa.js
    - NestJS
    - Hono

- Schema-Validation
    - Ajv
    - Joi
    - Superstruct
    - Validator.js
    - Yup
    - Zod

- SSR-SSR-Frameworks
    - Next.js
    - Nuxt.js

------

### Monitoring

------

### Testing

------

### Scripting

------

### Cryptography

------

## Edge Computing

------

### Edge-Runtimes

- Cloudflare Workers
- Vercel Edge Runtime
- Deno Deploy
- WasmEdge
- CDN 逻辑增强
    - 智能缓存策略（动态 TTL、个性化缓存）
    - 动态图片/内容裁剪与压缩
    - URL 重写、缓存 Key 定制
      - 👉 比纯 CDN 更灵活，可写逻辑进行缓存分析与命中优化

- API 前置层（API Gateway on Edge）
    - 请求路由 / 聚合 / 转发
    - Webhook 预处理
    - Header 增减与协议转换（REST ↔ GraphQL）
    - 负载均衡、A/B 实验、灰度发布
      - 👉 将一部分服务逻辑前移，减少回源压力

- Proxy / 安全访问控制
    - Auth 验证（JWT / OAuth）
    - DDoS & Bot Filter 初步筛选
    - IP / 地区访问控制
    - Rate Limiting 限流
    - 隐藏源站（作为反向代理）
    - 👉 提前阻挡恶意流量，保护后端

- 个性化内容与边缘渲染
    - 对用户地区 / Cookie / Device 做实时裁剪
    - A/B 测试和实验投放
    - 静态站点的边缘 SSR（如 Next.js Edge）
    - Landing page 个性化（营销场景）
    - 👉 动态但低延迟的内容定制

- 隐私计算与数据分散
    - 用户数据就近处理（隐私优先）
    - 边缘缓存 + K/V 存储（Cloudflare KV / Durable Objects）
    - 地域合规处理：数据不跨出区域
    - 👉 常用于 GDPR、跨区存储敏感数据

- IoT & 实时流数据处理（轻量 JS）
    - 本地协议转换（MQTT → HTTP）
    - 实时预处理后送回云端
    - 数据过滤、降采样
    - 👉 JS + 小型 Wasm 模块加速：适合工业/零售边缘节点

- 多媒体近边缘处理
    - 视频预裁剪／水印
    - 音频转码（轻量场景）
    - 图片智能处理（WebP/AVIF）
    - 👉 降低带宽消耗、提升页面加载速度

- 电商 / 广告实时逻辑
    - 实时定价、推荐、优惠计算
    - 风控模型本地判断（小模型）
    - Anti-fraud 校验前置
    - 👉 降低延迟对转化率非常关键

- WebAssembly 扩展的高性能任务
    - 小型 AI 推理
    - 正则/压缩/加密加速
    - 金融运算安全沙箱
    - 👉 JS + WASM 在边缘是趋势（更快、更安全）

------

## Embedded

- Espruino
- JerryScript
- Duktape
- Duktape