# Task Plan

## Goal

Fork-ready mobile adaptation of cc-connect's built-in Web Admin so the phone and IM platforms share the same projects, sessions, agent adapters, models, attachments, and task lifecycle.

## Phases

- [completed] Create the formal local Git repository from GitHub upstream and create the mobile feature branch.
- [in_progress] Port verified app-server event forwarding and multi-browser Bridge stability changes.
- [pending] Add a mobile-first chat layout reusing the existing Web Admin APIs and Bridge connection.
- [pending] Add image attachment input and project model selection to the mobile chat flow.
- [pending] Build, test, document deployment and configure the user's GitHub Fork as `origin`.

## Remote Strategy

- `upstream`: https://github.com/chenhg5/cc-connect.git
- `origin`: reserved for the user's GitHub Fork after authorization is available.
- Working branch: `feature/mobile-web-adapter`.
