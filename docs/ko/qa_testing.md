# 🧪 QA & 테스트 허브: 품질 보증

이 가이드는 자동화된 테스트, 브라우저 검증 및 엄격한 코드 품질 유지를 위한 스킬들을 다룹니다.

---

## 🏗️ 핵심 QA & 테스트 도구

### 1. 🧪 @testing-qa
단위 테스트(Unit test)부터 최종 품질 게이트(Quality gates)까지 조율하는 포괄적인 8단계 테스트 워크플로우 번들입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/testing-qa/`
*   🎯 **핵심 역량**:
    *   **테스팅 피라미드(Testing Pyramid)**: 70% 단위 테스트, 20% 통합 테스트, 10% E2E 테스트라는 표준 전략을 구조화합니다.
    *   **단계별 자동화**: 단위, 통합, E2E, 웹 브라우저, 그리고 성능 테스트 단계를 차례대로 안내합니다.
    *   **품질 게이트 체크리스트**: 테스트 커버리지 80% 이상, 린트(Linting) 통과, 코드 리뷰 완료 등을 강제합니다.
*   💬 **프롬프트 예시**: `"@testing-qa 스킬로 이 새로운 결제 처리 기능에 대한 포괄적인 테스팅 피라미드와 테스트 스위트를 설계해줘."`

---

### 🎭 2. @e2e-testing
Playwright 기반의 브라우저 자동화에 중점을 둔 7단계 심층 엔드투엔드(E2E) 테스트 워크플로우입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/e2e-testing/`
*   🛠️ **핵심 역량**:
    *   **구현 및 자동화**: 페이지 객체(Page Objects) 생성, 동적 콘텐츠 대기, 헤드리스(Headless) 브라우저 구성을 자동화합니다.
    *   **시각적 회귀 검증(Visual Regression)**: 베이스라인 이미지를 캡처하고 `@ui-visual-validator`를 이용해 UI 픽셀 단위의 변화를 검증합니다.
    *   **크로스 브라우저 & CI/CD**: Chromium, Firefox, WebKit 기반 테스트와 GitHub Actions에서의 병렬 실행을 설정합니다.
*   💬 **프롬프트 예시**: `"@e2e-testing 스킬로 사용자 로그인 및 결제 흐름을 점검하고, 크로스 브라우저 시각적 회귀 테스트까지 포함하는 Playwright 스크립트를 만들어줘."`

---

### 🔴 3. @tdd-workflow
TDD(테스트 주도 개발)의 핵심인 **RED(실패) → GREEN(성공) → REFACTOR(리팩토링)** 사이클을 엄격하게 강제하는 전문가입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/tdd-workflow/`
*   ✨ **핵심 역량**:
    *   **위대한 3원칙(Three Laws)**: 오직 실패하는 테스트를 통과시키기 위한 최소한의 프로덕션 코드만 작성하도록 제어합니다.
    *   **AAA 패턴**: 모든 테스트를 Arrange(준비), Act(실행), Assert(검증) 단계로 명확히 분리합니다.
    *   **YAGNI 원칙 적용**: "테스트가 곧 스펙(Specification)"이라는 철학 아래, Green 단계에서의 불필요한 과잉 엔지니어링을 차단합니다.
*   💬 **프롬프트 예시**: `"@tdd-workflow 스킬의 가이드에 따라 새로운 '주문 내역' 기능을 개발할게. 가장 먼저 RED 단계의 실패하는 테스트부터 작성해줘."`

---

### 🌐 4. @webapp-testing
로컬에서 실행 중인 SPA, 동적 렌더링 웹 애플리케이션을 파이썬 Playwright로 정교하게 테스트하는 특화 스킬입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/webapp-testing/`
*   🌟 **핵심 역량**:
    *   **라이프사이클 관리**: `scripts/with_server.py`를 활용해 테스트용 로컬 서버를 자동으로 띄우고 종료합니다.
    *   **정찰 후 조치(Recon-Then-Action)**: 클릭 전에 반드시 `networkidle`을 기다리고, 렌더링된 DOM의 스냅샷을 찍어 정확한 선택자(Selector)를 확인하도록 강제합니다.
    *   **블랙박스 실행**: LLM의 컨텍스트 윈도우가 낭비되지 않도록 복잡한 브라우저 조작 코드를 외부 스크립트로 격리해 실행합니다.
*   💬 **프롬프트 예시**: `"@webapp-testing 스킬로 로컬 서버를 띄운 뒤, localhost:5173의 '제출' 버튼이 잘못된 입력 시 비활성화되는지 확인해줘."`

---

### 🛡️ 5. @lint-and-validate
작업을 "완료" 상태로 넘기기 전, 반드시 거쳐야 하는 최후의 코드 품질 수문장(Quality Gate)입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/lint-and-validate/`
*   🔪 **핵심 역량**:
    *   **품질 루프(Quality Loop)**: *작성 → 감사(Audit) → 분석 → 수정* 의 무한 루프를 통해 결점을 없앱니다.
    *   **생태계별 유효성 검사**: `npm run lint`, `tsc --noEmit`뿐만 아니라 파이썬의 `ruff`, `bandit`, `mypy` 등 각 포맷에 맞는 린팅을 수행합니다.
    *   **엄격한 차단(Strict Blocking)**: "FINAL AUDIT REPORT"가 실패할 경우 어떠한 코드 커밋이나 작업 완료 선언도 절대 허용하지 않습니다.
*   💬 **프롬프트 예시**: `"커밋하기 전에 @lint-and-validate 스킬로 프로젝트 전체 코드가 우리의 품질 표준을 통과하는지 유효성 검사를 실행해줘."`

---

## 🌊 QA 우선 워크플로우

1.  **Red 단계**: `@tdd-workflow`로 실패하는 테스트 케이스를 먼저 작성합니다.
2.  **구현 단계**: 테스트가 통과될 때까지 기능을 개발합니다.
3.  **품질 검사**: `@lint-and-validate`로 코드 품질과 스타일을 점검합니다.
4.  **실제 환경 검증**: `@e2e-testing` + `@webapp-testing`으로 실제 브라우저 환경에서 최종 확인합니다.

---

## 🧭 탐색 (Navigation)

| [🏠 홈으로](../../README_KO.md) | [📓 기획 가이드](./planning.md) | [🎨 프론트엔드](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 백엔드](./backend.md) | [🛡️ 보안](./security.md) | [🧞 에이전트](./agents.md) |
| [🧪 QA 테스트](./qa_testing.md) | [📦 스킬 번들](./bundles.md) | [🌊 워크플로우](./workflows.md) |
| [🌐 English Version](../en/qa_testing.md) | | |

---
