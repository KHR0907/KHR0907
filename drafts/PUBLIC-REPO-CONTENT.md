# 공개 저장소 기반 프로필 콘텐츠 조사

> 조사일: 2026-08-12 · 도구: GitHub CLI (`gh`) · 계정: `KHR0907`

이 문서는 GitHub 공개 저장소의 설명, README, 언어 통계, 기여자 목록을 바탕으로 프로필 README에 사용할 수 있는 내용을 정리합니다. 비공개 저장소의 내용과 추정치는 포함하지 않았습니다.

## 계정과 Organization

- GitHub 계정: [`KHR0907`](https://github.com/KHR0907) — 공개 저장소 15개
- [`PostZi`](https://github.com/PostZi) — 공개 저장소 없음
- [`MC-agent`](https://github.com/MC-agent) — 공개 저장소 3개
- [`tokepet`](https://github.com/tokepet) — 공개 저장소 1개
- [`prompt-way`](https://github.com/prompt-way) — 공개 저장소 1개
- [`don-t-land`](https://github.com/don-t-land) — 공개 저장소 3개

총 23개 공개 저장소가 확인됐습니다. 이 중 개인 프로필 저장소 1개, 포크, Organization 소속만 있고 현재 계정 기여가 확인되지 않는 저장소는 대표 프로젝트 후보에서 분리했습니다.

> 일부 개인 저장소의 기여자 표시는 `KHR0907`과 `hyungrae0907`로 나뉩니다. 저장소 소유권은 확인되지만 두 로그인 사이의 동일인 여부는 이 문서에서 단정하지 않습니다.

## 최종 프로필에 우선 추천하는 프로젝트

### 1. [Don't Land](https://github.com/don-t-land/dev) · Organization/Team project

**복사 가능한 한 줄 소개**

> Three.js와 Rapier3D로 구현한 브라우저 3D 종이비행기 멀티플레이 게임입니다. WebSocket 상태 동기화, 클라이언트 예측·원격 보간, 서버 검증, 회귀 테스트와 자동 롤백 배포까지 구성했습니다.

**README에서 확인된 증거**

- 설치 없이 브라우저에서 실행되는 3D 멀티플레이 게임
- 최대 4명의 거리 경쟁 모드와 최대 8명의 생존 모드
- Three.js 3D 월드, Rapier3D 고정 시간 간격 물리 계산
- 종이 접기 프리셋에서 공력 특성과 충돌체 계산
- WebSocket으로 방, 참가자, 위치, 순위, 경기 이벤트 동기화
- 로컬 기체 예측과 원격 기체 보간
- 연결별 메시지 속도 제한과 16KiB 크기 제한
- Node 기본 테스트 러너로 방 수명주기, 동기화, 물리, UI 정책, 보안 제한 검증
- Jenkins에서 테스트 → 불변 릴리스 디렉터리 → 원자적 심볼릭 링크 전환 → 헬스 체크 → 실패 시 롤백
- 기여자 목록상 `KHR0907` 76 contributions

**프로필용 스택**

`JavaScript` `Node.js` `Three.js` `Rapier3D` `WebSocket` `Jenkins`

### 2. [Obsidian 3D Semantic Graph](https://github.com/KHR0907/obsidian-3d-semantic-graph) · Personal project

**복사 가능한 한 줄 소개**

> 임베딩과 UMAP/PCA로 노트의 의미적 관계를 3D 공간에 배치하고, 시맨틱 검색·자동 라벨 클러스터·연결 추천을 제공하는 Obsidian 플러그인입니다.

**README에서 확인된 증거**

- OpenAI 임베딩 또는 업로드 벡터를 UMAP/PCA로 3D 투영
- 의미 검색 후 상위 결과 강조와 카메라 이동
- k-means 기반 의미 클러스터와 제목·태그 기반 자동 토픽 라벨
- 미연결 유사 노트 추천, 중복 후보, 고립 노트, MOC 생성
- 타임라인 재생, HTML 내보내기, 한/영 UI
- 콘텐츠 해시, 임베딩, 레이아웃 캐시로 불필요한 재계산 방지
- 벡터 차원·유한값·노트 경로 검증과 데이터 전송 범위 문서화
- 750개 한국어 노트로 구성된 별도 공개 검증 데이터셋
- MIT License, GitHub stars 5, `KHR0907` 87 contributions

**프로필용 스택**

`TypeScript` `Three.js` `3d-force-graph` `UMAP` `PCA` `OpenAI Embeddings`

### 3. [Kyuing Bot](https://github.com/KHR0907/kyuing-bot) · Personal project

**복사 가능한 한 줄 소개**

> 여러 Discord 봇과 TTS 엔진을 하나의 OAuth 대시보드에서 운영하는 Docker 기반 음성 서비스입니다. 사용자별 음성 설정, 발음 규칙, 사운드보드와 운영 지표를 제공합니다.

**README에서 확인된 증거**

- 하나의 supervisor가 웹 대시보드와 여러 Discord bot worker 관리
- Google Cloud TTS 기본 지원, Supertonic-3 선택 지원
- Supertonic-3의 31개 언어, 자동 감지, 표현 태그 지원
- 사용자별 엔진·음성·속도·언어·품질 설정
- 봇별 채널, 치환어, 발음 규칙, 사용량, 대시보드 지표
- Discord OAuth 관리자 로그인과 다중 봇 시작·중지·재시작
- SQLite 영속화, Docker Compose 배포, 로그 회전과 일별 사용량 스냅샷
- 토큰을 명령행 인자로 전달하지 않고 DB에서 조회하여 프로세스 목록 노출 방지
- 비루트 컨테이너 사용자와 운영 보안 지침
- 기여자 목록상 `KHR0907` 61 contributions

**프로필용 스택**

`Python` `discord.py` `Quart` `SQLite` `Docker` `Google Cloud TTS`

### 4. [Maestro](https://github.com/KHR0907/maestro) · Personal project

**복사 가능한 한 줄 소개**

> 코딩 태스크를 여러 LLM 에이전트에 우선순위로 배분하고 격리된 워크스페이스에서 실행하며, 이슈 상태와 토큰 사용량을 실시간으로 추적하는 셀프호스팅 오케스트레이션 플랫폼입니다.

**README에서 확인된 증거**

- 프로젝트·이슈·댓글과 FSM 상태 전이를 제공하는 자체 이슈 트래커
- Claude, OpenAI, Ollama 등 OpenAI 호환 API와 자동 fallback
- 파일 읽기·쓰기, 테스트, PR 생성, 이슈 갱신을 수행하는 에이전트 루프
- 이슈별 sandbox directory와 path containment validation
- 우선순위 dispatch, 지수 backoff 재시도, stall detection
- YAML front matter와 Jinja2 기반 `WORKFLOW.md` hot reload
- Kanban, 에이전트 모니터링, 토큰 사용량을 보여주는 실시간 대시보드
- tracker, LLM adapter, agent tool, orchestrator를 대상으로 README 기준 62 tests

**프로필용 스택**

`Python` `FastAPI` `SQLAlchemy` `asyncio` `SSE` `Claude/OpenAI APIs`

### 5. [TokiMon](https://github.com/tokepet/tokimon-app) · Organization/Team project

**복사 가능한 한 줄 소개**

> 여러 AI 서비스의 토큰 사용량을 로컬에서 수집하고 펫의 성장으로 시각화하는 크로스플랫폼 데스크탑 앱입니다.

**README와 공개 기획 문서에서 확인된 증거**

- Claude, OpenAI와 OpenAI 호환 서비스의 토큰 사용량 통합
- AI 사용량을 성장, TokiPoint, 펫 수집 경험으로 변환
- Tauri 2 데스크탑 셸, React/TypeScript UI, Vite 빌드
- macOS와 Windows, 오프라인 핵심 기능, 로컬 설치를 제품 제약으로 정의
- Python sidecar와 SQLite를 이용한 로컬 수집 설계
- provider adapter로 멀티 프로바이더 확장을 분리
- 기여자 목록상 `KHR0907` 5 contributions

**프로필용 스택**

`Tauri 2` `Rust` `React` `TypeScript` `Python` `SQLite`

### 6. [AF Agent](https://github.com/MC-agent/AF_agent) · Organization/Team project

**복사 가능한 한 줄 소개**

> 숙박·음식 탐색을 위해 전문 에이전트와 RAG 파이프라인을 구성하고, 인증·채팅·번역 API를 제공하는 멀티 에이전트 백엔드입니다.

**공개 저장소에서 확인된 증거**

- 저장소 설명: Accommodation Food agent
- LangChain, LangGraph, OpenAI/Anthropic 연계 의존성
- accommodation, restaurant, room search/detail/location/check, translation agent 모듈
- supervisor와 planner 구조
- pgvector 기반 인프라와 vector store/RAG service
- JWT 회원가입·로그인, 채팅, 파이프라인, 번역 API 문서
- Docker 및 Python 3.12 실행 환경
- 기여자 목록상 `KHR0907` 73 contributions

**프로필용 스택**

`Python` `FastAPI` `LangChain` `LangGraph` `pgvector` `Docker`

## 추가 프로젝트 후보

### [MCP Deploy Hook](https://github.com/KHR0907/mcp-deploy-hook)

> AI 에이전트가 MCP를 통해 Git 기반 배포 파이프라인을 실행하는 headless 서버입니다. 순차 실행, 첫 실패 중단, 프로젝트별 lock, 단계 timeout, SQLite 로그를 제공합니다.

`Python` `MCP` `SQLite` `pytest` · MIT

### [Deploy Hook](https://github.com/KHR0907/deploy-hook)

> GitHub Webhook이나 대시보드 버튼으로 프로젝트별 셸 파이프라인을 순차 실행하는 FastAPI 기반 셀프호스팅 CI/CD 도구입니다.

`Python` `FastAPI` `SQLite` `Docker` `GitHub Webhook`

### [Mouse Handwriting](https://github.com/KHR0907/obsidian-mouse-handwriting)

> 마우스로 한글·영문·일본어 글자와 문장을 따라 쓰며 필기와 포인터 제어를 연습하는 Obsidian 플러그인입니다.

`TypeScript` `Obsidian API` `Canvas` · MIT

### [Efficient LLM Routing Challenge](https://github.com/prompt-way/ossp-2026-llm-router-challenge) · Organization/Team challenge

> “쉬운 문제는 싸게, 어려운 문제만 비싸게.” 프롬프트의 난이도와 특성만으로 비용 등급별 후보 모델 하나를 선택해 제한된 예산 안에서 답변 품질을 높이는 compute-efficient LLM routing 챌린지입니다.

- `ax31-light`, `ax31`, `axk1-think` 중 하나를 프롬프트 내용으로 선택
- `Fast 1.25`, `Balanced 2.0`, `Premium 4.0` 세 예산 등급별 라우팅 정책 설계
- 최종 평가 가중치 `Fast 0.4`, `Balanced 0.3`, `Premium 0.3`으로 저예산 라우팅을 더 중요하게 평가
- 예산을 초과한 등급은 0점, 동점이면 실행 시간이 짧은 라우터가 우선
- 모델 직접 호출, 복수 답변 비교, 순차 승급, 외부 API와 네트워크 사용 금지
- 입력은 프롬프트 또는 대화 메시지와 budget tier, 출력은 단일 후보 model ID
- 과제명·데이터 출처·문항 ID 같은 프롬프트 외 메타데이터를 이용한 라우팅 금지
- 공개 Train 1,760문항과 Dev 880문항의 outcome·토큰·비용 정보를 학습과 정책 최적화에 활용
- 프롬프트 난이도·유형 분류, tier별 정책, 품질·비용 trade-off 최적화가 핵심 개발 영역
- 결과 schema, 비용 한도, 점수, 실행 시간과 자원 제한을 검증하는 평가 harness
- 네트워크 없이 `linux/arm64` Docker image로 재현 가능하게 실행
- 전체 소스와 의존성·모델 라이선스를 공개하는 오픈소스 제출

**프로필용 소개**

> 프롬프트 난이도와 budget tier를 입력받아 제한된 예산 안에서 품질이 가장 높은 후보 모델 하나를 선택하는 오프라인 LLM 라우터를 개발합니다.

**개발 후보 기술**

`Python` `Budget-aware Routing` `Lightweight Classifier` `Feature Engineering` `Policy Optimization` `Docker` `ARM64`

### [Memo Board Wallpaper](https://github.com/KHR0907/memo-board-wallpaper)

> Markdown/JSON을 실시간 반영하고 섹션 드래그, 브라우저 편집, 소프트 삭제를 제공하는 Wallpaper Engine 메모 보드입니다.

`JavaScript` `HTML` `CSS` `Wallpaper Engine` · MIT

### [Character Persona System Design](https://github.com/KHR0907/character-persona-system-design)

> 사용자별로 진화하는 가상 캐릭터를 Identity, Psychology, Memory, Relationship, World State, Time, Events로 분해한 시스템 설계 문서입니다.

문서·스키마·템플릿 중심 저장소입니다.

### [Semantic Vault](https://github.com/KHR0907/obsidian-semantic-vault)

> 25개 주제와 주제별 30개 노트, 총 750개 한국어 Markdown 문서로 구성한 임베딩 클러스터링·3D 배치 검증 데이터셋입니다.

### [Pytools](https://github.com/KHR0907/pytools)

> 유사 프레임 제거·리사이즈·색상 축소로 GIF를 최적화하고 비디오 구간을 GIF로 변환하는 Python 유틸리티 모음입니다.

### [Web Lab](https://github.com/KHR0907/web-lab)

루트 README가 없어 프로필 설명의 근거가 약합니다. 공개 트리에는 TypeScript/Vite 인터랙션 실험, swarm animation, TokiPet Next.js landing page가 확인됩니다. README를 보강한 뒤 프로필에 넣는 편이 안전합니다.

## 별도 분류한 저장소

### 개인 계정 포크

- `KHR0907/CL4R1T4S`
- `KHR0907/obsidian-releases`
- `KHR0907/not-claude-code-emulator`

직접 프로젝트로 소개하기보다 기여 내역이 있을 때만 별도 언급하는 편이 적절합니다.

### Organization 저장소 중 현재 계정 기여가 확인되지 않은 항목

- `MC-agent/AF_agent_frontend`
- `MC-agent/af_agent_frontend1`

`prompt-way/ossp-2026-llm-router-challenge`는 현재 공개 기여자 목록에서 `KHR0907` 기여가 표시되지 않는 upstream 포크이지만, 사용자 지정에 따라 진행 중인 Team Challenge로 프로필 후보에 포함합니다.

Organization 소속만으로 개인 프로젝트처럼 소개하지 않습니다.

### 프로젝트를 보조하는 저장소

- `don-t-land/docs` — 기술 설계, 운영 기준, 협업 기록
- `don-t-land/report` — 게임 소개서, AI 활용 기술 문서, 팀 역할 문서

두 저장소는 Don't Land의 증거 링크로 활용하고 별도 프로젝트 카드로 중복 노출하지 않는 편이 좋습니다.

## Template 1에 넣을 추천 조합

프로필이 보여줘야 할 범위를 고려하면 다음 8개 조합이 가장 균형이 좋습니다. 1~4번은 핵심 프로젝트, 5~8번은 역량 범위를 확장하는 프로젝트입니다.

| 순서 | Project | 구분 | 보여주는 역량 |
|---:|---|---|---|
| 1 | Don't Land | Team | 실시간 멀티플레이, 물리, 네트워크, 테스트, CI/CD |
| 2 | Obsidian 3D Semantic Graph | Personal | AI/임베딩, 알고리즘, 3D 인터페이스, 캐싱·프라이버시 |
| 3 | Kyuing Bot | Personal | Python 서비스 운영, OAuth, 멀티프로세스, Docker, 보안 |
| 4 | Maestro | Personal | 에이전트 오케스트레이션, 격리, 상태 머신, 비동기 실행 |
| 5 | AF Agent | Team | 멀티 에이전트, RAG, pgvector, 인증·채팅 API |
| 6 | TokiMon | Team | 크로스플랫폼 데스크탑, 멀티 프로바이더, 로컬 우선 설계 |
| 7 | MCP Deploy Hook | Personal | MCP 도구 설계, 배포 파이프라인, 동시성 제어, 실행 로그 |
| 8 | Efficient LLM Routing Challenge | Team | 비용 제약형 모델 라우팅, 특징 추출, 평가 harness, ARM64 컨테이너 |

플러그인·인터랙션 역량을 강조하고 싶다면 8번을 Mouse Handwriting으로, 배포 도구의 연속성을 강조하고 싶다면 Deploy Hook으로 교체할 수 있습니다.
