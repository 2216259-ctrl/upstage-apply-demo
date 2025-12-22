# Tech Stack — 올리브영 고객 인사이트 프로젝트

## 개요
- 대상: PRD('뷰티 구매 여정 최적화') 기반 리서치·프로토타이핑 프로젝트
- 목적: 리서치 데이터 수집·분석, 프로토타입 제작 및 A/B 검증까지 포트폴리오에 포함할 실행 가능한 기술 스택 제안

## 요구사항 요약
- 정성 데이터(인터뷰 녹취, 세션 녹화) 수집 및 관리
- 정량 데이터(웹/앱 로그, 설문) 수집·분석(퍼널, 세그먼트)
- 텍스트(리뷰·SNS) 마이닝 및 감성분석
- 빠른 프로토타입 제작 및 사용성 테스트
- 결과 시각화 및 보고서 작성(공유 가능한 산출물)
- 개인정보·민감정보 보호 준수

## 주요 선택 기준
- 학습곡선: 포트폴리오 작업에서 빠르게 결과를 만들 수 있어야 함
- 범용성: 재사용 가능하고 이력서에 기재하기 적절할 것
- 비용: 오픈소스 + 무료 tier를 우선 고려
- 확장성: 추후 실제 기업 데이터와 대규모 분석에 적용 가능해야 함

## 권장 스택 요약
- 데이터 수집: `Google Analytics` / `GA4` (웹/앱 퍼널), 서버 로그(간단한 이벤트 추적)
- 설문조사: `Typeform` 또는 `Google Forms`
- 인터뷰 녹취·전사: `Otter.ai` 또는 `Descript` (전사 자동화), 로컬 음성 파일은 `ffmpeg` 보관
- 정성 분석 도구: `Dovetail` 또는 Notion + 태깅 워크플로
- 텍스트 마이닝: Python (`pandas`, `scikit-learn`, `spaCy`, `transformers`), 감성분석에 `NLTK`/`Hugging Face` 모델
- 데이터 저장/처리(개발용): `SQLite` 또는 `Postgres` (작업 규모에 따라)
- 데이터 분석/대시보드: `Python`(Jupyter/VSCode) + `pandas`, 시각화는 `Altair`/`Plotly` 또는 `Tableau Public`
- 프로토타이핑(디자인->유저테스트): `Figma` (디자인 + 프로토타이핑), 인터랙티브 프로토타입은 `Figma` 또는 `ProtoPie`
- 사용성 테스트 / 리모트 세션: `Lookback`, `UserTesting`, 혹은 Zoom + OBS(녹화)
- 실험(A/B)·검증: 단기간 포트폴리오라면 `Optimizely`/`Google Optimize`(가능 시) 또는 가설 기반 실험 설계 + 로그 비교
- 협업·문서화: `Notion` 또는 `Confluence`, 산출물 저장소로 `Google Drive`(보고서·데이터 샘플)
- 버전관리·코드: `git` + `GitHub` (포트폴리오 레포 링크 포함)

## 인프라(간단/포트폴리오용)
- 개발·분석 환경: 로컬(Anaconda/venv) 또는 GitHub Codespaces / Colab
- 데이터 파이프라인(경량): ETL 스크립트(Python) → `Postgres` / `SQLite`
- 배포(최소): 정적 리포트 호스팅은 `GitHub Pages`, 대시보드는 `Tableau Public` 또는 `Streamlit` 앱 호스팅

## 보안·프라이버시 고려사항
- 인터뷰·의료·민감정보: 녹취 전 명시적 동의서 확보, 개인식별정보(PII) 익명화/마스킹
- 데이터 저장: 민감 데이터는 암호화 저장, 권한 있는 사람만 접근
- 법규: 개인정보보호법(한국) 준수 — 필요 시 샘플 데이터로 대체

## 개발·연구 워크플로(예시)
1. 리서치 설계 및 도구 세팅(Week 1): 이벤트 스키마 정의, GA4 이벤트, 설문 템플릿
2. 데이터 수집(Week 2~3): 인터뷰 녹취·전사, 설문 수집, 로그 수집
3. 초기 정성·정량 분석(Week 3~4): Jupyter 노트북 기반 탐색, 키 인사이트 추출
4. 프로토타입 제작(Week 4~5): Figma로 와이어 → 인터랙티브 시나리오
5. 사용성 테스트 및 A/B(Week 5): 리모트 세션 또는 내부 테스트, 결과 수집
6. 리포트·대시보드(Week 6): 시각화, 최종 권고안, 실행 로드맵

## 도구 매핑 (직무 강조 포인트)
- 고객 인사이트·정성: `Dovetail`(태깅·인사이트), `Descript`(전사), 인터뷰 가설 매핑
- 정량 분석: `GA4` + `Python(pandas)` + `Postgres`(SQL 쿼리 예시 포함 가능)
- 커뮤니케이션: `Notion`(워크플로·결과 공유), `Figma`(디자인 협업)

## 추천 이유(채용공고 연계)
- Research Specialist 역할에서 기대하는 정성·정량 역량을 모두 보여줄 수 있음
- 도구들이 직관적이고 빠른 산출물 제작을 지원하여 포트폴리오 완성도를 높임
- 데이터 파이프라인과 분석 코드를 함께 제공하면 채용 담당자에게 실무 적용 능력을 효과적으로 어필 가능

## 예시 리포지토리 구조 (포트폴리오용)
- /research
  - /data_raw (샘플 CSV, 익명화된 데이터)
  - /notebooks (분석 노트북)
  - /scripts (ETL, 분석 스크립트)
- /design
  - figma-link.txt
  - prototype-images
- /deliverables
  - final-report.pdf
  - journey-map.png

## 다음 단계 제안
- 실제 샘플 데이터(익명화)를 넣어 `notebooks`에 간단한 EDA 노트북 추가
- `Streamlit` 또는 `Tableau`로 핵심 대시보드(퍼널·세그먼트) 시연

---
작성자: 지원자 이름
참고 PRD: [docs/PRD.md](docs/PRD.md)
