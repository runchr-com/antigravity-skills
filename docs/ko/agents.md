# 🧞 AI 에이전트 허브: 자율 지능

이 가이드는 자율형 AI 에이전트 시스템 및 모델 컨텍스트 프로토콜(MCP) 서버의 설계, 구축 및 평가에 관한 스킬들을 다룹니다.

---

## 🏗️ 핵심 AI 에이전트 도구

### 1. 🧞 @agent-orchestrator
생태계 내의 모든 에이전트를 조율하고 스킬 레지스트리 역할을 하는 중앙 메타 스킬입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/agent-orchestrator/`
*   🎯 **핵심 역량**:
    *   **자동 탐색(Auto-Discovery)**: MD5 캐싱을 통해 사용 가능한 모든 스킬을 동적으로 스캔하고 등록합니다.
    *   **알고리즘 매칭**: 역량 태그와 트리거 키워드를 활용해 사용자 요청에 가장 적합한 스킬을 매칭합니다.
    *   **워크플로우 패턴**: 순차적 파이프라인(Sequential), 병렬 실행(Parallel), 주/보조(Primary+Support) 모델로 스킬들을 오케스트레이션합니다.
*   💬 **프롬프트 예시**: `"@agent-orchestrator 스킬로 이커머스 데이터를 추출하기 위한 최적의 스킬들을 찾고, 결과를 메시지로 전송하는 순차적 파이프라인을 설계해줘."`

---

### 🧠 2. @autonomous-agent-patterns
Cline, OpenAI Codex 등의 아키텍처에서 영감을 받은 자율 코딩 에이전트 구축용 디자인 패턴입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/autonomous-agent-patterns/`
*   🛠️ **핵심 역량**:
    *   **에이전트 루프**: *생각(Think) → 결정(Decide) → 행동(Act) → 관찰(Observe)* 로 이어지는 자율 루프 구조를 구현합니다.
    *   **컨텍스트 및 메모리**: 복잡한 컨텍스트 주입 및 상태 저장/복구(Checkpoint/Resume) 알고리즘을 관리합니다.
    *   **샌드박싱 및 브라우저**: 격리된 환경에서의 코드 실행과 시각적 브라우저 자동화를 위한 아키텍처 패턴을 제공합니다.
*   💬 **프롬프트 예시**: `"@autonomous-agent-patterns 스킬을 사용해, 기획에는 빠른 모델을 사용하고 코드 생성에는 똑똑한 모델을 사용하는 자율 에이전트 루프를 설계해봐."`

---

### ⚒️ 3. @agent-tool-builder
LLM과 외부 도구 사이의 인터페이스를 설계하여 환각(Hallucination)이나 치명적 오류를 방지하는 전문가입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/agent-tool-builder/`
*   ✨ **핵심 역량**:
    *   **스키마 설계(Schema Design)**: LLM이 완벽하게 이해할 수 있도록 모호함 없는 JSON 스키마를 제작합니다.
    *   **에러 힐링(Error Healing)**: 조용히 실패하는(Silent failure) 대신, 에이전트가 스스로 복구할 수 있는 명시적인 에러 메시지를 설계합니다.
    *   **안전 가드레일**: 위험한 도구 호출에 대해 권한 수준(AUTO, ASK_ONCE, ASK_EACH)을 강제합니다.
*   💬 **프롬프트 예시**: `"@agent-tool-builder 스킬을 활용하여, Google Sheets 데이터 추출 도구의 JSON 스키마와 에러 처리 로직을 설계해줘."`

---

### 📏 4. @agent-evaluation
"정답"이 하나만 존재하지 않는 환경에서 LLM 에이전트의 성능과 신뢰성을 평가하기 위한 벤치마킹 프레임워크입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/agent-evaluation/`
*   🌟 **핵심 역량**:
    *   **통계적 검증**: 이분법적인 합격/불합격이 아니라, 테스트를 여러 번 반복하여 결과의 분포도를 분석합니다.
    *   **행동 계약(Behavioral Contracts)**: 퇴행(Regression)을 방지하기 위해 에이전트가 반드시 지켜야 할 행동 불변성을 정의하고 테스트합니다.
    *   **적대적 테스트(Adversarial Testing)**: 프로덕션 환경에서의 신뢰성을 보장하기 위해 의도적으로 에이전트의 로직을 파훼하려 시도합니다.
*   💬 **프롬프트 예시**: `"@agent-evaluation 스킬을 사용해 우리가 새로 만든 리서치 에이전트의 신뢰성을 검증할 적대적 테스트(Adversarial test) 프레임워크를 설계해줘."`

---

### 🏛️ 5. @mcp-builder
LLM과 로컬 환경 또는 외부 API를 연결하는 모델 컨텍스트 프로토콜(MCP) 서버 구축 전문가 시스템입니다.
*   📂 **경로**: `~/.gemini/antigravity/skills/mcp-builder/`
*   🔪 **핵심 역량**:
    *   **프로토콜 구현(Protocol Implementation)**: MCP 사양에 맞춰 Streamable HTTP 또는 stdio 전송 방식을 올바르게 구현합니다.
    *   **SDK 마스터**: FastMCP 프레임워크를 사용하여 안정적이고 관용적인 TypeScript 및 Python 코드를 작성합니다.
    *   **읽기/쓰기 작업 관리**: 도구에 `readOnlyHint`, `destructiveHint` 등의 적절한 어노테이션을 추가하고 페이징(Pagination)을 처리합니다.
*   💬 **프롬프트 예시**: `"@mcp-builder 스킬을 이용해, 내 로컬 JIRA 이슈들을 에이전트에게 안전하게 노출하는 TypeScript 기반의 MCP 서버 초안을 작성해줘."`

---

## 🌊 AI 에이전트 우선 워크플로우

1.  **아키텍처 설계**: `@agent-orchestrator`로 전체 시스템 흐름을 설계합니다.
2.  **패턴 선정**: `@autonomous-agent-patterns`로 추론 루프를 선택합니다.
3.  **도구 개발**: `@agent-tool-builder` + `@mcp-builder`로 필요한 기능을 구축합니다.
4.  **최적화**: `@agent-evaluation`을 통해 성능을 반복적으로 개선합니다.

---

## 🧭 탐색 (Navigation)

| [🏠 홈으로](../../README_KO.md) | [📓 기획 가이드](./planning.md) | [🎨 프론트엔드](./frontend.md) |
| :---: | :---: | :---: |
| [🐍 백엔드](./backend.md) | [🛡️ 보안](./security.md) | [🧞 에이전트](./agents.md) |
| [🧪 QA 테스트](./qa_testing.md) | [📦 스킬 번들](./bundles.md) | [🌊 워크플로우](./workflows.md) |
| [🌐 English Version](../en/agents.md) | | |

---
