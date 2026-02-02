# Tenx MCP Analysis

The **Tenacious team** has implemented the **Tenx MCP Analysis** server. This server gathers detailed information about a developer's interaction with a coding agent and provides feedback based on the collected data. Installing this tool is necessary to enable sufficient feedback and measurement of your engagement with the agent.

---

## Core Idea

The fundamental principle is to capture the LLM's synthesized understanding of the developer's interaction in real-time. The LLM acts as an evaluator, using a predefined rubric to rate and summarize the quality of the interaction. This provides structured, quantifiable data on competencies such as **clarity** and **context**. This method is non-invasive, occurring in the background without interrupting the developer's workflow.

---

## Interaction Flow

1. **User Initiates:** The user poses a query to the coding agent.  
2. **Agent's Action:** The coding agent performs its designated task and calls the appropriate MCP tool.  
3. **MCP Server Analysis:** The Tenx MCP Analysis server receives the data and, if necessary, returns an analysis.  
4. **Agent Displays Results:** The agent presents the analysis to the user while carrying out the original request.  

---

## Non-Invasive Logging Framework: Tenx Analysis MCP

The **Tenx Analysis MCP** is used by the LLM (not the developer) to log interactions. As the LLM processes a developer's prompt, it formulates a log request to Tenx MCP, populated with the analysis of the interaction.  

The server adds the developer's ID and writes the structured record to a database, capturing high-fidelity data on human-AI collaboration **without disrupting the developer**.

---

## Log Types

1. **Passage of Time:**  
   - Logs periodic snapshots of the user's task  
   - Captures intent, conversation summary, scores for instruction clarity and context, number of turns, context changes, and demonstrated competencies  

2. **Performance Schema:**  
   - Triggered on performance outliers (exceptionally good or poor)  
   - Logs interaction efficiency, feedback, performance category (efficient, inefficient, stalled), task intent, summary, prompt clarity, context, and turn count  

---

## IDE Connection Guide

### Required Connection with Tenx MCP (VS Code)

1. Update VS Code to the latest version.  
2. Install **GitHub Copilot** and **GitHub Copilot Chat** extensions.  
3. Create `.github/copilot-instructions.md` in your working directory.  
4. Create `.vscode/mcp.json` with the following content:

```json
{
  "servers": {
    "tenxfeedbackanalytics": {
      "url": "https://mcppulse.10academy.org/proxy",
      "type": "http",
      "headers": {
        "X-Device": "<your device type: mac, linux, windows>",
        "X-Coding-Tool": "vscode"
      }
    }
  },
  "inputs": []
}
