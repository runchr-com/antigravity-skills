# 🐍 백엔드 & 데이터 허브: 확장 가능한 로직

이 가이드는 고성능 API 구축, 견고한 데이터 모델링, 최적화된 데이터베이스 스키마 설계를 위한 스킬들을 다룹니다.

---

## 🏗️ 핵심 백엔드 도구

### 1. 🐍 @python-pro
최신 Python 3.12+ (2024/2025 에코시스템)에 정통한 시니어 백엔드 아키텍트입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/python-pro/`
*   🎯 **핵심 역량**:
    *   **모던 툴체인 도입**: 레거시 도구 대신 `uv`(패키지), `ruff`(린터/포매터), `pyright`(타이핑) 등의 최신 툴을 사용합니다.
    *   **고성능 비동기 설계**: `asyncio`, FastAPI 및 백그라운드 워커를 활용한 고성능 아키텍처를 구축합니다.
    *   **프로덕션 레벨 코드**: 90% 이상의 테스트 커버리지, 엄격한 예외 처리, 멀티스테이지 Docker 빌드를 강제합니다.
*   💬 **프롬프트 예시**: `"@python-pro 스킬로 이 데이터 처리 스크립트를 리팩토링해 줘. uv와 ruff를 적용하고 Python 3.12 구조적 패턴 매칭을 써 줘."`

---

### 2. 🛣️ @fastapi-router-py
확립된 베스트 프랙티스에 따라 FastAPI 라우터를 빠르고 정확하게 생성하는 스캐폴딩 스킬입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/fastapi-router-py/`
*   🛠️ **핵심 역량**:
    *   **라우터 패턴 준수**: 깔끔한 URL 계층 구조를 유지하며 라우터를 올바르게 연결합니다.
    *   **강력한 타입 반환**: 모든 엔드포인트에 정확한 Pydantic `response_model`을 바인딩합니다.
    *   **정확한 HTTP 상태 코드**: POST에는 `201`, DELETE에는 `204` 등 RESTful 원칙을 엄격히 적용합니다.
*   💬 **프롬프트 예시**: `"@fastapi-router-py 스킬로 인증(회원가입/로그인) 라우터를 생성해 줘. 정확한 401 예외와 상태 코드를 갖춰야 해."`

---

### 3. 💎 @pydantic-models-py
명확한 API 계약(Contract) 관리를 위해 Pydantic(v2)의 **멀티 모델 패턴(Multi-Model Pattern)**을 마스터했습니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/pydantic-models-py/`
*   ✨ **핵심 역량**:
    *   **계층화된 검증모델**: 데이터 구조를 `Base`, `Create`(필수), `Update`(선택), `Response`, `InDB`로 완벽히 분리합니다.
    *   **자동 직렬화**: 프론트엔드와의 매끄러운 통신을 위해 `camelCase` alias를 자동으로 구성합니다.
*   💬 **프롬프트 예시**: `"@pydantic-models-py 스킬을 사용해 'Workspace' 도메인의 멀티 모델 패턴을 작성해. camelCase 변환도 잊지 마."`

---

### 4. 🗄️ @database-design
논리적 구조, 정규화, 그리고 상황에 맞는 최적의 선택을 돕는 데이터베이스 아키텍처 조언자입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/database-design/`
*   🌟 **핵심 역량**:
    *   **맥락 기반 선택**: 무조건 PostgreSQL만 쓰는 것이 아니라, SQLite, Neon 등 컨텍스트에 맞는 DB와 ORM(Prisma, Drizzle 등)을 선택합니다.
    *   **안티 패턴 차단**: 인덱스 누락, `SELECT *` 남용, N+1 쿼리 등의 치명적 실수를 설계 단계에서 방지합니다.
*   💬 **프롬프트 예시**: `"@database-design 스킬로 현재 Drizzle ORM 스키마를 리뷰해 줘. 읽기가 잦은 테이블인데 인덱스가 적절한지 봐줘."`

---

### 5. 💾 @sql-pro
고성능 튜닝, OLAP/OLTP 최적화, 클라우드 네이티브 데이터베이스에 특화된 심화 SQL 스페셜리스트입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/sql-pro/`
*   📈 **핵심 역량**:
    *   **고급 분석 쿼리**: 복잡한 CTE(공통 테이블 표현식), 윈도우 함수, 시계열 데이터를 분석하는 Raw SQL을 자유자재로 작성합니다.
    *   **실행 계획 분석**: `EXPLAIN ANALYZE`를 개념적으로 수행하여 스캔을 피하는 완벽한 복합 인덱스 전략을 짭니다.
    *   **클라우드 데이터 웨어하우스**: Snowflake, BigQuery 등의 아키텍처에 최적화된 SQL을 제공합니다.
*   💬 **프롬프트 예시**: `"@sql-pro 스킬로 이 분석용 쿼리의 성능을 최적화해 줘. 순차 스캔(Sequential scan)을 막을 수 있는 조치 방법과 복합 인덱스를 제시해."`

---

## 🌊 백엔드 우선 워크플로우

1.  **모델링**: `@pydantic-models-py`로 데이터의 형태와 규격을 정의합니다.
2.  **데이터 저장**: `@database-design`으로 정의된 데이터를 DB 스키마에 매핑합니다.
3.  **API 구축**: `@fastapi-router-py`로 데이터에 접근하기 위한 엔드포인트를 만듭니다.
4.  **최적화**: `@python-pro` + `@sql-pro`로 로직의 효율성과 성능을 극대화합니다.

---

## 🧭 탐색 (Navigation)

| [🏠 홈으로](../../README_KO.md) | [📓 기획 가이드](./planning.md) | [🎨 프론트엔드](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 백엔드](./backend.md) | [🛡️ 보안](./security.md) | [🧞 에이전트](./agents.md) |
| [🧪 QA 테스트](./qa_testing.md) | [📦 스킬 번들](./bundles.md) | [🌊 워크플로우](./workflows.md) |
| [🌐 English Version](../en/backend.md) | | |

---
