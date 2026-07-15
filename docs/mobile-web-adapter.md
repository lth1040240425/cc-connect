# Mobile Web Adapter

## Purpose

This branch adapts cc-connect's embedded Web Admin for phone use. It is not a separate PWA relay: the mobile UI calls the same management API and Bridge server as the desktop Web Admin and IM platforms.

## Architecture

```text
Phone browser / desktop browser / Feishu
                |
        cc-connect Web Admin + Bridge
                |
             Core Engine
                |
        Codex app-server / other agents
```

The shared Core Engine remains responsible for project routing, session queues, model state, permissions, attachments, and agent execution.

## Scope

- Mobile-first chat layout with a project contact list.
- One project contact maps to the same cc-connect project and session model used by other platforms.
- Image attachment input and preview using Bridge `message.images`.
- Model menu backed by `GET /api/v1/projects/{name}/models` and `POST /api/v1/projects/{name}/model`.
- Real process display from tool and public app-server events only.
- Unique browser Bridge adapter identities so separate tabs or devices do not disconnect one another.

## Non-goals

- Reimplementing the Codex Desktop App.
- Inventing private reasoning content when the upstream app-server does not emit it.
- Replacing the existing Web Admin APIs, Bridge protocol, or IM platform adapters.

## Git Workflow

1. Keep `upstream` pointed at the original GitHub repository.
2. Configure the user's GitHub Fork as `origin`.
3. Make all mobile work on `feature/mobile-web-adapter`.
4. Rebase onto `upstream/main` before opening a pull request.
