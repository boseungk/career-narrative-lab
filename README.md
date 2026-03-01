# Career Narrative Lab

자기소개서(자소서) 작성과 커리어 스토리 정리를 위한 스킬 저장소입니다.  
문항 분석부터 초안 작성, 리뷰, 에피소드 발굴까지 하나의 워크플로우로 다룹니다.

## What This Repo Solves

- 문항 의도 해석이 어려울 때: 질문 유형별 전략 제공
- 내용은 있는데 정리가 안 될 때: STAR 기반 구조화 지원
- 초안 품질을 끌어올리고 싶을 때: 체크리스트 기반 리뷰 제공
- 경험 정리가 막막할 때: 프로젝트/경험에서 자소서용 에피소드 추출

## Included Skills

| Skill | 목적 | 주요 산출물 |
| --- | --- | --- |
| `cover-letter-general` | 자소서 초안 작성/개선 | 문항별 답변 초안, 표현 다듬기 |
| `cover-letter-review` | 기존 초안 리뷰 | 강점/리스크 분석, 수정 제안 |
| `episode-mining` | 경험 기반 소재 발굴 | 에피소드 후보 목록, STAR 메모 |

## Directory Layout

동일한 스킬셋을 여러 에이전트 런타임에서 쓸 수 있도록 동일 구조를 복제해 둔 형태입니다.

```text
career-narrative-lab/
├── .agent/skills/
├── .agents/skills/
├── .claude/skills/
└── .gemini/skills/
```

각 스킬 폴더는 다음과 같이 구성됩니다.

```text
<skill-name>/
├── SKILL.md               # 진입 지침
├── checklist.md           # 점검 항목 (있는 경우)
├── *-guide.md             # 작성/분석 가이드
└── *-template.md          # 결과 템플릿
```

## Quick Start

```bash
git clone https://github.com/boseungk/career-narrative-lab.git
cd career-narrative-lab
```

Codex 기준으로는 `.agent/skills/*/SKILL.md`를 자동 참조해 작업합니다.

## Recommended Workflow

1. `episode-mining`으로 경험 소재를 수집/정리
2. `cover-letter-general`로 문항별 초안 작성
3. `cover-letter-review`로 리스크 점검 및 문장 개선

## Example Requests

- "내 프로젝트 경험에서 책임감이 드러나는 에피소드 3개 뽑아줘"
- "은행 IT 직무 1번 문항 초안 작성해줘"
- "이 자소서 문항별로 논리/가독성/구체성 관점에서 리뷰해줘"

## Maintenance Notes

- 스킬 내용 수정 시 `.agent` 기준으로 먼저 반영
- 필요하면 `.agents`, `.claude`, `.gemini`에도 동일하게 동기화
- 새 스킬 추가 시 `SKILL.md` + 참고 문서(체크리스트/템플릿)를 함께 추가

## Target Outcome

실제 경험 기반의 설득력 있는 커리어 내러티브를 만들고,  
문항 의도에 맞는 자소서를 빠르게 반복 개선하는 것을 목표로 합니다.
