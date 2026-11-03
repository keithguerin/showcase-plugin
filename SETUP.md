---
name: showcase-setup
description: Connect the Showcase plugin to the user's account. Use when Showcase tools return an authentication error, or just after the plugin is installed.
---

# Connecting Showcase

Showcase talks to `https://showcase.chat/api/mcp/showcase` over MCP, and needs
the user's own account behind it — the tools are scoped to one library.

## Signing in

Authentication is OAuth 2.1 with Dynamic Client Registration, so there is
nothing to paste. On first use the host opens a Showcase consent screen naming
both sides; the user approves once and the connection persists.

If a tool returns **"Not authenticated. Reconnect the Showcase connector."**,
the token has expired or was revoked. Ask the user to reconnect the connector in
their client's settings. Do not ask them for a token, and never ask them to
paste credentials into the conversation.

## Hosts with a sign-in step of their own

Google Antigravity does MCP OAuth with one
step the others lack: Authenticate, under Customizations → Installed → MCP
Servers, opens the browser, and after Google a page at antigravity.google
shows an authorization code that the user copies into the "Enter authorization
code" box in that same row, then Submit. That code is a one-time OAuth code,
not a credential, and it goes into Antigravity's box, never into the
conversation. A server declared inside an Antigravity plugin gets no sign-in
button at all; the connector belongs in Antigravity's own server list.

Showcase no longer issues API tokens: there is no token to create, and
never ask the user for one, whatever the host.

## Checking it works

Ask Showcase to list the user's shows. A working connection returns their
library; a broken one returns an authentication error rather than an empty list,
so an empty result means the library is genuinely empty.
