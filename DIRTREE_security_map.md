# DIRTREE_security_map

Curated security-relevant map of high-impact paths (entrypoints, Electron boundaries, IPC, agent/tool execution, auth/key handling, network/config/packaging).

Exclusions: build/cache/VCS and binary/media folders/files are omitted because they are generated artifacts or non-source assets with low audit value for code-flow/security review.

## Entrypoints & app bootstrap

- `package.json`
- `pnpm-workspace.yaml`
- `apps/web/package.json`
- `apps/desktop/package.json`
- `packages/agent-core/package.json`
- `apps/web/index.html`
- `apps/desktop/src/main/index.ts`
- `apps/desktop/src/preload/index.ts`

## Electron main/renderer/preload

- `apps/desktop/src/main/`
- `apps/desktop/src/preload/`
- `apps/web/src/client/`

## IPC surface

- `apps/desktop/src/main/ipc/`
- `apps/web/src/client/lib/accomplish.ts`

## Agent core / tools / execution

- `packages/agent-core/src/`
- `packages/agent-core/src/storage/`

## Auth / keys / crypto / storage

- `packages/agent-core/src/storage/`
- `apps/desktop/src/main/services/`

## Network / API / external integrations

- `apps/web/src/client/lib/`
- `apps/desktop/src/main/services/`
- `packages/agent-core/src/providers/`

## Config / CI / release / policies

- `.github/workflows/`
- `.prettierrc`
- `eslint.config.js`
- `docs/architecture.md`

## Installers / packaging

- `apps/desktop/scripts/`
