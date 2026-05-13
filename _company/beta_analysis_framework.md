# 📊 베타 유저 확보 및 분석 프레임워크 (v1.0)
## I. 목표 정의: 수익화 가설 검증 (Business Goal)
*   **최종 목표:** MVP 출시 후 4주 내, '짠테크맵'을 이용한 사용자당 평균 전환율(Conversion Rate) 측정 $\rightarrow$ 월 매출 $X$ 달성 가능성 입증.
*   **핵심 지표(North Star Metric):** **Active Value Loop Completion Count (AVLC)**: 사용자가 [행동 A] $\rightarrow$ [보상 획득] $\rightarrow$ [재참여 행동 B]의 순환 고리(Loop)를 완료한 총횟수.

## II. 유입 채널별 목표 및 KPI 매핑
| 출처 (Channel) | 주력 콘텐츠 Hook (Content Focus) | 예상 Funnel 진입 지점 | 1차 핵심 KPI (Leading Indicator) | 2차 수익성 KPI (Lagging Indicator) | 측정 필요 Action (Tracking) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Instagram** | '시각적 만족도' 기반의 목표 달성 후기(Before/After). | Onboarding / 핵심 기능 사용 초기 진입. | 릴스 시청 완료율 > 70% & 프로필 클릭률 (CTR) | *첫 포인트 지급 유저 비율* (재방문 유발 여부) | UTM Link 및 Instagram Insights 활용. |
| **Reddit** | '실제 절약 경험 공유' 및 심층 분석 기반의 신뢰성 콘텐츠. | 정보 탐색/챌린지 참여(정보 습득 후 행동). | 게시글 하단 댓글 참여율 (질문 수) & 앱 다운로드 비율 | *미션 수행 완료 횟수* (Deep engagement) | 고유 커뮤니티 코드 또는 랜딩 페이지 필터링. |

## III. 사용자 여정 Funnel 및 측정 지표 상세 설계
**[A] 유입 (Acquisition)** $\rightarrow$ **[B] 활성화 (Activation)** $\rightarrow$ **[C] 수익화/재참여 (Retention/Monetization)**

### 1. [A] 유입 (Acquisition): 초기 관심 유발
*   **핵심 지표:** 채널별 다운로드 전환율 ($\text{CTR} \times \text{CVR}$)
*   **측정 가설:** Instagram은 *감성적 동기*에 의한 유저를, Reddit은 *이성적/실질적 목표*에 의한 유저를 주력으로 확보할 것이다.

### 2. [B] 활성화 (Activation): 핵심 기능 사용 입증
*   **핵심 지표:** **Time to First Core Action (TTFCA)**: 앱 설치 후, 포인트 지급을 위한 '첫 미션 완료'에 걸린 평균 시간. (가장 중요)
*   **측정 목표:** 유저가 튜토리얼 없이도 자발적으로 가장 중요한 가치 생성 루프(예: 장소 정보 입력 $\rightarrow$ 포인트 적립)를 경험하도록 설계해야 함.

### 3. [C] 수익화/재참여 (Monetization/Retention): 비즈니스 가설 검증
*   **핵심 지표:** **Premium Feature Interaction Rate (PFIR)**: 유료 기능(가령, 특정 필터링/추가 정보)을 확인하거나 사용하려는 시도 횟수.
    *   $\text{KPI} = \frac{\text{유료 기능을 보고 이탈한 사용자 수}}{\text{활성 사용자 수}} \times 100$ (이탈 자체가 수요 증거임).
*   **측정 지표:** **Cohort Retention Rate by Acquisition Source**: 특정 유입 채널(Reddit vs. Insta)에서 유입된 그룹별로, 7일차/30일차 재사용률 비교.

## IV. 다음 단계 액션 플랜 (Actionable Next Step)
1.  **[Developer]**: 위 Funnel의 모든 측정 지표(TTFCA, PFIR 등)가 Supabase 백엔드 레벨에서 트래킹 가능한 이벤트로 구현되었는지 QA를 재실행한다.
2.  **[Designer]**: 각 KPI 단계별로 사용자에게 '다음 행동을 유도하는 CTA' 디자인 가이드라인을 강화하여 전달한다.
3.  **[Writer/Insta]**: 위의 1차 핵심 KPI(Leading Indicator)에 초점을 맞춘 콘텐츠를 제작하고 배포한다.