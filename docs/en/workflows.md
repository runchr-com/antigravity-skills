# 🌊 Execution Workflows

Workflows are high-level playbooks for complex, multi-stage projects. They help you orchestrate multiple skills in the correct order to achieve a specific outcome.

---

## 🚀 1. The Ultrawork Pipeline (`/ultrawork`)
The flagship high-quality 5-phase development workflow featuring 11 review steps.
*   **Trigger**: `/ultrawork`
*   **Phases**:
    1.  **Preparation**: Repository audit and dependency checks.
    2.  **Implementation**: TDD-based coding with active security linting.
    3.  **Review**: Deep differential reviews and vulnerability scans.
    4.  **Testing**: Automated E2E and unit test executions.
    5.  **Finalization**: Conventional commits and changelog generation.

---

## 🧠 2. Ideation & Planning (`/brainstorm` & `/plan`)
Design-first scoping before a single line of code is written.
*   **Triggers**: `/brainstorm`, `/plan`, `/deepinit`
*   **Capabilities**:
    *   **Brainstorm**: Explores user intent, clarifies constraints, and proposes approaches.
    *   **Plan**: Analyzes requirements, selects tech stack, and decomposes into prioritized, atomic tasks.
    *   **Deep Init**: Initializes project harness (`AGENTS.md`, `ARCHITECTURE.md`, structured knowledge base).

---

## 🧞 3. Multi-Agent Orchestration (`/orchestrate` & `/coordinate`)
Coordinate multiple agents for complex, multi-domain projects.
*   **Triggers**: `/orchestrate`, `/coordinate`
*   **Capabilities**:
    *   **Orchestrate**: Automated CLI-based parallel agent execution (spawns subagents via Gemini CLI).
    *   **Coordinate**: PM-led planning, parallel agent spawning, and QA review synchronization.

---

## 🛡️ 4. Review & Debugging (`/review` & `/debug`)
Structured bug diagnosis and comprehensive QA pipelines.
*   **Triggers**: `/review`, `/debug`
*   **Capabilities**:
    *   **Review**: Full QA pipeline encompassing OWASP Top 10 security audits, performance analysis, and WCAG 2.1 AA accessibility checks.
    *   **Debug**: Structured diagnosis (Reproduce → Root Cause → Minimal Fix → Regression Test → Pattern Scan).

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/workflows.md) | | |

---
