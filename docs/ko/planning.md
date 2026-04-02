# 📓 기획 허브: 제품 전략 및 설계

이 가이드는 Antigravity Awesome Skills 라이브러리 중 가장 효과적인 **기획-우선(Planning-First)** 스킬들을 심층적으로 다룹니다.

---

## 🏗️ 핵심 기획 도구

### 1. 🧠 @brainstorming
"위험 제거 기계"입니다. 코드 한 줄을 작성하기도 전에 아이디어를 다각도로 검증하도록 설계되었습니다.

*   📂 **경로**: `~/.gemini/antigravity/skills/brainstorming/`
*   🔥 **활용 시나리오**:
    *   **MVP 범위 설정**: 출시를 위해 필요한 최소한의 요소를 정의합니다.
    *   **아키텍처 및 로직**: 복잡한 시스템과 데이터 흐름을 사전에 설계합니다.
    *   **ROI 분석**: 구현 가능성 대비 가치를 에이전트와 함께 평가합니다.
*   💬 **프롬프트 예시**: `"@brainstorming 스킬을 사용해 구독형 AI 뉴스레터 생성 서비스를 설계해줘. 사용자 온보딩과 API 연동에 집중해."`

---

### 2. 📋 @product-manager
단순한 기획 보조를 넘어 6가지 전문 지식, 30개 이상의 기획 프레임워크, SaaS 성과 지표를 꿰뚫고 있는 시니어 PM 에이전트입니다.

*   📂 **경로**: `~/.gemini/antigravity/skills/product-manager/`
*   🎯 **핵심 역량**:
    *   **검증된 프레임워크**: RICE 스코어링, MoSCoW, Kano 모델, Jobs-to-be-Done 지원.
    *   **전문 템플릿**: PRD(제품 요구사항 정의서), 원페이저, 회고 템플릿 내장.
    *   **SaaS 지표**: MRR, ARR, 이탈률(Churn), LTV, CAC 등 32가지 필수 지표 계산.
*   💬 **프롬프트 예시**: `"캘린더 연동 하이브리드 투두앱의 PRD를 작성해 주고, 초기 개발 항목을 MoSCoW 프레임워크로 분류해 줘."`

---

### 3. 🚀 @saas-mvp-launcher
아이디어를 최소 기능 제품(MVP)으로 구현해 가장 빠른 시간 내에 시장에 출시하기 위한 실행 전술과 기술 트리를 제공합니다.

*   📂 **경로**: `~/.gemini/antigravity/skills/saas-mvp-launcher/`
*   🛠️ **핵심 역량**:
    *   **검증 체크리스트**: 코드를 작성하기 전 아이디어를 엄격하게 검증하는 기준점 제시.
    *   **최적 기술 스택 (2026)**: Next.js 15, Tailwind, Supabase, Prisma, Clerk, Stripe 등 견고한 스택 추천.
    *   **아키텍처 스니펫**: 다중 테넌트 DB 모델, 인증 미들웨어, 결제 연동 표준 코드 제공.
    *   **사전 런칭 체크리스트**: 보안, SEO, 온보딩 로직 등 출시 직전 놓치기 쉬운 항목 점검.
*   💬 **프롬프트 예시**: `"B2B용 리뷰 관리 SaaS를 만들려고 해. 결제와 구독이 포함된 초기 DB 스키마(Prisma)를 짜줘."`

---

### 4. 📊 @business-analyst
추상적인 아이디어를 날카로운 숫자로 바꾸고, 데이터를 기반으로 시장성과 최적화 전략을 세워주는 비즈니스 데이터 분석가입니다.

*   📂 **경로**: `~/.gemini/antigravity/skills/business-analyst/`
*   📈 **핵심 역량**:
    *   **시장/고객 애널리틱스**: TAM/SAM/SOM 분석, 유저 세그먼테이션, A/B 테스트 프레임워크 설계.
    *   **재무 모델링**: 코호트 분석, LTV/CAC 최적화, 수익 모델(Unit Economics) 시나리오 기획.
    *   **KPI 프레임워크**: North Star(북극성) 지표 도출 및 OKR 설계, 데이터 대시보드 기획.
*   💬 **프롬프트 예시**: `"준비 중인 구독형 서비스의 TAM/SAM/SOM(시장 규모)을 분석해 줘."`

---

## 🌊 기획에서 실행으로 이어지는 워크플로우

기획 단계를 건너뛰는 것은 가장 큰 실수입니다. 다음 **"골든 패스(Golden Path)"**를 따르세요:

1.  **아이디어 선별**: `@brainstorming`으로 "무엇을(What)" 할지 탐색.
2.  **시장 검증**: `@business-analyst`로 "타당성(Market)" 확인.
3.  **구체화**: `@product-manager`로 "어떻게(How)" (PRD/유저 스토리) 정의.
4.  **실행 준비**: `@saas-mvp-launcher`로 "도구(Tools)" 선택 및 체크리스트 점검.

> [!IMPORTANT]
> **기획 결과물은 항상 문서화하세요.** 기획 결과를 프로젝트의 `docs/SPEC.md`나 `docs/PLAN.md`로 저장하면, 나중에 작업할 때 문맥을 잃지 않고 정확하게 수행할 수 있습니다.

---

## 🧭 탐색 (Navigation)

| [🏠 홈으로](../../README_KO.md) | [📓 기획 가이드](./planning.md) | [🎨 프론트엔드](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 백엔드](./backend.md) | [🛡️ 보안](./security.md) | [🧞 에이전트](./agents.md) |
| [🧪 QA 테스트](./qa_testing.md) | [📦 스킬 번들](./bundles.md) | [🌊 워크플로우](./workflows.md) |
| [🌐 English Version](../en/planning.md) | | |

---
