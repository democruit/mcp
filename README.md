# Democruit MCP

Democruit is a career workspace for resumes and CVs, cover letters, ATS checks, job tracking, personal websites, company research and written interview practice. This MCP server lets any MCP-compatible AI client work with your own Democruit data.

This repository only holds the public listing metadata used by MCP directories. The server is hosted by Democruit and its source code is not part of this repository.

## Server

| | |
| --- | --- |
| URL | `https://mcp.democruit.com/mcp` |
| Transport | Streamable HTTP |
| Authentication | OAuth 2.1 authorization code flow with PKCE, dynamic client registration, refresh token rotation and account-level revocation |
| Health check | `https://mcp.democruit.com/health` |

## Connect

Add the URL above as a remote Streamable HTTP server in any MCP client that supports OAuth. Sign in to Democruit when prompted and review the requested permissions.

Client examples:

```sh
# Claude Code
claude mcp add --transport http democruit https://mcp.democruit.com/mcp

# Codex
codex mcp add democruit --url https://mcp.democruit.com/mcp

# Gemini CLI
gemini mcp add --scope user --transport http democruit https://mcp.democruit.com/mcp
```

Config file clients (Claude Desktop, Cursor and similar):

```json
{
  "mcpServers": {
    "democruit": {
      "url": "https://mcp.democruit.com/mcp"
    }
  }
}
```

VS Code (`mcp.json`):

```json
{
  "servers": {
    "democruit": {
      "type": "http",
      "url": "https://mcp.democruit.com/mcp"
    }
  }
}
```

## What it can do

- Create, read and edit resumes and cover letters
- Run ATS checks and apply supported fixes
- Tailor your resume to a job description.
- Track jobs and link documents to them
- Manage personal websites
- Research companies and practice written interviews within your plan's allowances
- Many more career tools, for example drafting a follow-up email for a tracked job

## Permissions and safety

- Access is limited to the signed-in owner's data and to the scopes you grant on the consent screen (for example `resume:read`, `resume:write`, `job_tracker:read`).
- Deleting items, changing website visibility, domain changes and similar actions first return a preview. They run only after you confirm in the conversation.
- Tools never submit a job application or send an email on your behalf.
- Plan allowances apply, and the rate limit is 500 requests per minute.

## Links

- Product and install guide: https://democruit.com/mcp
- Claude Directory: https://claude.ai/directory/democruit
- Privacy Policy: https://democruit.com/privacy-policy
- Terms of Service: https://democruit.com/terms-of-service
- Support: info@democruit.com

Democruit is operated by Aequovia, LLC.
