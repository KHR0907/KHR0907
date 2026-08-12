<div align="center">

# 김형래 · Backend Developer

### 확장 가능한 백엔드와 실제로 동작하는 AI 제품을 만듭니다.

서비스 경계를 명확히 나누고, 독립적으로 배포·운영할 수 있는 시스템을 지향합니다.

[![Portfolio](https://img.shields.io/badge/Portfolio-111827?style=flat-square&logo=github&logoColor=white)](https://khr0907.github.io/portfolio/)
[![Resume](https://img.shields.io/badge/Resume-059669?style=flat-square&logo=readme&logoColor=white)](https://khr0907.github.io/portfolio/resume.html)
[![Repositories](https://img.shields.io/badge/Repositories-2563EB?style=flat-square&logo=github&logoColor=white)](https://github.com/KHR0907?tab=repositories)

</div>

## Engineering Snapshot

| | |
|---|---|
| **Primary role** | Backend Developer |
| **Core languages** | Java, Python, TypeScript, JavaScript |
| **Architecture** | Independently deployable services, real-time systems |
| **Current focus** | AI agent orchestration, semantic interfaces, self-hosted AI |
| **Delivery** | Docker, AWS, Jenkins, GitHub |

## About

Java와 Spring Boot를 주력으로, 비즈니스 요구사항을 명확한 도메인 모델과 안정적인 API로 구체화하는 백엔드 개발자입니다. 서비스 경계와 데이터 소유권, 트랜잭션 일관성, 동시성 제어를 설계 단계부터 고려하며, JPA·QueryDSL 기반 데이터 접근 계층과 관계형 데이터베이스·Redis를 활용해 변경에 강한 구조를 만듭니다.

기능 구현만으로 개발이 끝난다고 생각하지 않습니다. 자동화 테스트, 장애 격리와 복구, 보안, 관측 가능한 실행 상태, CI/CD와 롤백까지 운영 수명주기 전체를 개발 범위로 다룹니다. 설계 근거와 인터페이스 계약을 문서화하고, 작은 변경 단위와 검증 가능한 결과를 통해 팀의 협업 비용과 운영 위험을 낮추는 것을 중요하게 생각합니다.

## Selected Projects

| Project | Overview | Core stack |
|---|---|---|
| **[Don't Land](https://github.com/don-t-land/dev)** · Team | 브라우저에서 바로 즐기는 3D 종이비행기 멀티플레이 게임입니다.<br>물리 기반 비행, WebSocket 동기화, 회귀 테스트와 자동 롤백 배포를 구성했습니다. | JavaScript, Node.js, Three.js, Rapier3D, WebSocket, Jenkins |
| **[Obsidian 3D Semantic Graph](https://github.com/KHR0907/obsidian-3d-semantic-graph)** | 임베딩과 UMAP/PCA로 노트를 의미 기반 3D 공간에 배치하는 Obsidian 플러그인입니다.<br>시맨틱 검색, 자동 라벨 클러스터, 연결 추천과 캐싱을 제공합니다. | TypeScript, Three.js, UMAP, PCA, OpenAI Embeddings |
| **[Kyuing Bot](https://github.com/KHR0907/kyuing-bot)** | 여러 Discord 봇과 TTS 엔진을 하나의 OAuth 대시보드에서 운영하는 음성 서비스입니다.<br>사용자별 음성 설정, 발음 규칙, 사운드보드와 운영 지표를 제공합니다. | Python, discord.py, Quart, SQLite, Docker, Google Cloud TTS |
| **[Maestro](https://github.com/KHR0907/maestro)** | 코딩 태스크를 여러 LLM 에이전트에 배분하고 실행을 관리하는 셀프호스팅 플랫폼입니다.<br>격리 워크스페이스, 이슈 상태 관리와 실시간 모니터링을 제공합니다. | Python, FastAPI, SQLAlchemy, asyncio, SSE, LLM APIs |
| **[AF Agent](https://github.com/MC-agent/AF_agent)** · Team | 숙박과 음식 탐색을 지원하는 멀티 에이전트 백엔드입니다.<br>전문 에이전트, RAG 파이프라인, 인증·채팅·번역 API를 구성했습니다. | Python, FastAPI, LangChain, LangGraph, pgvector, Docker |
| **[TokiMon](https://github.com/tokepet/tokimon-app)** · Team | 여러 AI 서비스의 토큰 사용량에 반응해 성장하는 크로스플랫폼 데스크탑 펫입니다.<br>멀티 프로바이더 사용량을 로컬에서 수집하고 시각적인 성장 경험으로 변환합니다. | Tauri 2, Rust, React, TypeScript, Python, SQLite |
| **[MCP Deploy Hook](https://github.com/KHR0907/mcp-deploy-hook)** | AI 에이전트가 MCP를 통해 Git 기반 배포 파이프라인을 실행하는 headless 서버입니다.<br>순차 실행, 프로젝트별 잠금, 단계별 timeout과 SQLite 실행 로그를 제공합니다. | Python, MCP, SQLite, pytest |
| **[Efficient LLM Routing Challenge](https://github.com/prompt-way/ossp-2026-llm-router-challenge)** · Team Challenge · In progress | “쉬운 문제는 싸게, 어려운 문제만 비싸게”를 목표로 개발 중인 오프라인 AI 라우터입니다.<br>프롬프트 난이도와 budget tier만으로 품질·비용 효율이 높은 후보 모델 하나를 선택합니다. | Python, Prompt-only Routing, Budget Policy, Feature Engineering, Docker |

## Engineering Focus

```text
Service boundaries  → 책임과 데이터 소유권이 분명한 구조
Real-time systems   → 예측·보간·검증을 통한 일관된 사용자 경험
Observable work     → 비동기 작업의 진행 상태와 실패를 외부에 공개
Practical AI        → 모델 호출을 제어 가능한 제품 흐름으로 연결
Cost-aware routing  → 제한된 예산에서 프롬프트별 품질·비용 최적화
Repeatable delivery → 테스트와 CI/CD를 통한 검증·배포·복구 자동화
```

## Toolbox

| Backend | Data | Platform | AI & Interface |
|---|---|---|---|
| Java, Spring Boot | MySQL, Oracle | Docker, AWS | OpenAI, Claude |
| JPA, QueryDSL | Redis, SQLite | Jenkins, GitHub | LangChain, LangGraph |
| Python, FastAPI, Node.js | SQLAlchemy, pgvector | CI/CD, MCP | Embeddings, Budget-aware Routing, Three.js |

## What I Optimize For

- 변경의 영향 범위를 설명할 수 있는 명확한 시스템 경계
- 실패 지점을 확인하고 복구할 수 있는 실행 구조
- 테스트를 통과한 변경을 반복 가능하게 전달하는 배포 과정
- 복잡한 AI와 실시간 동작을 사용자가 이해하고 제어할 수 있는 인터페이스

---

<div align="center">

더 자세한 프로젝트와 경험은 **[Portfolio](https://khr0907.github.io/portfolio/)**에서 확인할 수 있습니다.

</div>
