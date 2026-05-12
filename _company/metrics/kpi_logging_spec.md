# 💾 필수 트랜잭션 KPI 로깅 스펙 (최종 확정)
모든 핵심 사용자 행동(로그인, 포인트 지급, 번들 구매 등) 발생 시 아래 필드를 Supabase의 `kpi_log` 테이블에 기록해야 합니다.

## 🎯 로깅 항목 정의
1.  **user_id:** [필수] 트랜잭션 주체 (Auth 연동).
2.  **timestamp:** [필수] 트랜잭션 발생 시각.
3.  **event_type:** [필수] 'login', 'point_earn', 'bundle_purchase', 'challenge_start' 등 명확한 이벤트 코드.
4.  **metric_value:** [필수] 해당 트랜잭션의 핵심 값 (예: 포인트 지급액, 구매 금액).
5.  **source_channel:** [선택/핵심] 사용자가 유입된 채널 ('youtube', 'instagram', 'direct'). **(획득 경로 추적 필수)**
6.  **bundle_variant:** [필수] 만약 번들 관련 이벤트라면, 어떤 버전인지 기록 (A/B 테스트 식별용).

## 💡 개발팀 요청 사항
`source_channel`은 반드시 분석에 활용될 수 있도록 구조화되어야 하며, 트랜잭션 발생 시점과 함께 로깅되는 것을 E2E QA 과정에서 최종 점검해야 합니다.
---