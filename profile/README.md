# DevPath AI

> **"내 수준에 맞는 다음 단계를 AI가 안내하는 최초의 개발자 교육"**

한국 백엔드 개발자 커리어를 타겟으로, **AI 개인화 학습 경로** · **실습 기반 AI 코드 리뷰** · **학습 맥락 연결 커뮤니티**를 결합한 학습 플랫폼입니다.

가입 후 1시간 안에 두 번의 Aha Moment를 제공합니다:
1. 🎉 **1st Aha** — GitHub 활동 + 진단 결과 기반 3개월 개인화 로드맵
2. 🎉 **2nd Aha** — Sandbox 실습 후 실무급 AI 코드 리뷰

## 📦 레포지토리

| 레포 | 용도 |
|------|------|
| [documents](https://github.com/DevPathAi/documents) | 기획·설계·운영 전체 문서 (계획서, ERD, 아키텍처, API 명세 등) |
| [storyboard](https://github.com/DevPathAi/storyboard) | 인터랙티브 HTML 화면 스토리보드 |
| [prototype](https://github.com/DevPathAi/prototype) | 프로토타입 구현 |
| [templates](https://github.com/DevPathAi/templates) | 공용 템플릿 모음 (서비스 템플릿 포함 예정) |

### 🗺 확장 방향

본격 개발 단계에서는 도메인별 서비스 레포로 분리해 운영할 예정입니다:

- `devpath-shared` — 공유 스키마 + 공통 라이브러리
- `devpath-gateway` — API Gateway
- `devpath-*-svc` — 도메인별 서비스 (learning / community / platform 등)
- `devpath-frontend` — 웹/모바일 클라이언트
- `devpath-gitops` — Kubernetes 매니페스트 + 배포 구성

## 🔑 기술 스택

`Spring Boot 4` `Java 21` `React 18` `Flutter 3` `Claude API` `pgvector` `Docker + gVisor` `Kafka` `MySQL` `Redis`
