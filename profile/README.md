# DevPath AI

> **"내 수준에 맞는 다음 단계를 AI가 안내하는 최초의 개발자 교육"**

한국 백엔드 개발자 커리어를 타겟으로, **AI 개인화 학습 경로** · **실습 기반 AI 코드 리뷰** · **학습 맥락 연결 커뮤니티**를 결합한 학습 플랫폼입니다.

가입 후 두 번의 Aha Moment를 목표로 합니다:
1. **1st Aha** — GitHub 활동 + 진단 결과 기반 개인화 학습 경로
2. **2nd Aha** — 콘텐츠 학습 + Sandbox 실습 후 학습 맥락 기반 AI 코드 리뷰

> **현재 구현 상태(2026-06-21)**: MD1 1st Aha와 MD2 Slice #4 콘텐츠 뷰어/진척 흐름이 `main`까지 릴리스되었습니다. 구현 완료 범위는 OAuth/JWT 사용자 흐름, 회원/비회원 진단, Ollama 기반 학습경로 생성·영속화·SSE, pgvector 콘텐츠 매칭 스키마, 문항 500개·콘텐츠 150편 seed, `/contents/**` API 라우팅, Flutter Web 콘텐츠 뷰어·진척 POST입니다. Sandbox runner, AI 코드 리뷰 worker, community API, 운영 Claude/FinOps, 모바일 실API 전환은 다음 슬라이스 범위입니다.

## 📦 레포지토리

폴리레포(distributed modular monolith) — 독립 배포 서비스 + 중앙 라이브러리·스키마. 최신 진행 상태는 [workflow-dashboard](https://devpathai.github.io/workflow-dashboard/)와 [documents](https://github.com/DevPathAi/documents)를 기준으로 확인합니다.

### 서비스 · 인프라
| 레포 | 용도 |
|------|------|
| [devpath-shared](https://github.com/DevPathAi/devpath-shared) | 공유 이벤트 스키마, 공통 라이브러리, 중앙 Flyway 스키마(SSOT), 로컬 compose(PostgreSQL/pgvector/Redis/Kafka/Elasticsearch) |
| [devpath-gateway](https://github.com/DevPathAi/devpath-gateway) | Spring Cloud Gateway 엣지 라우팅, OAuth2/JWT 검증, learning/platform/content API 프록시 |
| [devpath-platform-svc](https://github.com/DevPathAi/devpath-platform-svc) | user/auth, OAuth2 연동, refresh/logout, notification, onboarding 상태 전이 |
| [devpath-learning-svc](https://github.com/DevPathAi/devpath-learning-svc) | onboarding 진단, 학습경로 엔진, 콘텐츠 seed·viewer API, 콘텐츠 진척, mentor 목표 도메인 |
| [devpath-ai-svc](https://github.com/DevPathAi/devpath-ai-svc) | dev Ollama AI Gateway(`/ai/embed`, `/ai/path/generate`)와 운영 provider 교체 지점 |
| [devpath-community-svc](https://github.com/DevPathAi/devpath-community-svc) | 게시판, 평판, 배지, 모더레이션, 학습 맥락 연결 목표 도메인(현재 스켈레톤) |
| [devpath-sandbox-svc](https://github.com/DevPathAi/devpath-sandbox-svc) | Docker + gVisor 격리 실행, 제출 실행 로그, Sandbox runner 목표 도메인(현재 스켈레톤) |
| [devpath-frontend](https://github.com/DevPathAi/devpath-frontend) | Flutter/Dart melos 모노레포: web 실API 흐름, admin 목 화면, mobile 초기 앱, dp_core/dp_design |
| [devpath-gitops](https://github.com/DevPathAi/devpath-gitops) | Kubernetes 매니페스트, ArgoCD ApplicationSet, 서비스별 Kustomize base |
| [devpath-svc-template](https://github.com/DevPathAi/devpath-svc-template) | 백엔드 서비스 스켈레톤 템플릿 |

### 문서 · 보조
| 레포 | 용도 |
|------|------|
| [documents](https://github.com/DevPathAi/documents) | 기획·설계·운영 전체 문서, 슬라이스 설계·플랜·핸드오프 |
| [storyboard](https://github.com/DevPathAi/storyboard) | 단일 HTML 인터랙티브 화면 스토리보드 |
| [prototype](https://github.com/DevPathAi/prototype) | 공개 Flutter Web 프로토타입 쇼케이스 |
| [templates](https://github.com/DevPathAi/templates) | 공용 템플릿 모음 |
| [workflow-dashboard](https://github.com/DevPathAi/workflow-dashboard) | MD1~MD4 수직 슬라이스 진행 대시보드(GitHub Pages) |
| [workflow-guide](https://github.com/DevPathAi/workflow-guide) | documents 기반 VitePress 워크플로 가이드 사이트 |
| [.github](https://github.com/DevPathAi/.github) | 조직 프로필과 공통 GitHub 설정 |

## 최근 릴리스 스냅샷

| 날짜 | 범위 | 상태 |
|------|------|------|
| 2026-06-20 | MD1 Slice #1~#3 | 인증/진단/학습경로 1st Aha E2E 수동검증 통과, develop -> main 릴리스 |
| 2026-06-21 | MD2 Slice #4 | `user_content_progress`, 문항·콘텐츠 seed, 콘텐츠 viewer/progress API, gateway `/contents/**`, Flutter Web 콘텐츠 진척 흐름 main 릴리스 |

## 🔑 기술 스택

`Spring Boot 4` `Java 21` `Spring Cloud Gateway` `Flutter Web` `Dart` `Riverpod 3` `melos 7` `Ollama(dev)` `Claude API(target)` `pgvector` `PostgreSQL` `Redis` `Kafka` `Docker + gVisor` `Kubernetes` `ArgoCD` `Vite/VitePress`
