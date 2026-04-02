# 🧪 QA & Testing Hub: Quality Assurance

This guide covers skills for automated testing, browser verification, and maintaining high code quality through rigorous validation.

---

## 🏗️ Core QA & Testing Tools

### 1. 🧪 @testing-qa
A comprehensive 8-phase testing workflow bundle that orchestrates everything from unit tests to quality gates.
*   📂 **Path**: `~/.gemini/antigravity/skills/testing-qa/`
*   🎯 **Capabilities**:
    *   **The Testing Pyramid**: Structures your testing strategy (70% Unit, 20% Integration, 10% E2E).
    *   **Phased Automation**: Guides you through Unit, Integration, E2E, Browser, and Performance phases.
    *   **Quality Gates Checklist**: Enforces >80% coverage, clean linting, and completed code reviews.
*   💬 **Example Prompt**: `"Use @testing-qa to design a comprehensive test suite and testing pyramid for this new payment processing feature."`

---

### 🎭 2. @e2e-testing
A rigorous 7-phase end-to-end testing workflow heavily relying on Playwright for browser automation.
*   📂 **Path**: `~/.gemini/antigravity/skills/e2e-testing/`
*   🛠️ **Capabilities**:
    *   **Implementation & Automation**: Builds page objects, handles dynamic content, and sets up headless testing.
    *   **Visual Regression Validation**: Implements baseline image creation and visual assertions using `@ui-visual-validator`.
    *   **Cross-Browser & CI/CD**: Configures multi-browser tests (Chromium, Firefox, WebKit) and parallel execution in GitHub Actions.
*   💬 **Example Prompt**: `"Use @e2e-testing to create a Playwright script that performs a complete checkout flow, including a cross-browser visual regression check."`

---

### 🔴 3. @tdd-workflow
A strict enforcer of the Test-Driven Development (TDD) cycle: **RED → GREEN → REFACTOR**.
*   📂 **Path**: `~/.gemini/antigravity/skills/tdd-workflow/`
*   ✨ **Capabilities**:
    *   **The Three Laws**: Ensures you write production code *only* to make a failing test pass.
    *   **AAA Pattern**: Structures every test into Arrange, Act, and Assert steps.
    *   **YAGNI Principle**: Prevents over-engineering during the Green phase. The test is the true specification.
*   💬 **Example Prompt**: `"Guide me through building a new 'Order History' feature using the @tdd-workflow. Start with the RED phase."`

---

### 🌐 4. @webapp-testing
A specialized skill for testing local, dynamically rendered web applications using native Python Playwright scripts.
*   📂 **Path**: `~/.gemini/antigravity/skills/webapp-testing/`
*   🌟 **Capabilities**:
    *   **Lifecycle Management**: Seamlessly spins up and shuts down local servers using `scripts/with_server.py`.
    *   **Reconnaissance-Then-Action**: Forces the agent to wait for `networkidle`, take a snapshot of the rendered DOM, and identify selectors *before* interacting.
    *   **Black-box Execution**: Executes complex interaction scripts externally to preserve the LLM's context window.
*   💬 **Example Prompt**: `"Use @webapp-testing to spin up my frontend and backend services, then check if the 'Submit' button on localhost:5173 is correctly disabled on invalid input."`

---

### 🛡️ 5. @lint-and-validate
A mandatory quality gate that acts as the final check before any task can be considered "done".
*   📂 **Path**: `~/.gemini/antigravity/skills/lint-and-validate/`
*   🔪 **Capabilities**:
    *   **The Quality Loop**: Enforces a strict *Write → Audit → Analyze → Fix* loop.
    *   **Ecosystem Validation**: Runs `npm run lint`, `tsc --noEmit`, `ruff check`, `bandit`, and `mypy` depending on the tech stack.
    *   **Strict Blocking**: Categorically blocks any "Task Completed" message if the *FINAL AUDIT REPORT* fails.
*   💬 **Example Prompt**: `"Run @lint-and-validate on the entire project to ensure it meets our quality standards before we commit."`

---

## 🌊 QA-First Workflow

1.  **Red Phase**: `@tdd-workflow` to write the failing test cases.
2.  **Implementation**: Build the feature until tests pass.
3.  **Sanity Check**: `@lint-and-validate` to ensure code quality and style.
4.  **End-to-End**: `@e2e-testing` + `@webapp-testing` to verify the feature in a real browser.

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/qa_testing.md) | | |

---
