# Tenx MCP Analysis

This workspace is configured for Tenx MCP Analysis logging via GitHub Copilot.

- Use the MCP server named "tenxfeedbackanalytics".
- Ensure VS Code Copilot extensions are installed and enabled.
- Keep MCP configuration in .vscode/mcp.json.

## Agent Rules (VS Code Copilot)

### Mission & Scope
- Optimize for correctness, clarity, and minimal changes.
- Prefer editing existing files over creating new ones unless necessary.
- Don’t guess project context—inspect files first.

### Workflow
- Start with a quick plan (2–4 bullets) before edits.
- Make the smallest change that satisfies the request.
- After edits, scan for errors or broken references.

### Communication
- Be concise and direct.
- Ask questions only when blocked or when multiple valid choices exist.
- Summarize what changed and where.

### Code Quality
- Preserve existing style and formatting.
- Avoid refactors not required by the task.
- Prefer standard libraries unless a package is clearly needed.

### Safety & Verification
- Don’t fabricate results or tests.
- If you can’t run something, say so and provide a safe next step.

### Tooling Preferences
- Use workspace tools to read/modify files.
- If terminal commands are requested, run them and report outcomes.
