# 🛡️ Security Hub: Hardening & Auditing

This guide covers skills for proactive security auditing, vulnerability identification, and infrastructure hardening.

---

## 🏗️ Core Security Tools

### 1. 🔍 @security-auditor
Your Expert Security Consultant specializing in DevSecOps, Shift-left security, and compliance frameworks.
*   📂 **Path**: `~/.gemini/antigravity/skills/security-auditor/`
*   🎯 **Capabilities**:
    *   **Threat Modeling & Scanning**: Integrates SAST/DAST/IAST and creates STRIDE/PASTA threat models.
    *   **Compliance & Governance**: Ensures adherence to GDPR, HIPAA, PCI-DSS, SOC 2, and ISO 27001.
    *   **Pipeline Security**: Enforces secrets management (HashiCorp Vault) and software supply chain security (SBOM).
*   💬 **Example Prompt**: `"Use @security-auditor to perform a threat model analysis (STRIDE) on this new authentication flow."`

---

### 2. 🔎 @differential-review
A highly structured, evidence-based security code reviewer for pull requests and commits.
*   📂 **Path**: `~/.gemini/antigravity/skills/differential-review/`
*   🛠️ **Capabilities**:
    *   **Risk-Level Triage**: Scales the review strategy based on codebase size and PR risk level (e.g., Auth/Crypto = HIGH).
    *   **Adversarial Analysis**: Rejects "small PR, quick review" fallacies and calculates exact blast radius.
    *   **Formal Reporting**: Automatically generates deep Markdown audit reports for the PR.
*   💬 **Example Prompt**: `"Use @differential-review to audit this PR containing an Auth rewrite. Run a SURGICAL strategy and calculate the blast radius."`

---

### 3. 🏗️ @security-scanning-security-hardening
An orchestrator skill that coordinates a 4-phase, defense-in-depth hardening program using multiple agents.
*   📂 **Path**: `~/.gemini/antigravity/skills/security-scanning-security-hardening/`
*   ✨ **Capabilities**:
    *   **Phase 1-2 (Assess & Fix)**: Dispatches `security-auditor` and specialized coders to fix CVSS 7+ vulnerabilities.
    *   **Phase 3-4 (Harden & Verify)**: Deploys WAF/IDS, configures SIEM, and validates via penetration testing.
*   💬 **Example Prompt**: `"Initiate a comprehensive hardening program for my backend API using @security-scanning-security-hardening."`

---

### 4. ⛓️ @solidity-security
Master of Web3 smart contract security, vulnerability prevention, and secure Solidity patterns.
*   📂 **Path**: `~/.gemini/antigravity/skills/solidity-security/`
*   🌟 **Capabilities**:
    *   **DeFi Protocols**: Audits for reentrancy, integer overflows, oracle manipulation, and access control bypassing.
    *   **Pattern Playbook**: References dedicated implementation playbooks for secure architectural patterns.
*   💬 **Example Prompt**: `"Audit this Solidity Crowdfunding contract using @solidity-security. Focus on reentrancy attack vectors."`

---

### 5. 🏴‍☠️ @red-team-tactics
An adversary simulation skill based strictly on the MITRE ATT&CK framework.
*   📂 **Path**: `~/.gemini/antigravity/skills/red-team-tactics/`
*   🔪 **Capabilities**:
    *   **Attack Lifecycle**: Simulates Reconnaissance, Privilege Escalation, Lateral Movement, and Defense Evasion.
    *   **Active Directory**: Simulates Kerberoasting, Golden Tickets, and credential harvesting methodologies.
    *   **Detection Gaps**: Identifies precisely where internal defenses failed to catch the simulated attack.
*   💬 **Example Prompt**: `"Use @red-team-tactics to outline an adversary simulation for Lateral Movement in a Windows Active Directory environment."`

---

## 🌊 Security-First Workflow

1.  **Modeling**: `@security-auditor` to identify the most critical assets and threats.
2.  **Audit**: `@differential-review` for all code changes.
3.  **Hardening**: `@security-scanning-security-hardening` to seal the vulnerabilities found.
4.  **Verification**: `@red-team-tactics` to challenge the new security layers.

---

## 🧭 Navigation

| [🏠 Home](../../README.md) | [📓 Planning](./planning.md) | [🎨 Frontend](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 Backend](./backend.md) | [🛡️ Security](./security.md) | [🧞 Agents](./agents.md) |
| [🧪 QA](./qa_testing.md) | [📦 Bundles](./bundles.md) | [🌊 Workflows](./workflows.md) |
| [🇰🇷 한국어 버전](../ko/security.md) | | |

---
