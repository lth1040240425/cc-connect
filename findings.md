# Findings

- Current deployed temporary source came from Gitee release v1.4.1; the formal repository uses newer GitHub `main`.
- The built-in Web Admin previously registered every browser as Bridge platform `web`. Two browser instances then replaced and disconnected each other because the Bridge server keys adapters by platform name.
- cc-connect already provides the reusable layers required by the mobile client: project/session management, model endpoints, Bridge attachments, and Codex app-server support.
- The local Codex app-server does not reliably expose reasoning or token deltas. Mobile UI must only display actual public events and tool activity.
