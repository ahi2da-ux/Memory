# 짠테크 앱 아키텍처 및 데이터 흐름 재정의 계획
## 🎯 목표: 생활형 성장 RPG 기반의 기술 아키텍처 및 데이터 흐름 개선
### 1. 아키텍처 제안
- **추천 구조:** Presentation, Domain, Data Layer 분리 (DDD 개념 도입)
- **핵심 변경 사항:** 기존 지도/로그 기능은 '행동 유발' 역할로 축소하고, RPG 상태 관리(Character, Village, Achievement)를 위한 별도의 데이터 계층을 구축.

### 2. 데이터 모델 재정의 (Supabase Schema Refinement)
- **추가 엔티티:** `characters`, `villages`, `achievements` 테이블 정의.
- **관계 설정:** 모든 성장 데이터는 `users` 테이블과 명확히 연결되어야 함.

### 3. 트랜잭션 및 로깅 개선
- **핵심 원칙:** 모든 행동 로그는 **원자적(Atomic)으로** 처리되어야 하며, 이 로그를 기반으로 Domain Layer에서 복합적인 성장 계산을 수행해야 함.

### 4. 즉각적인 개발 액션 플랜 (Immediate Action Plan for Developer)
1. **Schema Migration:** Supabase에 새로운 테이블 스키마를 적용하는 마이그레이션 스크립트 작성.
2. **Core Logic Implementation:** `Domain Layer`에 성장 공식 및 보상 지급 로직을 캡슐화하고 단위 테스트 우선 수행.
3. **E2E QA Scenario Expansion:** RPG 관련 상태 변화(레벨업, 마을 점수)를 포함하는 통합 검증 시나리오 확장.