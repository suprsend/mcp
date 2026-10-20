# SuprSend MCP Server

The official hosted **Model Context Protocol (MCP)** server for [SuprSend](https://www.suprsend.com). Connect an AI agent — Claude, ChatGPT, GitHub Copilot, Cursor, or any MCP client — to your SuprSend account and operate your notification stack in natural language.

- **Endpoint:** `https://mcp.suprsend.com/mcp`
- **Transport:** Streamable HTTP (remote MCP server — nothing to install or host)
- **Auth:** OAuth 2.1 — you sign in with your SuprSend account

> This repository is the public description of the hosted server, for the MCP registries and Copilot surfaces. The server runs at the endpoint above.

## What it does

SuprSend is a notification infrastructure platform. The MCP server lets an agent operate your SuprSend workspaces:

- **Users & preferences** — look up users, their channels, subscriptions, and notification preferences, and update them.
- **Lists & objects** — manage subscriber lists and objects (teams, accounts) and their members.
- **Workflows** — read, draft, and publish notification workflows.
- **Templates** — read, edit, validate, and publish multi-channel templates (email, SMS, push, Inbox, WhatsApp, Slack, Teams).
- **Delivery data** — query delivery logs, workflow runs, and analytics with read-only SQL to answer questions like "why did user X not get Y?".
- **Events, schemas, translations, vendors, tenants, and broadcasts** — and more.

It also ships **skills** (packaged guidance for authoring workflows, templates, and SQL) and interactive **MCP Apps** (a chart view for query results and a message-content preview).

## Connect it

Add the remote MCP server URL in your client and sign in when prompted:

- **Claude (web, desktop, or Code):** add a custom connector with the URL `https://mcp.suprsend.com/mcp`.
- **ChatGPT and other MCP clients:** add `https://mcp.suprsend.com/mcp` as a remote (Streamable HTTP) MCP server.
- **Scope to one workspace:** connect to `https://mcp.suprsend.com/mcp/<workspace>` to pin a single workspace, or use `.../mcp` for all workspaces you can access.

You authenticate with your SuprSend login, and the agent gets only the access your role allows (admins get write tools; members get reads).

## Learn more

- SuprSend: https://www.suprsend.com
- Documentation: https://docs.suprsend.com
