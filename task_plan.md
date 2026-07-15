# 任务计划

## 目标

基于 cc-connect 内置 Web 管理端完成可推送到 Fork 的手机端适配，使手机端和 IM 平台共用项目、会话、Agent 适配器、模型、附件及任务生命周期。

## 阶段

- [已完成] 从 GitHub 上游建立正式本地仓库，并创建手机端特性分支。
- [已完成] 移植已验证的 app-server 事件转发和多浏览器 Bridge 稳定性修复。
- [已完成] 基于既有 Web Admin API 和 Bridge 连接实现手机优先的聊天布局。
- [已完成] 为手机聊天流程添加图片附件输入和项目模型选择。
- [进行中] 构建、测试、整理部署文档，并将用户 Fork 配置为 `origin`。

## 远程策略

- `upstream`: https://github.com/chenhg5/cc-connect.git
- `origin`: https://github.com/lth1040240425/cc-connect.git
- 工作分支：`feature/mobile-web-adapter`。
