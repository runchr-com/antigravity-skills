# 📓 Planning Hub: Strategy & Design

This guide provides a deep dive into the most effective **Planning-First** skills from the Antigravity Awesome Skills library.

---

## 🏗️ Core Planning Tools

### 1. 🧠 @brainstorming
The "De-risking Machine." It is designed to evaluate your ideas before a single line of code is written.

*   📂 **Path**: `~/.gemini/antigravity/skills/brainstorming/`
*   🔥 **Scenarios**:
    *   **MVP Scoping**: Define the absolute minimum needed to launch.
    *   **Architecture & Logic**: Plan complex systems and data flows.
    *   **ROI Analysis**: Ask the agent to evaluate the feasibility vs. value.
*   💬 **Example Prompt**: `"Use @brainstorming to design a subscription-based AI newsletter generator. Focus on user onboarding and API integration."`

---

### 2. 📋 @product-manager
A senior PM agent with deep expertise across 6 knowledge domains, 30+ frameworks, and 12 templates. Focuses on **User Experience** and **Product-Market Fit**.

*   📂 **Path**: `~/.gemini/antigravity/skills/product-manager/`
*   🎯 **Capabilities**:
    *   **Proven Frameworks**: Applies RICE scoring, MoSCoW, Kano Model, and Jobs-to-be-Done.
    *   **Templates**: Built-in templates for PRDs, One-pagers, and Retrospectives.
    *   **SaaS Metrics**: Calculates 32 metrics including MRR, ARR, Churn, LTV, and CAC.
*   💬 **Example Prompt**: `"Write a PRD for a hybrid to-do app and categorize the initial tasks using the MoSCoW framework."`

---

### 3. 🚀 @saas-mvp-launcher
Provides a structured roadmap covering the tech stack, architecture, auth, payments, and checklists to launch a SaaS MVP from scratch as fast as possible.

*   📂 **Path**: `~/.gemini/antigravity/skills/saas-mvp-launcher/`
*   🛠️ **Capabilities**:
    *   **Validation Checklist**: Forces you to get out of the building and validate before coding.
    *   **Tech Stack Choice (2026)**: Recommends Next.js 15, Tailwind, Supabase, Prisma, Clerk, Stripe, Vercel.
    *   **Architecture Snippets**: Provides standard boilerplates for multi-tenant DB schema, Clerk middleware, and Stripe integrations.
    *   **Pre-Launch Checklist**: Reviews environment variables, security headers, and onboarding flows.
*   💬 **Example Prompt**: `"I'm building a B2B review management SaaS. Design the initial Prisma schema including subscriptions and multi-tenancy."`

---

### 4. 📊 @business-analyst
Expert business analyst focused on transforming complex business data into actionable insights, market sizing, and strategic recommendations.

*   📂 **Path**: `~/.gemini/antigravity/skills/business-analyst/`
*   📈 **Capabilities**:
    *   **Market & Customer Analytics**: TAM/SAM/SOM breakdown, A/B testing frameworks, and cohort analysis.
    *   **Financial Modeling**: LTV modeling, CAC optimization, and unit economics.
    *   **KPI Frameworks**: North Star metrics, OKRs, and executive dashboard design.
*   💬 **Example Prompt**: `"Create a market sizing analysis for our new subscription service with a TAM/SAM/SOM breakdown."`

---

## 🌊 Planning-to-Execution Workflow

A common mistake is to skip planning. Follow this **Golden Path**:

1.  **Ideation**: Use `@brainstorming` to explore the "What."
2.  **Validation**: Use `@business-analyst` to check the "Market."
3.  **Refinement**: Use `@product-manager` to define the "How" (PRDs/Specs).
4.  **Launch Prep**: Use `@saas-mvp-launcher` to select the "Tools" and prepare the stack.

> [!IMPORTANT]
> **Always document your planning results.** I can save these results as `docs/SPEC.md` or `docs/PLAN.md` in your project to ensure I don't lose context later.

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/planning.md) | | |

---
