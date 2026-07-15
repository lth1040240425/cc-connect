# 关键发现

- 当前部署的临时源码来自 Gitee v1.4.1；正式二开仓库基于较新的 GitHub `main`。
- 内置 Web Admin 曾将每个浏览器注册为 Bridge 平台 `web`。Bridge 按平台名保存适配器，因此多个浏览器会互相替换并掉线。
- cc-connect 已具备手机端可复用的项目/会话管理、模型接口、Bridge 附件和 Codex app-server 支持。
- 本机 Codex app-server 不能稳定提供 reasoning 或逐 token 增量。手机 UI 只展示实际公开事件和工具活动。
