# Operating Model — smart-read-mcp

**Status:** Bootstrap target  
**Owner:** smart-read-mcp

## Goal

Universal read path for agents — local files and guarded remote URLs resolved into the Smart Reader stack.

## Non-Goals

- Hosted platform services inside this package.
- Frame-by-frame or whole-image generative LLM understanding as default.

## Acceptance (v0.1.0)

- `read_path` ships with schema, handler, tests, and docs.
- Default path works without remote providers or ML model downloads.
- Release gate JSON artifact passes in CI.
