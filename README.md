# Project Management Process

## 이 저장소 소개

- 신규 팀원 프로세스 파악 지원
- 규칙 변경 시 기준 문서
- 프로세스와 Notion 실제 운영 간 불일치 시 기준점

## 표기 규칙

| 항목 | 의미 | 예 |
|---|---|---|
| **(사실)** | 팀이 합의했거나 기록된 것. 출처 명시 | 매주 수요일 미팅 (1차 미팅 회의록 2026-08-04) |
| **미정** | 아직 결정되지 않았거나 기록이 없는 것 | 서비스화 형태 확정 (미정) |
| **제안** | 일반적으로 좋은 관행이나 아직 팀이 합의하지 않은 것 | (별도 섹션 또는 `[제안]` 태그) |

## 문서 구성

| 문서 | 내용 |
|---|---|
| [docs/01-project-record.md](docs/01-project-record.md) | 팀 구성, 프로젝트 주제, 미팅 이력, 현재 상태 (Epic·Sprint·Ticket) |
| [docs/02-notion-structure.md](docs/02-notion-structure.md) | Notion DB 실제 구조: 각 DB의 속성, 선택지, 템플릿 |
| [docs/03-workflow.md](docs/03-workflow.md) | 현재 운영 방식: Epic→Sprint→Ticket 관계, 정례 주기, 문서 분리 원칙 |
| [docs/04-proposals.md](docs/04-proposals.md) | 미합의 제안: 브랜치·커밋 컨벤션, 티켓 네이밍, 착수/완료 조건 등 |
| [docs/05-timeline.md](docs/05-timeline.md) | 타임라인: Phase 구분, 스프린트 달력, 마일스톤, Epic 목록, 기술 결정 기한, 축소 순서 |
| [docs/06-wbs.md](docs/06-wbs.md) | WBS: 구간별 작업 분해(2단계), 트랙 구조, 여유 0 구간, 미합의 제안 7건 |

## 템플릿

| 템플릿 | 용도 |
|---|---|
| [templates/sprint-planning.md](templates/sprint-planning.md) | Sprint Planning 페이지 |
| [templates/retrospective.md](templates/retrospective.md) | Sprint 회고 페이지 |
| [templates/ticket.md](templates/ticket.md) | 엔지니어링 (Ticket) 작업 |
| [templates/meeting-notes.md](templates/meeting-notes.md) | 회의록 |

## 개요

```
Epic (왜/무엇)
 └─ Sprint (이번 주기에 어디까지)
     └─ Ticket (누가 무엇을 언제까지)
```

| 항목 | 내용 |
|---|---|
| 정례 | 매주 수요일 미팅 (1차 미팅 이후 확정) |
| 첫 Sprint | Week 1, 2026-08-04–2026-08-19 (16일) |
| 계획 위치 | Sprint Planning 페이지 (사용자 지시) |

## 프로세스 변경 방식

1. 회고에서 문제 제기
2. 팀 합의 후 저장소 PR
3. 머지 후 Notion 반영

- 프로세스 목적: 업무 진행 지원
- 불일치 발견 시 변경. 변경 기록 유지

## 미결

없음
