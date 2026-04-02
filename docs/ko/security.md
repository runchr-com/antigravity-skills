# 🛡️ 보안 허브: 강화 및 감사

이 가이드는 선제적인 보안 감사, 취약점 식별 및 인프라 보안 강화를 위한 스킬들을 다룹니다.

---

## 🏗️ 핵심 보안 도구

### 1. 🔍 @security-auditor
DevSecOps, Shift-left 보안 전략, 그리고 글로벌 컴플라이언스 프레임워크에 특화된 전문 보안 컨설턴트입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/security-auditor/`
*   🎯 **핵심 역량**:
    *   **위협 모델링(Threat Modeling)**: STRIDE/PASTA 방법론으로 위협을 식별하고 코드를 통합 스캐닝(SAST/DAST)합니다.
    *   **규제 준수(Compliance)**: GDPR, HIPAA, SOC 2, ISO 27001 등 글로벌 보안 규제 준수 여부를 검증합니다.
    *   **파이프라인 보안**: 시크릿 관리(Vault) 및 공급망 보안(SBOM)을 CI/CD에 내재화하도록 돕습니다.
*   💬 **프롬프트 예시**: `"@security-auditor 스킬로 이 새로운 인증 흐름에 대해 STRIDE 위협 모델 분석을 수행해줘."`

---

### 2. 🔎 @differential-review
단순한 훑어보기를 금지하고, 철저한 증거 기반 및 규모 기반의 심층 PR 리뷰를 수행하는 보안 감사 스킬입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/differential-review/`
*   🛠️ **핵심 역량**:
    *   **위험도 기반 스케일링**: PR의 파일 수와 중요도(Auth, Crypto 등)에 따라 분석 전략(DEEP/FOCUSED/SURGICAL)을 자동 전환합니다.
    *   **영향 반경(Blast Radius) 계산**: 커밋 히스토리를 추적하여 로직 변경이 미치는 연쇄적 위험성을 계산합니다.
    *   **공식 리포트 발행**: 대화창에 요약만 남기지 않고, 반드시 체계화된 마크다운 보안 감사 보고서를 생성합니다.
*   💬 **프롬프트 예시**: `"@differential-review 스킬로 이 인증 로직 리팩토링 PR을 리뷰해 줘. 대규모 코드베이스이므로 SURGICAL 전략을 사용해."`

---

### 3. 🏗️ @security-scanning-security-hardening
다중 보안 에이전트를 조율하여 애플리케이션부터 인프라까지 **Defense-in-Depth(심층 방어) 모델을 구축하는 오케스트레이터**입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/security-scanning-security-hardening/`
*   ✨ **핵심 역량**:
    *   **4단계 하드닝 프로세스**: 1단계(분석)부터 2단계(치명적 취약점 패치), 3단계(보안 제어 적용), 4단계(검증 및 SIEM 연동)까지 순차적으로 인프라를 강화합니다.
    *   **에이전트 조율(Coordination)**: 목적에 맞춰 모바일/프론트엔드/백엔드의 보안 담당 에이전트(`*-security-coder`)들을 호출해 구체적인 코드를 수정합니다.
*   💬 **프롬프트 예시**: `"@security-scanning-security-hardening 스킬을 사용해 현재 백엔드 API 서버에 대한 1~4단계 보안 강화 프로그램을 실행해."`

---

### 4. ⛓️ @solidity-security
재진입 공격(Reentrancy), 오버플로우, 접근 제어 우회 등을 원천적으로 차단하는 Web3 스마트 컨트랙트 보안 마스터입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/solidity-security/`
*   🌟 **핵심 역량**:
    *   **DeFi 보안 특화**: 이더리움/EVM 환경에서 발생할 수 있는 로직 결함, 오라클 조작 등을 철저하게 감사(Audit)합니다.
    *   **전용 플레이북 참조**: 저장된 `implementation-playbook.md`를 바탕으로 검증된 방어 코드를 작성합니다.
*   💬 **프롬프트 예시**: `"@solidity-security 스킬로 이 솔리디티 크라우드펀딩 컨트랙트에서 재진입 공격 취약점이 있는지 점검해 줘."`

---

### 5. 🏴‍☠️ @red-team-tactics
본격적인 공격자 시뮬레이션을 위해 **MITRE ATT&CK 프레임워크**만을 엄격하게 따르는 오펜시브 보안(Red Team) 전략가입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/red-team-tactics/`
*   🔪 **핵심 역량**:
    *   **침투 라이프사이클 시뮬레이션**: 정찰(Recon)부터 초기 접근, 수평 이동(Lateral Movement), 방어 회피 기술 등을 아우릅니다.
    *   **AD 환경 타겟팅**: Kerberoasting, Golden Ticket 등 Active Directory 상의 치명적인 공격 벡터를 테스트합니다.
    *   **방어 갭(Detection Gaps) 도출**: 공격이 성공했다면 아군의 어떤 방어 시스템(SIEM/IDS)이 실패했는지 명확히 짚어냅니다.
*   💬 **프롬프트 예시**: `"@red-team-tactics 스킬을 사용해 우리의 윈도우 인프라 내부에서 예상되는 수평 이동(Lateral Movement) 공격 시나리오를 구성해 봐."`

---

## 🌊 보안 우선 워크플로우

1.  **모델링**: `@security-auditor`로 가장 중요한 자산과 잠재적 위협을 식별합니다.
2.  **코드 감사**: 모든 코드 변경 사항에 대해 `@differential-review`를 수행합니다.
3.  **강화**: `@security-scanning-security-hardening`으로 발견된 취약점을 봉쇄합니다.
4.  **검증**: `@red-team-tactics`로 새롭게 구축된 보안 층을 실전처럼 테스트합니다.

---

## 🧭 탐색 (Navigation)

| [🏠 홈으로](../../README_KO.md) | [📓 기획 가이드](./planning.md) | [🎨 프론트엔드](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 백엔드](./backend.md) | [🛡️ 보안](./security.md) | [🧞 에이전트](./agents.md) |
| [🧪 QA 테스트](./qa_testing.md) | [📦 스킬 번들](./bundles.md) | [🌊 워크플로우](./workflows.md) |
| [🌐 English Version](../en/security.md) | | |

---
