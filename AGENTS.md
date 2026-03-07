# AGENTS.md

이 저장소는 자기소개서 작성용 스킬 저장소다.
에이전트는 아래 규칙에 따라 스킬을 찾고 사용한다.

## Source Of Truth

- 기본 기준은 `.agent/skills/*` 이다.
- `.agents/skills/*`, `.claude/skills/*`, `.gemini/skills/*` 는 런타임별 복제본이다.
- 스킬 내용을 수정할 때는 먼저 `.agent` 에 반영하고, 필요하면 다른 런타임 디렉터리로 동기화한다.

## Available Skills

- `episode-mining`
  - 경로: `.agent/skills/episode-mining/SKILL.md`
  - 목적: 자소서용 에피소드 발굴, 프로젝트 파일 스캔, 경험 분류
- `cover-letter-general`
  - 경로: `.agent/skills/cover-letter-general/SKILL.md`
  - 목적: 자소서 초안 작성, 문항 분석, 표현 다듬기
- `cover-letter-review`
  - 경로: `.agent/skills/cover-letter-review/SKILL.md`
  - 목적: 자소서 리뷰, 논리/구체성/면접 방어 리스크 점검

## Usage Rules

- 사용자가 스킬 이름을 직접 언급하면 해당 `SKILL.md` 를 연다.
- 요청이 특정 스킬 목적과 명확히 맞으면 해당 스킬을 사용한다.
- 여러 스킬이 걸치면 최소 개수만 선택한다.
- `SKILL.md` 는 진입 지침으로 읽고, 상세 기준은 그 문서가 직접 가리키는 참조 파일만 연다.
- 품질 우선 작업에서는 `episode-mining` 으로 전체 소재를 정리한 뒤, `cover-letter-general` 과 `cover-letter-review` 는 **문항별로** 적용하는 방식을 기본 추천한다.
- 사용자가 넓게 "자소서 써줘", "자소서 리뷰해줘"라고 요청하더라도, 특별한 이유가 없으면 **문항별 초안 작성과 문항별 리뷰가 결과 품질이 더 높다**고 먼저 짧게 안내한다.
- 전체 자기소개서를 한 번에 작성하거나 리뷰하는 방식은 **빠른 초안 작성** 또는 **최종 정합성 점검**용 보조 모드로 취급한다.
- `episode-mining` 결과가 충분히 정리된 경우에는 `episode_inventory.md` 생성을 먼저 권장한다.
- `MASTER_cover_letter.md` 는 탐색 초반 기본 산출물이 아니라, 대표 에피소드가 안정되었거나 문항별 초안 작업이 일부 진행된 뒤에 만드는 조건부 문서로 안내한다.

## Sync Rules

- `.agent` 와 다른 런타임 디렉터리 간 형식은 다를 수 있다.
- `.agents` 는 `agents/openai.yaml` 을 유지한다.
- `.claude` 는 Claude 문서 기준의 평탄한 파일 배치를 우선한다.
- `.gemini` 는 기존 구조를 유지하되 내용만 동기화할 수 있다.

## Maintenance Notes

- 새 스킬을 추가할 때는 최소한 `SKILL.md` 와 필요한 참조 문서를 함께 추가한다.
- `AGENTS.md` 에는 스킬 본문 전체를 복붙하지 않는다.
- 이 파일에는 스킬 이름, 경로, 사용 규칙처럼 런타임이 빠르게 알아야 할 정보만 적는다.
