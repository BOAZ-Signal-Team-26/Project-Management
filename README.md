# Project-Management

판매 중인 금융상품 설명서를 전수 채점해 부·절마다 설명 난독성 점수를 산출하는 파이프라인 프로젝트의 계획 저장소.
상세 전제: [signal-pipeline 「프로젝트 전제」](https://github.com/BOAZ-Signal-Team-26/signal-pipeline/blob/main/docs/README.md)

## 현재 개요 (Week 4 기준)

| 항목 | 내용 |
|---|---|
| 현재 스프린트 | Week 4, 9월 17일~9월 30일 (2주) |
| 이번 스프린트 마감 | 2단계 데이터 파이프라인 Flow 설계(9월 30일), 데이터 처리 요구 명세 승인(9월 30일) |
| 1단계 데이터 테이블·ERD 설계 | ERD v2.1 검토안(9월 23일, 표 20개·관계 47개). 승인 미완료 → [data-model.md](https://github.com/BOAZ-Signal-Team-26/signal-pipeline/blob/main/docs/data-model.md) |
| 다음 스프린트 | Week 5, 10월 1일~10월 14일. 3단계 입출력 Schema 설계, 파이프라인 가동 점검 |
| 스프린트 주기 | 2주. 9월 3일부터 적용 |
| 정례 | 매주 수요일 20:30 미팅. 스프린트 경계도 이 미팅 |
| 최종 마감 | 12월 23일 완료 판정. 예비 기간 2027년 1월 6일까지 |

## 팀 구성

| 역할(이름) |
|---|
| PM(대현) |
| 분석·리서치(민석) |
| 데이터 사이언스(다빈) |
| 데이터 엔지니어링·인프라(주영) |

## 저장소 구성

9월 22일 결정. Github 저장소 3개.

| 저장소 | 담는 것 |
|---|---|
| [`signal-pipeline`](https://github.com/BOAZ-Signal-Team-26/signal-pipeline) | 코드 + 설계 (ERD, 소스 명세, 실측 기록) |
| [`signal-infra`](https://github.com/BOAZ-Signal-Team-26/signal-infra) | 클라우드 구축 |
| `Project-Management` (이 저장소) | 계획 (일정, WBS, 스프린트, 운영 규칙) |

## 정본 위치 (Notion과 이 저장소)

같은 사실은 한 곳에만 기록. 다른 쪽은 링크만 둠.

| 사실 | 정본 | 다른 쪽은 |
|---|---|---|
| 회의록, 결정 발언 | Notion 회의록 DB | 저장소에 복사하지 않음. 결정 날짜만 「(사실, 팀장 확정 날짜)」로 인용 |
| 티켓 진행 상태, 결과, 담당 변경 | Notion 티켓 DB | 저장소에 「현재 상태」 표를 두지 않음 |
| 스프린트 문서(6절) | Notion Sprint 관리 DB | 저장소는 틀(`templates/sprint-page.md`)만 |
| Epic 진행 상태 | Notion EPIC 로드맵 DB | WBS에는 완료 조건만 |
| 용어 정의 | Notion 「프로젝트 용어 사전」 | 링크만 |
| 일정 기준선: Phase, 스프린트 달력, 마일스톤, 축소 순서 | 이 저장소 `05-timeline.md` | Notion은 링크 |
| 작업 분해: Epic → 하위 작업, 선후 관계, 스프린트 배치 | 이 저장소 `06-wbs.md`, `07-sprint-plan.md` | Notion 티켓은 여기서 생성 |
| 팀 운영 규칙: 주기, PR·브랜치 규칙, 문서 틀 | 이 저장소 `03-workflow.md`, `04-proposals.md`, `templates/` | 변경은 PR로 (아래 「프로세스 변경 방식」) |
| 설계: ERD, 소스 명세, 실측 수치 | `signal-pipeline` `docs/` | 이 저장소는 링크만. 숫자를 복사하지 않음 |
| 문서 작성 지침 | 이 저장소 `agents/tpm-doc-ko.md` | 로컬 `.claude/agents/`는 사본 |

## 읽는 순서

| 순서 | 문서 | 알게 되는 것 |
|---|---|---|
| 1 | README (이 문서) | 프로젝트 정의, 저장소 구성, 정본 위치 |
| 2 | [signal-pipeline docs/README](https://github.com/BOAZ-Signal-Team-26/signal-pipeline/blob/main/docs/README.md) | 프로젝트 전제, 설계 단계와 상태 |
| 3 | [05-timeline.md](docs/05-timeline.md) | Phase, 스프린트 달력, 마일스톤, 축소 순서 |
| 4 | [06-wbs.md](docs/06-wbs.md) | Epic 14건과 하위 작업, 담당 예정, 선후 관계 |
| 5 | [07-sprint-plan.md](docs/07-sprint-plan.md) | 스프린트별 생성 티켓, 스프린트 문서 틀 |
| 6 | [04-proposals.md](docs/04-proposals.md), [templates/](templates/) | PR 규칙(확정분), 미합의 제안, 문서 틀 |
| 참고 | 01·02·03·08, 09-plan-review | 지난 시점 기록 |

## 문서 목록

| 문서 | 내용 | 상태 |
|---|---|---|
| [docs/05-timeline.md](docs/05-timeline.md) | Phase 구분, 스프린트 달력, 마일스톤, Epic 목록, 기술 결정 기한, 축소 순서 | 현행 |
| [docs/06-wbs.md](docs/06-wbs.md) | WBS: 범위 확정, 제목 대응표, Epic 완료 조건, 구간별 작업 분해, 미합의 제안 | 현행 |
| [docs/07-sprint-plan.md](docs/07-sprint-plan.md) | 스프린트별 티켓·작업 계획, 스프린트 문서 틀 | 현행 |
| [docs/04-proposals.md](docs/04-proposals.md) | PR 규칙(9월 29일 확정), 그 밖의 미합의 제안 | 현행 (1-3절 외 제안) |
| [templates/](templates/) | 스프린트 문서, Sprint Planning, 회고, 티켓, 회의록 틀 | 현행 |
| [docs/01-project-record.md](docs/01-project-record.md) | 초기 팀 구성, 초기 주제(이상탐지), 미팅 이력 | 기록 (8월 12일) |
| [docs/02-notion-structure.md](docs/02-notion-structure.md) | Notion DB 속성·선택지 스냅숏 | 기록 (8월 12일) |
| [docs/03-workflow.md](docs/03-workflow.md) | Epic→Sprint→Ticket 관계, 초기 운영 방식 | 기록 (8월 12일) |
| [docs/08-m1-decisions.md](docs/08-m1-decisions.md) | 데이터 테이블·ERD 설계 확정 점검 전 선택지(검증 노선, CDI 산출 단위) | 기록 (종결. 채택 결과는 2-6절) |
| [docs/09-plan-review/](docs/09-plan-review/00-summary.md) | 외부 자문 계획 검토(9월 8일): 종합, 관점별 보고서 4건, 추가 검토 3건, 입력 요약 | 기록 (외부 원문, 수정 안 함) |

## 템플릿

| 템플릿 | 용도 |
|---|---|
| [templates/sprint-page.md](templates/sprint-page.md) | Notion 스프린트 문서 (6절 고정) |
| [templates/sprint-planning.md](templates/sprint-planning.md) | Sprint Planning 페이지 |
| [templates/retrospective.md](templates/retrospective.md) | Sprint 회고 페이지 |
| [templates/ticket.md](templates/ticket.md) | 엔지니어링 (Ticket) 작업 |
| [templates/meeting-notes.md](templates/meeting-notes.md) | 회의록 |

## 표기 규칙

| 항목 | 의미 | 예 |
|---|---|---|
| **(사실)** | 팀이 합의했거나 기록된 것. 출처 명시 | 매주 수요일 미팅 (1차 미팅 회의록 8월 4일) |
| **미정** | 아직 결정되지 않았거나 기록이 없는 것 | 서비스화 형태 확정 (미정) |
| **제안** | 일반적으로 좋은 관행이나 아직 팀이 합의하지 않은 것 | (별도 섹션 또는 `[제안]` 태그) |

## 프로세스 변경 방식

1. 회고에서 문제 제기
2. 팀 합의 후 저장소 PR
3. 머지 후 Notion 반영

- 불일치 발견 시 변경. 변경 기록 유지

## 미결

- 없음
