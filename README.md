# MetaDock MCP

Control the [MetaDock](https://metadock.app) desktop workspace over the **Model Context Protocol**.

MetaDock is a Windows power-user workspace that docks browsers and native apps side by side. Its
built-in MCP server exposes everything you can do by hand as tools, so Claude — or any MCP client —
can open and drive browsers, arrange layouts, manage bookmarks and downloads, search, and more.

Listed in the official MCP registry as **`app.metadock/metadock`**.

## What you can do

The server exposes 11 tool groups:

| Group | Examples |
|---|---|
| **Browser** | create/close browsers, navigate, execute JavaScript, click, type, screenshot, cookies, zoom, device emulation |
| **Layout** | arrange, save, and switch multi-browser layouts |
| **Workspace** | manage and switch whole workspaces |
| **Bookmark** | read and write bookmarks |
| **History** | query browsing history |
| **Download** | start and manage downloads |
| **Search** | search + aliases |
| **Adblock** | toggle ad-blocking and lists |
| **App / Settings / Permission** | app state, settings, and permissions |

## Requirements

- The **MetaDock desktop app** installed and running (Windows). Get it at **[metadock.app](https://metadock.app)**.
- The MCP server enabled in **MetaDock → Settings → API & Automation**.

The server runs **locally** on your machine — stdio (`metadock mcp`) or loopback HTTP — so your data
never leaves your computer.

## Install

### Option A — from inside MetaDock (recommended)

**Settings → API & Automation → Install to desktop tools**, then pick your client (Claude Desktop,
Claude Code, Cursor, VS Code, Codex, …). MetaDock writes the correct config and enables the endpoint
for you.

### Option B — Claude Desktop (.mcpb)

Download the latest `metadock-<version>.mcpb` from [Releases](../../releases), open it with Claude
Desktop, and confirm the path to `metadock.exe` when prompted.

### Option C — manual (any stdio MCP client)

Add this to your client's MCP config, adjusting the path to where MetaDock is installed
(default `%LOCALAPPDATA%\MetaDock\bin\metadock.exe`):

```json
{
  "mcpServers": {
    "metadock": {
      "command": "C:\\Users\\YOU\\AppData\\Local\\MetaDock\\bin\\metadock.exe",
      "args": ["mcp"]
    }
  }
}
```

### Option D — official MCP registry

Any registry-aware client can discover the server by name: **`app.metadock/metadock`**.

## Privacy & safety

Everything runs on your machine. By design, the following are **not** reachable over MCP (or any
automation surface): the Password Vault, the AI assistant, profile-bundle import/export, and the
system clipboard.

## Links

- Website — https://metadock.app
- MCP setup docs — https://metadock.app/docs/mcp
- Support — https://metadock.app/support
- Privacy policy — https://metadock.app/privacy

## Notes

- The `.mcpb` in Releases is currently **unsigned**; Claude Desktop will note this on install.
- This bundle references your installed `metadock.exe` and launches `metadock mcp` — the app itself
  is not bundled.
