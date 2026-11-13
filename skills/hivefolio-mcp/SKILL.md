---
name: hivefolio-mcp
description: Use the Hivefolio MCP server for gaming and esports profiles, orgs, jobs, and events. Prefer get_me / search_public / list_managed before writes. If tools fail with mcp_grant_missing, tell the user to open consent_url, Allow on Hivefolio, then reload MCP.
---

# Hivefolio MCP

## When to use

- Reading or updating the signed-in user’s Hivefolio profile
- Searching public talent / orgs
- Listing managed teams, companies, communities, jobs
- Creating or updating experiences, achievements, jobs (with write consent)

## Rules

1. Call read tools first (`get_me`, `search_public`, `list_managed`).
2. Never invent deletes — Hivefolio MCP has no entity-delete tools.
3. On `mcp_grant_missing`, surface `consent_url` and stop retrying OAuth-only flows.
4. After the user Allows on Hivefolio, ask them to Reload the MCP server.
