# [Schedule] Project Task List
> **Objective:** 올리브영 O2O 이탈 분석 및 개선 전략 수립을 위한 단계별 실행 계획

---

## **Phase 1: Research Preparation (Week 1)**
> **Goal:** 조사를 위한 데이터 환경 셋팅 및 설문 설계

### **Epic 1. Hypotheses Setting**
- [ ] **Task 1-1:** `Ideation.md` 기반 상세 가설 수립 (재고 정확도 vs 직원 응대 부담)
- [ ] **Task 1-2:** 세그먼트 정의 (Target: 2030 여성, 최근 3개월 앱 접속 O / 매장 구매 X)

### **Epic 2. Data Collection Setup (Popow.ai)**
- [ ] **Task 2-1:** Popow.ai 서베이 문항 초안 생성 (Pre-Survey)
- [ ] **Task 2-2:** Logic 점검 (응답에 따른 분기 처리: Branching Logic)
- [ ] **Task 2-3:** Pilot Test 진행 및 문항 **Fine-tuning**

---

## **Phase 2: Execution & Analysis (Week 1~2)**
> **Goal:** 데이터 수집 및 Popow.ai 기반 통합 분석

### **Epic 3. Quantitative Analysis (Internal Data)**
- [ ] **Task 3-1:** 앱 로그 데이터 추출 (장바구니 전환율, 매장 픽업 포기율)
- [ ] **Task 3-2:** 가상 데이터셋 생성 (Python Faker 활용) *※ Portfolio용*
- [ ] **Task 3-3:** 이탈 유저의 주요 행동 패턴 시각화 (Funnel Analysis)

### **Epic 4. Qualitative Analysis (Popow.ai)**
- [ ] **Task 4-1:** 설문 배포 및 응답 수집 (가상 시뮬레이션)
- [ ] **Task 4-2:** **Automated Coding** 기능으로 서술형 응답 키워드 추출 (`#재고없음`, `#눈치보임`)
- [ ] **Task 4-3:** Sentiment Analysis (감성 분석) 결과 리포트 추출

---

## **Phase 3: Strategy & Reporting (Week 2)**
> **Goal:** 인사이트 도출 및 비즈니스 액션 제안

### **Epic 5. Insight Synthesis**
- [ ] **Task 5-1:** 정량/정성 데이터 결합 (Integrated Analysis)
- [ ] **Task 5-2:** 핵심 문제점(Root Cause) 2가지 확정
    1.  Information Gap (재고)
    2.  Psychological Barrier (직원 응대)

### **Epic 6. Solution Design (Action Plan)**
- [ ] **Task 6-1:** 실시간 재고 신호등(Traffic Light) UI 기획안 작성
- [ ] **Task 6-2:** 언택트 큐레이션(Untact Curation) 존/키트 구성안 작성

### **Epic 7. Final Deliverable**
- [ ] **Task 7-1:** 최종 결과 보고서 작성 (`docs/Report.md` 예정)
- [ ] **Task 7-2:** 포트폴리오용 요약 장표(Deck) 구성
