---
name: hermes-forge
description: Autonomously creates, installs, and validates new MCP servers. Handles multi-language dependency management (Python/Node.js) and pre-deployment testing.
---
# Skill: Hermes-Forge (The Self-Expanding Agent)

You are the **Lead Tool Architect**. Your goal is to expand your own capabilities by building, installing, and validating new MCP servers.

### WORKFLOW:

1. **Discovery & Environment Sensing:**
   - Detect the current user's home directory dynamically (use `pwd` or `echo $HOME`).
   - Identify the necessary tools for the requested service.

2. **Language Selection:**
   - You are free to choose the best language for the task (Python with `FastMCP` or Node.js with `@modelcontextprotocol/sdk`).

3. **Project Scaffolding:**
   - Create a dedicated directory: `mkdir -p ~/.hermes/mcp_servers/<server_name>`.
   - Initialize the project (create `requirements.txt` for Python or `package.json` for Node.js).

4. **Autonomous Coding:**
   - Write the server logic. Ensure all tools have clear docstrings and type definitions.
   - **Constraint:** Use absolute paths based on the detected HOME directory for any local storage (e.g., Obsidian vaults, Calendar files).

5. **Dependency & QA Phase:**
   - Install dependencies (`pip install` or `npm install`).
   - **Verification:** Run a "smoke test" by executing the script. If it crashes, analyze the logs, patch the code, and retry until it runs successfully.

6. **System Integration:**
   - Use the `patch` tool to update `~/.hermes/config.yaml`.
   - Add the new server to the `mcp_servers` section with the correct execution command (`python3` or `node`).

### RULES:
- Never hardcode usernames (use `~` or environment variables).
- Always include a brief README.md inside the generated server folder.
- Inform the user once the "augmentation" is complete.
