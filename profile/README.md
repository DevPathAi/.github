# 레바(Leva)

> 사수 없는 0~3년차 개발자의 첫 AI 사수

레바는 학습 이력과 직전 오류를 질문에 자동으로 붙여, 막힐 때마다 AI에게 상황을 처음부터 다시 설명하지 않아도 되게 합니다. 핵심은 LCS(Learning Context Snapshot, 학습 맥락 자동 첨부)입니다.

- 서비스: https://leva.ai.kr
- 앱: https://app.leva.ai.kr
- 개발 기록: https://leva.ai.kr/notes/
- 문의: https://leva.ai.kr/contact

## 현재 상태

무료 베타 운영 중입니다.

- 가입 없이 15문항 적응형 진단과 결과 확인
- 진단 결과 기반 12주 학습 경로 (저장 시 로그인)
- 학습 맥락을 붙여 질문하는 AI 멘토 (순차 초대)
- 지금은 브라우저만 지원

## 저장소

### 서비스 · 인프라

| 저장소 | 용도 |
|---|---|
| [devpath-gateway](https://github.com/DevPathAi/devpath-gateway) | Spring Cloud Gateway 엣지 — 라우팅, OAuth2/JWT 검증 |
| [devpath-platform-svc](https://github.com/DevPathAi/devpath-platform-svc) | 사용자 · 인증, GitHub 수집 |
| [devpath-learning-svc](https://github.com/DevPathAi/devpath-learning-svc) | 진단, 학습 경로 엔진, 콘텐츠, AI 멘토 |
| [devpath-ai-svc](https://github.com/DevPathAi/devpath-ai-svc) | AI Gateway — Claude API 1차, Ollama 폴백 |
| [devpath-lcs-svc](https://github.com/DevPathAi/devpath-lcs-svc) | LCS — 질문에 학습 맥락 스냅샷 자동 첨부 |
| [devpath-community-svc](https://github.com/DevPathAi/devpath-community-svc) | Q&A 게시판, 평판, 배지, 검색 |
| [devpath-notification-svc](https://github.com/DevPathAi/devpath-notification-svc) | 디바이스 토큰, 인앱 알림, 리텐션 배치 |
| [devpath-sandbox-svc](https://github.com/DevPathAi/devpath-sandbox-svc) | Docker + gVisor 격리 실행 |
| [devpath-shared](https://github.com/DevPathAi/devpath-shared) | 공유 이벤트 스키마, 공통 라이브러리, 중앙 Flyway 스키마 |
| [devpath-frontend](https://github.com/DevPathAi/devpath-frontend) | Flutter 웹 · 관리자 모노레포 |
| [devpath-mobile](https://github.com/DevPathAi/devpath-mobile) | Flutter 네이티브 모바일 앱 |
| [devpath-home-page](https://github.com/DevPathAi/devpath-home-page) | 홈페이지(leva.ai.kr) |
| [devpath-gitops](https://github.com/DevPathAi/devpath-gitops) | Kubernetes 매니페스트, ArgoCD |
| [devpath-svc-template](https://github.com/DevPathAi/devpath-svc-template) | 백엔드 서비스 스켈레톤 템플릿 |

### 문서 · 보조

| 저장소 | 용도 |
|---|---|
| [documents](https://github.com/DevPathAi/documents) | 기획 · 설계 · 운영 문서 |
| [workflow-guide](https://github.com/DevPathAi/workflow-guide) | documents 기반 워크플로 가이드 사이트 |
| [workflow-dashboard](https://github.com/DevPathAi/workflow-dashboard) | 워크플로 진행 대시보드 |
| [storyboard](https://github.com/DevPathAi/storyboard) | 화면 설계 스토리보드 |
| [prototype](https://github.com/DevPathAi/prototype) | Flutter 프로토타입 쇼케이스 |
| [templates](https://github.com/DevPathAi/templates) | 공용 템플릿 모음 |

## 기술 스택

`Spring Boot 4` `Java 21` `Spring Cloud Gateway` `Flutter Web` `PostgreSQL` `pgvector` `Redis` `Kafka` `Elasticsearch` `Kubernetes` `ArgoCD` `Claude API` `Ollama`

## 저장소 이름에 대해

저장소와 조직 이름의 `devpath`는 초기 프로젝트 코드명입니다. 서비스의 공식 이름은 레바(Leva)입니다.
