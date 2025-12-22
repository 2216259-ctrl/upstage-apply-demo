# [Tech Stack] Research Methodology & Service Architecture

본 문서는 **[PRD] 올리브영 옴니채널 유저 경험 분석** 프로젝트를 수행하기 위해 활용된 **리서치 기술 스택(Research Tech)**과, 제안된 솔루션을 실현하기 위한 **서비스 기술 스택(Service Tech)**을 정의합니다.

---

## 1. Research & Analytics Stack (Research Phase)
> **Objective:** 데이터 기반의 정교한 문제 정의 및 가설 검증

### **A. Generative AI Research Tool**
*   **Name:** **Popow.ai** (Core Tool)
*   **Usage:**
    *   **AI Survey Architect:** 가설(O2O 이탈)을 입력하면 관련성 높은 문항을 자동 생성.
    *   **Adaptive Probing:** 응답자의 답변에 따라 실시간으로 심층 질문을 던져 '진짜 이유' 발굴.
    *   **Automated Coding:** 1,000건 이상의 주관식(서술형) 응답을 NLP(자연어 처리)로 분석하여 `재고 불일치`, `직원 응대 부담` 등의 핵심 키워드로 자동 분류.

### **B. Data Analytics & Visualization**
*   **Python (Pandas/Scikit-learn):**
    *   Popow.ai의 서베이 데이터와 내부 구매 데이터(가상)를 병합(Merge)하여 상관관계 분석.
    *   *예: "매장 재고 불만"을 언급한 유저의 실제 앱 내 "장바구니 포기율" 상관계수 산출.*
*   **Tableau / Excel:**
    *   User Journey Map 시각화 및 세그먼트별 이탈률 대시보드 구현.

---

## 2. Proposed Solution Tech Stack (Implementation Phase)
> **Objective:** PRD에서 제안한 [실시간 재고 신호등] 및 [언택트 큐레이션] 구현을 위한 기술적 타당성 검토

### **A. Real-time Inventory Traffic Light (App)**
매장 재고의 '정확도'와 '실시간성'을 보장하기 위한 아키텍처.

*   **Backend:**
    *   **Redis (Cache):** 매장별 재고 데이터의 초고속 조회를 위한 인메모리 캐시 적용.
    *   **Near Real-time Sync API:** POS 시스템의 재고 변동 사항을 5분 단위가 아닌 '이벤트 기반(Event-driven)'으로 앱에 반영.
*   **Frontend (App):**
    *   **UX UI:** 재고 수량을 단순히 보여주는 것이 아니라, `여유(Green)` / `임박(Orange)` / `품절(Red)`의 직관적 UI로 변환하여 표시.

### **B. Untact Curation Intelligence (Store)**
직원 도움 없이도 고도화된 경험을 제공하기 위한 오프라인 기술.

*   **AI Vision / AR:**
    *   **Personal Color Analysis:** 키오스크/태블릿 카메라를 통해 고객의 피부 톤을 분석하고 적합한 제품 추천 (OpenCV, TensorFlow 활용).
    *   **Virtual Try-on:** 립/치크 제품을 실제 바르지 않고도 증강현실(AR)로 테스트.
*   **IoT Sensors (Optional):**
    *   테스터 제품 하단에 압력 센서를 부착하여, 특정 제품의 테스트 빈도(집어 듦 횟수) 데이터 수집.
