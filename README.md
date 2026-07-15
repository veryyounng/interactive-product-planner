# Interactive Product Planner

아이디어를 한 번에 하나의 질문으로 구체화하는 Claude Code·Codex용 오픈소스 기획 스킬입니다.

막연한 아이디어를 바로 결론 내리지 않고 다음 과정을 따라 구조화합니다.

- 사용자 답변을 한 단계씩 수집하고 정리
- 관찰 사실, 추정, 가설, 확인 필요 사항 구분
- 현재 흐름 진단 → 타깃 후보 3개 → 채널 후보 3개 → 최종 전략 정리
- 중요한 결정마다 사용자 승인 요청
- 최신 정보가 필요한 주장에는 출처와 확인일 기록

## 사용 대상

- 앱·서비스·캠페인 아이디어를 구체화하려는 사람
- 기획 경험이 많지 않아 질문을 따라가며 정리하고 싶은 사람
- AI가 근거 없이 결론을 확정하지 않도록 통제하고 싶은 사람
- 챌린지, 제안서, 포트폴리오용 기획안을 만들고 싶은 사람

## 폴더 구조

```text
skills/
└── interactive-product-planner/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── output-template.md
```

## Codex 설치

저장소를 내려받은 뒤 `skills/interactive-product-planner` 폴더 전체를 사용자 스킬 디렉터리에 복사합니다.

### Windows CMD

```cmd
mkdir "%USERPROFILE%\.codex\skills"
xcopy "skills\interactive-product-planner" "%USERPROFILE%\.codex\skills\interactive-product-planner\" /E /I /Y
```

설치 결과:

```text
C:\Users\사용자명\.codex\skills\interactive-product-planner\SKILL.md
```

Codex를 다시 시작한 뒤 다음과 같이 호출합니다.

```text
@interactive-product-planner 새로운 앱 아이디어를 기획해줘.
```

## Claude Code 설치

프로젝트 단위로 사용할 경우 아래처럼 복사합니다.

```cmd
mkdir ".claude\skills"
xcopy "skills\interactive-product-planner" ".claude\skills\interactive-product-planner\" /E /I /Y
```

Claude Code를 다시 시작한 뒤 자연어로 기획을 요청하거나 스킬 이름을 명시합니다.

## 사용 예시

```text
회의가 끝나면 할 일을 자동으로 정리해주는 서비스를 기획하고 싶어.
한 번에 하나씩 질문하고 내 답변을 정리하면서 진행해줘.
```

스킬은 먼저 아이템명, 가치, 목표, 관찰 자료, 운영 조건과 미확인 사항을 확인합니다. 이후 사용자의 승인 없이 다음 의사결정 단계로 넘어가지 않습니다.

## 핵심 원칙

1. 한 번에 중요한 질문 하나만 합니다.
2. 한 사람의 경험을 전체 시장의 사실로 확대하지 않습니다.
3. 후보와 확정 결정을 구분합니다.
4. 플랫폼 기능, API, 법률, 가격 등 변할 수 있는 정보는 검증합니다.
5. 최종 결정은 AI가 아니라 사용자가 합니다.

## 라이선스

MIT License에 따라 자유롭게 사용, 수정, 배포할 수 있습니다.

