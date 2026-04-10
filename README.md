# 🛠️ Hermes-Forge: The Self-Expanding AI Agent

[![Hermes Agent](https://img.shields.io/badge/Agent-Hermes--3-orange.svg)](https://github.com/NousResearch/hermes-agent)
[![MCP](https://img.shields.io/badge/Protocol-MCP-blue.svg)](https://modelcontextprotocol.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **"Don't just give an agent tools. Give it the power to build its own."**

**Hermes-Forge** is a meta-skill for [Hermes-Agent](https://github.com/NousResearch/hermes-agent) that enables it to autonomously design, code, install, and validate new **Model Context Protocol (MCP)** servers. 

When Hermes encounters a task for which it lacks the proper tools, it can "forge" a new limb for itself, expanding its capabilities in real-time.

---

## 🧠 Why is this "Exotic"?

Most agents are limited by the tools provided by their developers. **Hermes-Forge** breaks this barrier. 

### The "Ghost in the Shell" Moment (Real Example)
During development, Hermes-Forge demonstrated remarkable autonomous resilience. When asked to install a server, it initially tried to guess the system path:
1. Attempted to write to `/home/user/...` → **Permission Denied.**
2. Attempted to write to `/home/hermes/...` → **Directory Not Found.**
3. **Self-Correction:** It ran `pwd` and `ls -ld ~/.hermes/` to identify the actual environment.
4. Correctly identified the path as `/home/john/...` and successfully completed the installation.

This skill also demonstrates **Autonomous Language Selection**: it can decide to forge a server in **Python** or **Node.js** based on the availability of specific libraries.

---

## 🚀 Key Features

*   **Autonomous Discovery:** Researches API documentation to design tool schemas.
*   **Cross-Language Support:** Forges servers in Python (FastMCP) or Node.js.
*   **Automatic Dependency Management:** Handles `pip install` and `npm install` automatically.
*   **Pre-Deployment QA:** Runs "smoke tests" on generated code and self-patches if errors occur.
*   **Seamless Integration:** Automatically updates `config.yaml` to activate new tools.

---

## 📦 Installation

1.  **Clone the skill** into your Hermes skills directory:
    ```bash
    cd ~/.hermes/skills/
    git clone https://github.com/NixTensor/hermes-forge.git
    ```

2.  **Ensure MCP tools are enabled** in your Hermes configuration.

---

## 🕹️ Usage

Simply tell Hermes to connect to a new service:

> **User:** "Hermes, I want to manage my local Obsidian notes. Create an MCP server for it and install it."
> 
> **Hermes:** *[Navigates, writes server.py, installs mcp, patches config.yaml]*
> "The Obsidian Forge is complete. I can now list and read your notes using the new `list_notes` and `read_note` tools."

---

## 📂 Project Structure

hermes-forge/
├── SKILL.md          # The core instructions for the "Forge" persona
├── templates/        # (Optional) Base templates for MCP servers
└── README.md         # Professional documentation

## 🤝 Contributing

Contributions to the Forge logic or new templates are welcome!
