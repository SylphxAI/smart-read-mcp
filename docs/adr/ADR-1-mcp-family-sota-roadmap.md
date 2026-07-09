# ADR-1: Adopt Smart Read MCP Family SOTA Roadmap

Date: 2026-07-09
Status: Accepted
Slug: mcp-family-sota-roadmap

## Context

Smart Read MCP was planned as a universal local and guarded-remote path reader.
The active family now has `smart-reader-mcp` as the shipped local format router.

This repo already contains legacy `docs/adr/0001-boundary.md`. That legacy ADR
is grandfathered. This PR-number ADR records the new family roadmap decision.

## Decision

Adopt `docs/roadmap/sota-family-roadmap.md` as the repo-local roadmap.

The repository should either remain retired in favor of `smart-reader-mcp`, or
reactivate only as a narrowly scoped remote URL/path policy substrate with a new
ADR.

## Consequences

- This repo must not publish a duplicate generic reader router.
- Smart Reader MCP remains the active universal local reader entrypoint.
- Reactivation requires a distinct boundary, SSRF tests, allowlist policy,
  provenance tests, and release gates.

## Verification

- Roadmap added at `docs/roadmap/sota-family-roadmap.md`.
- PROJECT and README link to the roadmap.
- Docs-only validation: `git diff --check`.
