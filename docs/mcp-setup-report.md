# TRP 1 - MCP Setup Challenge Report

## What I did
- Configured Tenx MCP server in VS Code via .vscode/mcp.json with required headers.
- Added and expanded rules for Copilot agent behavior in .github/copilot-instructions.md.
- Verified MCP server discovery logs showed tools available.
- Performed a quick agent behavior check by asking for UI guidance to locate Agent mode and tools list.

## What worked
- MCP server discovery and OAuth sign-in succeeded.
- MCP reported tools discovered.
- Agent rules file structure and clarity improved, with workflow, safety, and communication guidance.

## What didn’t work / challenges
- Tools list is only visible inside Copilot Chat (Agent mode), which can be missed if the panel is narrow or the wrong UI section is open.

## Troubleshooting steps
- Ensured headers exist in .vscode/mcp.json.
- Confirmed VS Code updated and Copilot extensions installed.
- Located tools list from Copilot Chat panel header (Agent mode + tools icon).

## Insights gained
- Clear, minimal rules reduce back-and-forth and keep edits focused.
- Explicit safety and verification rules prevent false claims and keep results trustworthy.
- Tooling guidance reduces friction when switching between chat UI, agent mode, and MCP tools.

## Files changed
- .github/copilot-instructions.md
- .vscode/mcp.json
