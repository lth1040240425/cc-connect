# 手机端 Web 适配

## 目标

本分支将 cc-connect 内置 Web Admin 适配为手机端界面。它不是独立 PWA 中转服务：手机界面与桌面 Web Admin、IM 平台共用同一套管理 API 和 Bridge 服务。

## 架构

```text
手机浏览器 / 桌面浏览器 / 飞书
                |
        cc-connect Web Admin + Bridge
                |
             Core Engine
                |
        Codex app-server / other agents
```

共享的 Core Engine 仍负责项目路由、会话队列、模型状态、权限、附件和 Agent 执行。

## 范围

- 使用项目联系人列表的手机优先聊天布局。
- 一个项目联系人对应其他平台使用的同一个 cc-connect 项目和会话模型。
- 使用 Bridge `message.images` 实现图片附件输入与预览。
- 通过 `GET /api/v1/projects/{name}/models` 和 `POST /api/v1/projects/{name}/model` 提供模型菜单。
- 只展示工具和公开 app-server 事件构成的真实过程。
- 为浏览器 Bridge 适配器提供唯一身份，避免不同标签页或设备互相断开连接。

## 不在范围内

- 重新实现 Codex Desktop App。
- 在上游 app-server 未发出事件时编造私有推理内容。
- 替换既有 Web Admin API、Bridge 协议或 IM 平台适配器。

## Git 工作流

1. `upstream` 始终指向原始 GitHub 仓库。
2. 用户 GitHub Fork 配置为 `origin`。
3. 所有手机端改动都在 `feature/mobile-web-adapter` 完成。
4. 发起 Pull Request 前先 rebase 到 `upstream/main`。
