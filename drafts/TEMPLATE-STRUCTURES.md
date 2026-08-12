# README 템플릿 구조 명세

## 공통 데이터 모델

네 템플릿은 같은 콘텐츠를 서로 다른 정보 구조로 표현합니다.

```text
PROFILE
├─ name, role, value proposition
├─ architecture/system focus
└─ short introduction

LINKS
├─ portfolio
├─ resume
└─ repositories

PROJECT[]
├─ name, URL, visibility/ownership
├─ problem or architecture challenge
├─ solution/implementation
└─ stack, interface, delivery

CAPABILITY
├─ backend
├─ data
├─ platform/delivery
└─ AI/interface

PRINCIPLE[]
└─ engineering judgment expressed as outcomes
```

## 1 · Final Hybrid

```text
Centered hero
→ Engineering Snapshot
→ About
→ Selected Projects table
→ Engineering Focus mappings
→ Toolbox matrix
→ Engineering Principles
→ Portfolio CTA
```

- **주 독자:** 채용 담당자와 엔지니어 모두
- **강점:** 역할, 프로젝트 증거, 설계 철학을 균형 있게 전달
- **프로젝트 권장 수:** 핵심 4개, 최대 8개
- **현재 선택된 최종 양식:** 이 템플릿을 실제 프로필 README의 기반으로 사용

## 2 · Recruiter First

```text
Centered hero
→ About + grouped stack
→ Project detail blocks
→ Portfolio CTA
```

- **주 독자:** 채용 담당자
- **강점:** 각 프로젝트의 설명 공간이 넓고 빠르게 읽힘
- **프로젝트 권장 수:** 핵심 4개, 최대 8개. 5~8번은 설명을 짧게 유지

## 3 · Systems Engineer

```text
Name + systems tagline
→ Engineering Focus mappings
→ Systems/challenges table
→ Working Set
→ Engineering Principles
→ Text links
```

- **주 독자:** 백엔드·플랫폼 엔지니어와 기술 면접관
- **강점:** 프레임워크 나열보다 시스템 문제와 판단을 앞세움
- **프로젝트 권장 수:** 핵심 4개, 최대 8개

## 4 · Engineering Dashboard

```text
Centered link hub
→ Snapshot
→ Five-column Project Matrix
→ Capability Map
→ Default Engineering Choices
→ Closing statement
```

- **주 독자:** 여러 프로젝트를 빠르게 비교하려는 방문자
- **강점:** 프로젝트·도메인·백엔드·인터페이스·배포의 대응 관계가 명확함
- **프로젝트 권장 수:** 핵심 4개, 최대 8개

## 작성 규칙

1. `{{UPPER_SNAKE_CASE}}` 플레이스홀더를 실제 콘텐츠로 치환합니다.
2. 프로젝트는 “무엇을 만들었다”보다 “어떤 문제를 어떤 구조로 해결했다”로 씁니다.
3. Organization 프로젝트에는 `Team project` 또는 Organization 이름을 표시합니다.
4. 공개 저장소가 없는 프로젝트에는 링크를 만들지 않습니다.
5. GitHub에서 확인되지 않은 사용자 수, 성능, 운영 규모는 추가하지 않습니다.
6. 프로젝트는 최대 8개까지 사용하되, 가장 강한 4개를 표의 앞부분에 배치합니다.
