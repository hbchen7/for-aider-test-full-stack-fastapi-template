# Full Stack FastAPI Template 总结

## 主要技术栈
- 后端：FastAPI + SQLModel + PostgreSQL
- 前端：React + TypeScript + Chakra UI
- 容器化：Docker Compose
- 安全：JWT 认证 + 密码哈希 + 邮件重置
- 测试：Pytest + Playwright E2E 测试
- 部署：Traefik 反向代理 + 自动 HTTPS 证书

## 核心功能
- 交互式 API 文档（Swagger/OpenAPI）
- 暗黑模式支持
- 自动生成前端客户端
- 环境变量配置（.env 文件）
- CI/CD 集成（GitHub Actions）

## 使用方式
1. **直接克隆**：适合公开仓库，可直接使用
2. **私有仓库**：需手动克隆并设置远程仓库
3. **Copier 工具**：支持快速生成项目，自动配置 .env

## 配置要点
- 必须修改的环境变量：`SECRET_KEY`、`FIRST_SUPERUSER_PASSWORD`、`POSTGRES_PASSWORD`
- 可选配置：SMTP 邮件服务器、Sentry DSN
- 密钥生成命令：`python -c "import secrets; print(secrets.token_urlsafe(32))"`

## 部署说明
- Docker Compose 支持开发与生产环境
- Traefik 用于反向代理和负载均衡
- 部署文档详见 [deployment.md](./deployment.md)

## 文档资源
- 后端文档：[backend/README.md](./backend/README.md)
- 前端文档：[frontend/README.md](./frontend/README.md)
- 开发指南：[development.md](./development.md)
- 发布说明：[release-notes.md](./release-notes.md)

## 许可证
- 采用 MIT 开源协议
