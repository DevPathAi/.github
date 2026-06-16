# DevPath AI

> **"내 수준에 맞는 다음 단계를 AI가 안내하는 최초의 개발자 교육"**

한국 백엔드 개발자 커리어를 타겟으로, **AI 개인화 학습 경로** · **실습 기반 AI 코드 리뷰** · **학습 맥락 연결 커뮤니티**를 결합한 학습 플랫폼입니다.

가입 후 1시간 안에 두 번의 Aha Moment를 제공합니다:
1. 🎉 **1st Aha** — GitHub 활동 + 진단 결과 기반 3개월 개인화 로드맵
2. 🎉 **2nd Aha** — Sandbox 실습 후 실무급 AI 코드 리뷰

## 📦 레포지토리

폴리레포(distributed modular monolith) — 독립 배포 서비스 + 중앙 라이브러리·스키마.

### 서비스 · 인프라
| 레포 | 용도 |
|------|------|
| [devpath-shared](https://github.com/DevPathAi/devpath-shared) | 공유 이벤트 스키마 + 공통 라이브러리 + 중앙 Flyway 스키마(SSOT) + 로컬 compose |
| [devpath-gateway](https://github.com/DevPathAi/devpath-gateway) | API Gateway (Spring Cloud Gateway, OAuth2 + JWT) |
| [devpath-platform-svc](https://github.com/DevPathAi/devpath-platform-svc) | user/auth · github 수집 · notification |
| [devpath-learning-svc](https://github.com/DevPathAi/devpath-learning-svc) | onboarding · 학습 경로 엔진 · content · mentor |
| [devpath-community-svc](https://github.com/DevPathAi/devpath-community-svc) | 게시판 · 평판 · 배지 · 모더레이션 · 학습 맥락 |
| [devpath-ai-svc](https://github.com/DevPathAi/devpath-ai-svc) | AI Gateway(Claude 오케스트레이터) · review worker · FinOps |
| [devpath-sandbox-svc](https://github.com/DevPathAi/devpath-sandbox-svc) | Docker + gVisor 격리 실행 |
| [devpath-frontend](https://github.com/DevPathAi/devpath-frontend) | web·admin·mobile 모두 Flutter (Dart, melos 모노레포) |
| [devpath-gitops](https://github.com/DevPathAi/devpath-gitops) | Kubernetes 매니페스트 + ArgoCD + 마이그레이션 Job |
| [devpath-svc-template](https://github.com/DevPathAi/devpath-svc-template) | 백엔드 서비스 스켈레톤 템플릿 |

### 문서 · 보조
| 레포 | 용도 |
|------|------|
| [documents](https://github.com/DevPathAi/documents) | 기획·설계·운영 전체 문서 (계획서, ERD, 아키텍처, API 명세 등) |
| [storyboard](https://github.com/DevPathAi/storyboard) | 인터랙티브 HTML 화면 스토리보드 |
| [prototype](https://github.com/DevPathAi/prototype) | 프로토타입 구현 |
| [templates](https://github.com/DevPathAi/templates) | 공용 템플릿 모음 |
| [workflow-dashboard](https://github.com/DevPathAi/workflow-dashboard) | 팀 워크플로 진행 대시보드 |
| [workflow-guide](https://github.com/DevPathAi/workflow-guide) | 워크플로 가이드 정적 사이트 |

## 🔑 기술 스택

`Spring Boot 4` `Java 21` `Flutter 3` `Dart` `Claude API` `pgvector` `Docker + gVisor` `Kafka` `PostgreSQL` `Redis`
