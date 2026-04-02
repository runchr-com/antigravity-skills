# 🧞 AI Agents Hub: Autonomous Intelligence

This guide focuses on skills for designing, building, and evaluating autonomous AI agent systems and Model Context Protocol (MCP) servers.

---

## 🏗️ Core AI Agent Tools

### 1. 🧞 @agent-orchestrator
The central meta-skill that orchestrates all agents in the ecosystem, acting as a skill registry and coordinator.
*   📂 **Path**: `~/.gemini/antigravity/skills/agent-orchestrator/`
*   🎯 **Capabilities**:
    *   **Auto-Discovery**: Scans and registers all available skills dynamically using MD5 caching.
    *   **Algorithmic Matching**: Matches user queries to the best skills using capability tags and triggers.
    *   **Workflow Patterns**: Orchestrates capabilities into Sequential Pipelines, Parallel Execution, or Primary+Support models.
*   💬 **Example Prompt**: `"Use @agent-orchestrator to find the best skills for extracting e-commerce data and orchestrate a sequential pipeline to send the results via messaging."`

---

### 🧠 2. @autonomous-agent-patterns
Design patterns for building autonomous coding agents, inspired by architectures like Cline and OpenAI Codex.
*   📂 **Path**: `~/.gemini/antigravity/skills/autonomous-agent-patterns/`
*   🛠️ **Capabilities**:
    *   **Agent Loops**: Implements the standard *Think → Decide → Act → Observe* autonomous loop.
    *   **Context & Memory**: Manages complex context injections and state checkpoint/resume algorithms.
    *   **Sandboxing & Browser**: Provides architectural patterns for isolated code execution and visual browser automation.
*   💬 **Example Prompt**: `"Design an autonomous agent loop using @autonomous-agent-patterns that employs a fast model for planning and a smart model for code generation."`

---

### ⚒️ 3. @agent-tool-builder
A specialized UI/UX expert for the LLM-to-tool interface, ensuring tools don't cause hallucinations or silent failures.
*   📂 **Path**: `~/.gemini/antigravity/skills/agent-tool-builder/`
*   ✨ **Capabilities**:
    *   **Schema Design**: Crafts unambiguous JSON Schemas that language models deeply understand.
    *   **Error Healing**: Designs explicit error messages that help the agent recover, instead of failing silently.
    *   **Safety Guards**: Enforces permission levels (AUTO, ASK_ONCE, ASK_EACH) for dangerous tool calls.
*   💬 **Example Prompt**: `"Use @agent-tool-builder to design the JSON Schema and error handling logic for a Google Sheets data extraction tool."`

---

### 📏 4. @agent-evaluation
Frameworks for benchmarking and evaluating LLM agent performance in an environment where "correct" has no single answer.
*   📂 **Path**: `~/.gemini/antigravity/skills/agent-evaluation/`
*   🌟 **Capabilities**:
    *   **Statistical Analysis**: Runs tests multiple times and analyzes result distributions instead of binary pass/fail.
    *   **Behavioral Contracts**: Defines and tests agent behavioral invariants to prevent regressions.
    *   **Adversarial Testing**: Actively attempts to break agent behavior to ensure production reliability.
*   💬 **Example Prompt**: `"Design an adversarial testing framework to evaluate our new research agent using @agent-evaluation."`

---

### 🏛️ 5. @mcp-builder
Expert system for building Model Context Protocol (MCP) servers, bridging LLMs with local environments and specific APIs.
*   📂 **Path**: `~/.gemini/antigravity/skills/mcp-builder/`
*   🔪 **Capabilities**:
    *   **Protocol Implementation**: Implements Streamable HTTP or stdio transports based on the MCP specification.
    *   **SDK Mastery**: Writes idiomatic TypeScript and Python using FastMCP frameworks.
    *   **Read/Write Operations**: Properly annotates tools with `readOnlyHint`, `destructiveHint`, and handles pagination.
*   💬 **Example Prompt**: `"Use @mcp-builder to scaffold a TypeScript MCP server that securely exposing my local JIRA issues to the agent."`

---

## 🌊 AI Agents Workflow

1.  **Architecture**: `@agent-orchestrator` to map out the system flow.
2.  **Pattern Selection**: `@autonomous-agent-patterns` to choose the reasoning loop.
3.  **Tool Development**: `@agent-tool-builder` + `@mcp-builder` to build the required capabilities.
4.  **Optimization**: `@agent-evaluation` to iterate and improve performance.

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/agents.md) | | |

---
