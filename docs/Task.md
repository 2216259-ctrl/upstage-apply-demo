# Project Tasks — Phase / Epic / Task

이 문서는 PRD(`docs/PRD.md`)와 TechStack(`docs/TechStack.md`)을 기반으로 프로젝트를 단계별로 실행할 수 있도록 Phase, Epic, Task로 분해한 체크리스트입니다.

사용법: 각 Phase를 순차적으로 진행하며 Epic과 Task를 체크하세요. 각 Task는 책임자(Owner), 예상기간(Estimate), 선행조건(Dependency), 완료기준(Acceptance Criteria)을 포함합니다.

---

## Phase 1: Discovery (Week 1)
- Epic 1.1: Stakeholder Alignment
  - Task 1.1.1: 스테이크홀더 인터뷰 (PO, MD, 데이터팀) — Owner: 리서처, Estimate: 1d, Dependency: 없음, Acceptance: 요구사항·가설 목록 합의
  - Task 1.1.2: 목표·성공지표 확정 워크샵 — Owner: 리서처/PO, Estimate: 0.5d, Dependency: 1.1.1, Acceptance: KPI 목록 문서화
- Epic 1.2: Research Plan
  - Task 1.2.1: 리서치 플랜 초안 작성(가설, 표본, 방법론) — Owner: 리서처, Estimate: 1d, Dependency: 1.1.1, Acceptance: `docs/research_plan.md` 초안
  - Task 1.2.2: 윤리/동의서 템플릿 준비(녹취·개인정보) — Owner: 리서처, Estimate: 0.5d, Dependency: 법무/PO 확인, Acceptance: 서명 가능한 템플릿

## Phase 2: Setup & Instrumentation (Week 1)
- Epic 2.1: 데이터 파이프라인 설정
  - Task 2.1.1: 이벤트 스키마 정의(GA4 / custom events) — Owner: 데이터팀/리서처, Estimate: 1d, Dependency: 1.1.2, Acceptance: 이벤트 명세서(PRD 연동)
  - Task 2.1.2: 로그 수집·샘플 확보(샘플 CSV) — Owner: 데이터팀, Estimate: 1d, Dependency: 2.1.1, Acceptance: 익명화된 샘플 데이터 제공
- Epic 2.2: 도구 세팅
  - Task 2.2.1: 설문 템플릿 생성(Typeform/Google Forms) — Owner: 리서처, Estimate: 0.5d, Dependency: 1.2.1, Acceptance: 배포용 링크 준비
  - Task 2.2.2: 인터뷰 녹취/전사 파이프라인(Descript/Otter) 구성 — Owner: 리서처, Estimate: 0.5d, Dependency: 계정 확보, Acceptance: 전사 예시 파일 생성

## Phase 3: Data Collection (Week 2-3)
- Epic 3.1: 정성 데이터 수집
  - Task 3.1.1: 인터뷰 리크루팅(페르소나 기준) — Owner: 리서처, Estimate: 3d, Dependency: 1.2.1, Acceptance: 10~15명 모집
  - Task 3.1.2: 인터뷰 진행 및 녹취 — Owner: 리서처, Estimate: 7d(병렬), Dependency: 3.1.1, Acceptance: 전사 파일 및 요약 노트
  - Task 3.1.3: 사용성 테스트 세션(프로토타입 사용시) — Owner: 리서처/디자이너, Estimate: 3d, Dependency: 프로토타입 준비, Acceptance: 세션 녹화·관찰 노트
- Epic 3.2: 정량 데이터 수집
  - Task 3.2.1: 설문 배포 및 응답 수집(200~400표본 목표) — Owner: 리서처, Estimate: 7d, Dependency: 2.2.1, Acceptance: 표본 수집 완료
  - Task 3.2.2: 웹/앱 로그 데이터 수집(정해진 기간) — Owner: 데이터팀, Estimate: 기간 설정, Dependency: 2.1.2, Acceptance: 분석용 쿼리/CSV 제공

## Phase 4: Analysis (Week 3-4)
- Epic 4.1: 정성 분석
  - Task 4.1.1: 전사 텍스트 태깅·코딩(Dovetail/수동) — Owner: 리서처, Estimate: 3d, Dependency: 3.1.2, Acceptance: 코드북 및 태그 빈도표
  - Task 4.1.2: 인사이트 추출(테마별 인용구 포함) — Owner: 리서처, Estimate: 2d, Dependency: 4.1.1, Acceptance: 핵심 인사이트 6개 도출
- Epic 4.2: 정량 분석
  - Task 4.2.1: EDA(퍼널, 세그먼트, 이상치) — Owner: 데이터애널리스트, Estimate: 3d, Dependency: 3.2.2/3.2.1, Acceptance: 노트북(EDA) 제출
  - Task 4.2.2: 가설검정 및 주요 메트릭 연관분석 — Owner: 데이터애널리스트, Estimate: 2d, Dependency: 4.2.1, Acceptance: 통계 결과 요약
  - Task 4.2.3: 텍스트 마이닝(리뷰·SNS 감성분석) — Owner: 데이터과학자, Estimate: 3d, Dependency: 데이터 확보, Acceptance: 키워드·감성 결과 차트

## Phase 5: Synthesis & Prototyping (Week 4-5)
- Epic 5.1: 인사이트 통합
  - Task 5.1.1: 페르소나·저니맵 작성 — Owner: 리서처/디자이너, Estimate: 2d, Dependency: 4.1.2/4.2.1, Acceptance: 페르소나 3종, 저니맵 산출
  - Task 5.1.2: 개선 아이디어 브레인스토밍(워크숍) — Owner: 리서처, Estimate: 0.5d, Dependency: 5.1.1, Acceptance: 아이디어 목록(우선순위화)
- Epic 5.2: 프로토타입 제작
  - Task 5.2.1: 와이어프레임 제작(Figma) — Owner: 디자이너, Estimate: 2d, Dependency: 5.1.2, Acceptance: 와이어 2안
  - Task 5.2.2: 인터랙티브 프로토타입 준비(사용성 테스트용) — Owner: 디자이너, Estimate: 1d, Dependency: 5.2.1, Acceptance: 테스트 가능한 프로토타입

## Phase 6: Validation (Week 5)
- Epic 6.1: 사용자 검증
  - Task 6.1.1: 사용성 테스트 실행(5~8 세션) — Owner: 리서처, Estimate: 3d, Dependency: 5.2.2, Acceptance: 관찰 노트·우선문제 리스트
  - Task 6.1.2: 소규모 A/B 테스트(로그 기반 비교) — Owner: 데이터팀, Estimate: 7~14d(옵션), Dependency: 배포/트래픽, Acceptance: 통계적 비교 결과(또는 실행 가능 권고)

## Phase 7: Delivery & Handoff (Week 6)
- Epic 7.1: 결과물 작성
  - Task 7.1.1: 최종 리포트(인사이트 + 권고안 우선순위) — Owner: 리서처, Estimate: 2d, Dependency: 4.1.2/4.2.2/6.1.1, Acceptance: `deliverables/final-report.pdf` 생성
  - Task 7.1.2: 발표자료(슬라이드) 준비 — Owner: 리서처/디자이너, Estimate: 1d, Dependency: 7.1.1, Acceptance: 발표 슬라이드 완성
- Epic 7.2: 실행 로드맵 및 핸드오프
  - Task 7.2.1: 실행 로드맵(우선순위·리소스·예상효과) 작성 — Owner: 리서처/PO, Estimate: 1d, Dependency: 7.1.1, Acceptance: 3개 우선권고와 예상 ROI 표
  - Task 7.2.2: 코드·분석 노트북·데이터 패키징 및 GitHub 업로드 — Owner: 데이터애널리스트/리서처, Estimate: 0.5d, Dependency: 7.1.1, Acceptance: 레포지토리 `research/` 정리

## 운영·유지 관리 (옵션)
- Epic O.1: 실험 추적 및 성과 모니터링
  - Task O.1.1: 핵심 메트릭 대시보드 구성(Streamlit/Tableau) — Owner: 데이터팀, Estimate: 3d, Dependency: 7.2.1, Acceptance: 대시보드 공유 링크

## 우선순위 가이드
- Must: 인터뷰(정성), 로그(정량) 확보 및 인사이트 도출
- Should: 프로토타입 기반 사용성 테스트 및 개선안 2안 제시
- Could: 정식 A/B(트래픽 필요) 및 장기 모니터링

## 템플릿/참고 자료
- research_plan.md (생성 권장)
- consent_template.md (녹취·데이터 동의서)
- notebooks/EDA_template.ipynb

---
작성자: 지원자 이름
참고: PRD — [docs/PRD.md](docs/PRD.md), TechStack — [docs/TechStack.md](docs/TechStack.md)
