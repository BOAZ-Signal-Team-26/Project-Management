# 현재 운영 방식

**최종 업데이트:** 2026-08-12

## 계층 구조

```
Epic (큰 목표)
 └─ Sprint (주기별 계획)
     └─ Ticket (개별 작업)
```

| 단계 | 저장소 | 예시 |
|---|---|---|
| Epic | EPIC 로드맵 DB | `프로젝트 Ideation` |
| Sprint | Sprint 관리 DB | `Week 1 주제·데이터 확정 디스커버리` |
| Ticket | 엔지니어링 (Ticket) 작업 DB | `[Study] 이상탐지 도메인 스터디` |

각 Ticket: Epic 1개 필수, Sprint 최대 1개 연결.

용어 정의: [01-project-record.md](01-project-record.md) 참조

출처: Notion DB 구조 및 현황 조회 2026-08-12

## 정례 주기

| 항목 | 내용 |
|---|---|
| 미팅 요일 | 매주 수요일 |
| 미팅 유형 | Sprint Planning (동기식 정례) |
| 첫 미팅 | 2026-08-04 (화요일) |
| 정례 확정 | 1차 미팅 이후 |

정례: 수요일 미팅 1건. 비동기 체크인·별도 정기 회의 없음.

출처: 1차 미팅 회의록 2026-08-04, 사용자 진술

## Sprint 문서 분리 원칙

### Sprint 페이지 (Sprint 관리 DB)

- 역할: Sprint 요약 정보만 저장
- 내용: Sprint 이름, 기간, 진행 상태 등 메타데이터
- 구조: 템플릿 `스프린트` (내용: 인라인 DB 2개 + "메모" 제목)
- 예시: `Week 1 주제·데이터 확정 디스커버리`

### Sprint Planning 페이지 (엔지니어링 회의 DB)

- 역할: Sprint 상세 계획 저장
- 내용: 지난 검토, 목표 설정, 작업 분해, 분담, 리스크, 의존성 등 상세 내용
- 구조: 사용자 지정 (아래 "Sprint Planning 구조" 참조)
- 예시: `Week 1 Sprint Planning (08.12)`

분리 원칙: Sprint 페이지는 기간·범위 요약, 상세 계획·의사결정은 Sprint Planning 페이지에서 진행.

출처: 사용자 지시 2026-08-12

## Sprint Planning 구조

1. Sprint 요약 정보
2. 지난 스프린트 리뷰 — 지난 Sprint의 완료 상황 정리
3. 스프린트 목표 설정 — 이번 Sprint의 1문장 목표
4. 제품 백로그 아이템(PBI) 선정 및 우선순위 결정 — 어떤 Epic의 어느 부분을 할지
5. 작업 분해(PBI) 및 Ticket 작성 — Epic을 어떤 Ticket으로 나눌지
6. Ticket 분담 및 책임 할당 — 누가 어느 Ticket을 맡을지 (FE/BE/AI/Data & Infra 표)
7. 리스크 및 장애 요소 식별 — 막힐 수 있는 요소
8. 의존성 및 외부 연계 확인 — 다른 팀/외부와의 연계
9. 스프린트 백로그 최종 확정 — 이번 Sprint 확정

성격: 템플릿 아닌 가이드. 작성자가 순서 참고해 작성.

출처: 사용자 지시 2026-08-12

## Sprint 회고 구조

1. Sprint Backlog(SBI) — 이번 Sprint의 Ticket 목록
2. Ticket 작업 List — Sprint 주간 및 이월 표
3. 임팩트 평가 (잘 됐던 것) — Keep
4. 근본 원인 분석 (잘 안 됐던 것 & 이슈 공유) — Problem
5. 해결과 복구 단계 (개인적으로 배운 것) — Lesson
6. 수정과 예방 조치 (Re-Planning) — Try

성격: 템플릿 아닌 가이드. 작성자가 순서 참고해 작성.

출처: 사용자 지시 2026-08-12

## 첫 Sprint (Week 1) 특성

| 항목 | 값 |
|---|---|
| 기간 | 2026-08-04 – 2026-08-19 (16일) |
| Sprint ID | 10 |
| 상태 | Current / 진행중 |
| 목표 | 주제·데이터 확정 |
| Ticket 수 | 2개 (이상탐지 스터디, 데이터 수집) |

Week 1 = 첫 Sprint. 지난 Sprint 리뷰 해당 없음.

출처: Notion 조회 2026-08-12, 사용자 지시

## Ticket 할당 방식

설정: 담당자 미분리, 전원 공통 과제로 지정.

| Ticket | 담당자 |
|---|---|
| `[Study] 이상탐지 도메인 스터디` | All Member (미할당) |
| `[Research] 금융권 데이터 수집` | All Member (미할당) |

설정 근거: 팀장 지시. 초기 Ideation 단계에서 전원 학습·수집 후 데이터 선정 공동 진행 목적.

향후 개별 담당자 할당 가능성 있음.

출처: Notion 조회, 사용자 지시 2026-08-12

## 정보 흐름

미정 항목:
- Ticket 코드 변경 반영 시점 (GitHub PR 연계 방식)
- Daily standup 또는 정기 progress update 방식 (동기/비동기)
- Ticket 진행 상태 업데이트 주기
- Review 미팅 형식 (산출물 기준 판정 방식)

## 도구

| 도구 | 용도 |
|---|---|
| Notion | 계획, 문서, 티켓 |
| GitHub | 코드, PR |

출처: README.md, 사용자 진술

## 미결

| # | 확인 필요 사항 |
|---|---|
| 1 | [확인 필요: Sprint 미배정 Ticket(백로그) 관리 위치 및 방식] |
| 2 | [확인 필요: 향후 Sprint 기간 설정 규칙 수립] |
| 3 | [확인 필요: 금융 실데이터 취급 절차 수립] |
