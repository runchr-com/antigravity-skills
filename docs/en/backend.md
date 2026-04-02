# 🐍 Backend & Data Hub: Scalable Logic

This guide covers skills for building high-performance APIs, robust data models, and optimized database schemas.

---

## 🏗️ Core Backend Tools

### 1. 🐍 @python-pro
Your Senior Backend Architect specializing in the modern Python 3.12+ 2024/2025 ecosystem.
*   📂 **Path**: `~/.gemini/antigravity/skills/python-pro/`
*   🎯 **Capabilities**:
    *   **Modern Tooling Ecosystem**: Recommends `uv` for package management, `ruff` for linting/formatting, and `pyright` for typing over legacy alternatives.
    *   **High-Performance Async**: Designs asynchronous architectures using modern `asyncio`, FastAPI, and background workers (Celery/Redis).
    *   **Production Readiness**: Enforces >90% test coverage, comprehensive exception handling, and Docker multi-stage builds.
*   💬 **Example Prompt**: `"Refactor this data processing script using @python-pro. Upgrade it to use uv, ruff, and Python 3.12+ structural pattern matching."`

---

### 2. 🛣️ @fastapi-router-py
A scaffold skill to rapidly implement FastAPI routers adhering to established best practices.
*   📂 **Path**: `~/.gemini/antigravity/skills/fastapi-router-py/`
*   🛠️ **Capabilities**:
    *   **Pattern Enforcement**: Mounts routers correctly with clean URL hierarchies (`/items`, `/items/{id}`).
    *   **Strict Contracts**: Binds precise Pydantic `response_model` types to every endpoint.
    *   **HTTP Semantics**: Forces correct HTTP status codes (e.g., `201 CREATED` for POST, `204 NO_CONTENT` for DELETE).
*   💬 **Example Prompt**: `"Use @fastapi-router-py to generate the auth endpoints (Login, Register). Ensure correct 401 exceptions and status codes."`

---

### 3. 💎 @pydantic-models-py
Masters the Multi-Model pattern for Pydantic (v2) to maintain crystal-clear API boundaries.
*   📂 **Path**: `~/.gemini/antigravity/skills/pydantic-models-py/`
*   ✨ **Capabilities**:
    *   **Layered Validation**: Separates schemas into `Base`, `Create` (all required), `Update` (all optional), and `Response`.
    *   **Serialization Rules**: Automatically configures `camelCase` aliases for seamless Frontend/Backend JSON interaction.
*   💬 **Example Prompt**: `"Generate the multi-model pattern for a 'Workspace' entity using @pydantic-models-py. Include camelCase aliasing."`

---

### 4. 🗄️ @database-design
An agnostic database architecture advisor focusing on logical structure, normalization, and optimization.
*   📂 **Path**: `~/.gemini/antigravity/skills/database-design/`
*   🌟 **Capabilities**:
    *   **Contextual Selection**: Chooses the right DB (PostgreSQL, SQLite, Neon, Turso) and ORM (Prisma, Drizzle) instead of blindly defaulting.
    *   **Anti-Pattern Guard**: Prevents missing indexes, `SELECT *`, and N+1 query problems in schema relationships.
*   💬 **Example Prompt**: `"Review this Drizzle ORM schema with @database-design. Are the indexes correct for a high-read tenant table?"`

---

### 5. 💾 @sql-pro
An advanced SQL specialist for high-performance tuning, OLAP/OLTP architecture, and cloud databases.
*   📂 **Path**: `~/.gemini/antigravity/skills/sql-pro/`
*   📈 **Capabilities**:
    *   **Advanced Analytics**: Writes raw complex CTEs, window functions, and time-travel queries.
    *   **Execution Analysis**: Runs `EXPLAIN ANALYZE` conceptually to build ideal indexing strategies.
    *   **Cloud Data Warehousing**: Optimized for Snowflake, BigQuery, and HTAP architecture.
*   💬 **Example Prompt**: `"Optimize this analytical query using @sql-pro. Suggest composite indexes to stop the sequential scan."`

---

## 🌊 Backend-First Workflow

1.  **Modeling**: `@pydantic-models-py` to define the shape of your data.
2.  **Storage**: `@database-design` to map that data into a database schema.
3.  **API**: `@fastapi-router-py` to build the endpoints for data access.
4.  **Refinement**: `@python-pro` + `@sql-pro` to optimize performance and logic.

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/backend.md) | | |

---
