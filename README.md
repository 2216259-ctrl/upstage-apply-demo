# 올리브영 옴니채널 유저 경험(CX) 분석 및 이탈 방지 전략

> **Portfolio Project**: 데이터 기반 UX 리서치 및 Action Plan 수립

## 📋 프로젝트 개요

앱(Online)과 매장(Offline)을 교차 이용하는 옴니채널 유저의 이탈 원인을 규명하고, 데이터 기반의 구체적인 **Action Plan**을 수립하여 구매 전환율을 제고하는 프로젝트입니다.

- **Role:** Research Specialist (Lead Researcher)
- **Duration:** 2025.01 - 2025.02 (2 Weeks)
- **Tools:** Popow.ai (AI Survey & Analytics), Internal Data Analysis

## 🎯 핵심 문제

올리브영 앱의 MAU는 지속 성장 중이나, **2030 Light User**의 앱 탐색 → 오프라인 방문/구매 전환율이 정체되는 현상 발견.

### 가설
1. **정보의 비대칭**: 앱 재고/프로모션 정보 ≠ 매장 실제 정보
2. **경험의 부재**: 매장만의 차별화된 경험 인지 부족

## 🔍 주요 인사이트

- **35%의 유저**: "앱엔 있는데 매장엔 없어요" 경험 → 결정적 이탈 요인
- **Hidden Need**: "눈치 보지 않고 혼자 테스트하고 싶다" (20대 초반)

## 💡 제안 솔루션

### 1. Seamless Information Experience
**실시간 매장 재고 신호등 (Traffic Light)**
- `여유` 🟢 / `품절임박` 🟡 / `입고예정` ⚪
- 예상 효과: 헛걸음 경험률 **30% 감소**

### 2. Untact Curation Zone
**'눈치 보지 마세요' 키트/존**
- 직원 응대 없는 자유 테스트 구역
- AI 키오스크 퍼스널 컬러 진단
- 예상 효과: 20대 체류시간 **15% 증대**

## 📊 기대 효과

- **Business Impact**: O2O 교차 구매 유저 비중 **5%p 확대**
- **Experience Impact**: NPS(순추천지수) **10점 상승**

## 🎤 프레젠테이션

**온라인 프레젠테이션 보기**: [GitHub Pages에서 보기](https://2216259-ctrl.github.io/upstage-apply-demo/)

> Marp을 사용하여 제작된 프레젠테이션이 GitHub Actions를 통해 자동으로 배포됩니다.

## 📁 프로젝트 구조

```
upstage-apply-demo/
├── docs/
│   ├── Ideation.md          # 아이디어 발상 및 브레인스토밍
│   ├── PRD.md               # Product Requirements Document
│   └── presentation.md      # Marp 프레젠테이션 소스
├── .github/
│   └── workflows/
│       └── deploy-presentation.yml  # 자동 배포 워크플로우
└── README.md
```

## 📖 문서

- **[Ideation](./docs/Ideation.md)**: 프로젝트 아이디어 발상 과정
- **[PRD](./docs/PRD.md)**: 상세한 프로젝트 요구사항 및 분석 방법론
- **[Presentation](./docs/presentation.md)**: Marp 프레젠테이션 소스 파일

## 🛠️ 기술 스택

- **Presentation**: Marp (Markdown Presentation Ecosystem)
- **CI/CD**: GitHub Actions
- **Hosting**: GitHub Pages
- **Analysis Tools**: Popow.ai (AI Survey & Analytics)

## 🚀 로컬에서 프레젠테이션 보기

```bash
# Marp CLI 설치
npm install -g @marp-team/marp-cli

# HTML로 변환
marp docs/presentation.md -o presentation.html --html

# 브라우저로 presentation.html 열기
```

## 📝 License

This is a portfolio project for demonstration purposes.

---

**Contact**: [GitHub Profile](https://github.com/2216259-ctrl)