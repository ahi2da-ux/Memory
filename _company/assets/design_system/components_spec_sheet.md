# 📊 짠테크맵 UI 컴포넌트 스펙 시트 V1.0

## 🎨 컬러 팔레트 (Color Palette)
*   **Primary:** `#007AFF` (강조 및 액션)
*   **Secondary:** `#4CAF50` (성장, 목표 달성)
*   **Neutral-Light:** `#EFEFF4` (배경, 보조)
*   **Text-Dark:** `#212121` (본문 텍스트)

## ✍️ 타이포그래피 (Typography)
*   **메인 폰트:** Pretendard (가독성 최우선)
*   **헤드라인 (H1/H2):** Bold, 32pt / 24pt. 목표 달성 시 강조를 위해 '글자 간격(letter-spacing)'을 미묘하게 조정하여 고급스러움을 추가함.

## ✨ 핵심 컴포넌트 스펙
### 1. CTA Button (Call To Action)
*   **Primary:** `background: #007AFF`, `border-radius: 8px`. **Hover Effect**: 배경색이 약간 어두워지며(Opacity -5%) 그림자가 미묘하게 생김.
*   **Secondary:** `background: none`, `border: 1px solid #CCCCCC`.

### 2. Progress Tracker Component (자산/목표 추적)
*   **구조:** `<Progress Bar (Width: X%)> + <Completion Text>`
*   **애니메이션 스펙:** 로딩 시, 바가 좌측에서 우측으로 부드럽게 채워지며(0.8초), 100%에 도달하면 Secondary 컬러로 깜빡임 효과를 준다.

### 3. Info Card (정보 카드)
*   **구조:** `[Border] + [Icon] + [Title/Content]`
*   **활용 예시:** '오늘의 절약 미션', 'OO 지역 숨은 할인 정보' 등 부가 정보를 담는 데 사용하며, 배경에 그림자(Shadow-soft)를 적용하여 깊이감을 부여함.