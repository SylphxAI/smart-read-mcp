# SOTA Family Roadmap

Status: archived adoption plan
Owner: Smart Read MCP
Scope: repo-local future plan and its role in the SylphxAI MCP family
Decision record: pending PR-number ADR

## Family Role

Smart Read MCP was planned as the universal path reader for local files and
guarded remote URLs. The active family now has `smart-reader-mcp` for format
sniffing and delegation.

This repository should not compete with Smart Reader MCP. Its future is either
formal retirement in favor of `smart-reader-mcp` or a narrowly scoped remote
URL/path policy package if that boundary is still needed.

## Family Fit

| Project | Relationship |
| --- | --- |
| Smart Reader MCP | Active universal local reader router; owns `read_media` and sibling delegation. |
| PDF/Image/Video Reader MCPs | Specialist evidence engines that Smart Reader routes to. |
| Filesystem MCP | Owns broad local filesystem access and write safety. |
| Reader Evidence | Potential shared evidence schema substrate. |

## SOTA End State

The cleanest family shape is one active reader router. If Smart Read MCP is
retired, its README should point to Smart Reader MCP and no package should be
published from this repo. If reactivated, it must own a distinct remote URL and
path-policy capability that Smart Reader MCP does not own.

## Roadmap

### Phase 0: Retirement Or Reactivation Decision

- Decide whether this repository is permanently retired.
- If retired, keep it archived and document Smart Reader MCP as the successor.
- If reactivated, update PROJECT and README to state the unique path/remote URL
  boundary.

### Phase 1: No Duplicate Router

- Do not implement another generic file router here while Smart Reader MCP owns
  active routing.
- Do not publish package versions that confuse users about the recommended
  Reader entrypoint.

### Phase 2: Possible Policy Substrate

- If a separate package is justified, limit it to guarded remote URL fetch,
  content-addressed fetch cache, allowlist policy, SSRF protection, and source
  provenance.
- Smart Reader MCP would consume that policy package instead of duplicating it.

## Validation Gates

- README clearly identifies the active successor or unique reactivation scope.
- No package release occurs without a new ADR.
- Any remote URL feature has SSRF, allowlist, size, cache, and provenance tests.
