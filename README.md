# Democruit MCP

Democruit is a career workspace for resumes and CVs, cover letters, ATS checks, job tracking, personal websites, company research and written interview practice. This MCP server lets your AI client work with your own Democruit data.

This repository only holds the public listing metadata. The server is hosted by Democruit and its source code is not part of this repository.

## Connect

- Endpoint: `https://mcp.democruit.com/mcp`
- Transport: Streamable HTTP
- Authentication: OAuth 2.1 authorization code flow with PKCE, dynamic client registration, refresh token rotation and account-level revocation
- Health check: `https://mcp.democruit.com/health`

Claude Code:

```sh
claude mcp add --transport http democruit https://mcp.democruit.com/mcp
```

Other clients: add the endpoint above as a remote Streamable HTTP server, sign in to Democruit and review the requested permissions.

## What it can do

- Read, create and edit resumes and cover letters from your saved facts
- Run ATS checks and apply supported fixes
- Track jobs and link documents to them
- Manage personal websites
- Research companies and practice written interviews within your plan's allowances
- Draft emails, LinkedIn text and resume bullets (drafts only, nothing is sent)

## Permissions and safety

- Access is limited to the signed-in owner's data and to the scopes you grant on the consent screen (for example `resume:read`, `resume:write`, `job_tracker:read`).
- Deleting items, changing website visibility, domain changes and similar actions first return a preview. They run only after you confirm in the conversation.
- Tools never submit a job application or send an email on your behalf.
- Plan allowances apply, and the rate limit is 500 requests per minute.

## Links

- Product and install guide: https://democruit.com/mcp
- Privacy Policy: https://democruit.com/privacy-policy
- Terms of Service: https://democruit.com/terms-of-service
- Support: info@democruit.com

Democruit is operated by Aequovia, LLC.
