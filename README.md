# Hivefolio MCP (Cursor plugin)

Remote MCP connector for [Hivefolio](https://www.hivefolio.gg) — gaming and esports profiles, organisations, jobs, and events.

**Server:** `https://api.hivefolio.gg/mcp` (Streamable HTTP)  
**Auth:** Auth0 OAuth + Hivefolio consent (Allow)  
**Privacy:** https://www.hivefolio.gg/hive/privacy  
**Support:** declan@hivefolio.gg

## Install (Marketplace)

Install **Hivefolio** from the Cursor Marketplace when listed, then complete Auth0 sign-in and Hivefolio **Allow**.

## Install (custom / pilot)

Add to Cursor MCP settings (`mcp.json`):

```json
{
  "mcpServers": {
    "hivefolio-prod": {
      "url": "https://api.hivefolio.gg/mcp"
    }
  }
}
```

## First-run consent

1. Cursor connects → Auth0 login.  
2. Open Hivefolio **Allow** (consent). Auth0 alone does not create a grant.  
3. Reload the MCP server in Cursor.  
4. Revoke anytime: https://www.hivefolio.gg/account-settings → Connected apps.

If you see `mcp_grant_missing`, open the `consent_url` from the error, Allow, then Reload.

## Demo prompts

- `Use Hivefolio get_me and summarise my profile in 5 bullets.`  
- `Search Hivefolio public profiles for "esports" and list the top 3 with usernames.`  
- `List my managed Hivefolio entities.`  
- `Update my Hivefolio tagline to "Esports builder — MCP pilot" (only with write consent).`

## License

MIT
