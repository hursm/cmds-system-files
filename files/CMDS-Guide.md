---
type: CMDS
aliases:
  - guide
author:
  - "[[구요한]]"
date created: 2025-09-15T23:39
date modified: 2026-01-24T00:12
tags: [index, NoteClass, maps, SystemPrompt, guideline, 설명서, 커맨드스페이스, v2, 태그는자유로워야지, example, operation, service]
links:
  - "[[🏛 CMDS Head Quarter|CMDS HQ]]"
---

# CMDS Guide

> **🔄 Last Updated: 2026-01-24** | Backup: `00. Inbox/03. AI Agent/cmds-system-files/CMDS-Guide_backup.md`
>
> 📌 **Version 2.1** - Properties 표준화 및 체계 개선판

## Properties
### 필수 Properties (Required)
모든 노트는 다음 6개의 필수 properties를 포함해야 합니다:
```yaml
---
type:           # 노트 유형 (아래 표준 type 참조)
aliases: []     # 별칭 (배열 형식)
author:
  - "[[구요한]]"  # 작성자 (wikilink 형식)
date created:   # 생성일 (YYYY-MM-DDTHH:mm:ss)
date modified:  # 수정일 (YYYY-MM-DDTHH:mm:ss)
tags: []        # 태그 (배열 형식)
---
```
### 표준 Properties 정의
#### 날짜 관련
- `date created` - 생성일 (YYYY-MM-DDTHH:mm:ss)
- `date modified` - 수정일 (YYYY-MM-DDTHH:mm:ss)
- `date` - 이벤트/미팅 날짜 (YYYY-MM-DD)
- `publish_date` - 발행일 (YYYY-MM-DD)
- `year` - 연도 (YYYY)
> ⚠️ **통일 규칙**: 모든 날짜는 ISO 8601 형식 (YYYY-MM-DD) 사용

#### 작성자 및 관계
- `author: [[구요한]]` - 항상 wikilink 형식 사용
- `attendees: []` - 참석자 목록 (wikilink 배열)
- `organization: [[조직명]]` - 조직 (wikilink)

#### 분류 및 상태
- `type` - 노트 유형 (아래 표준 type 목록 참조)
- `CMDS` - CMDS 카테고리 연결 (예: `[[📚 620 Generative AI]]`)
- `index` - 인덱스 참조 (예: `[[🏷 Meeting Notes]]`)
- `status` - 상태값
	- ✅ 표준값: `unread` | `reading` | `inProgress` | `completed` | `archived`

#### 평가 및 측정
- `myRate` - 평점 (1-5 scale, 숫자)
- `totalPage` - 총 페이지 수 (camelCase)
- `views` - 조회수

#### 연결 및 참조
- `aliases: []` - 별칭 (배열 형식으로 통일)
- `tags: []` - 태그 (배열 형식으로 통일)
- `links` - 관련 링크
- `source` - 출처
- `source_url` - 출처 URL
- `bookends` - 북엔드 (기존 유지)
- `CMDS` - CMDS 카테고리 참조
### 표준 Type 목록
#### 주요 노트 타입
- `note` - 일반 노트
- `terminology` - 용어 정의
- `meeting` - 회의록
- `people` - 인물 정보
- `curriculum` - 강의 커리큘럼
- `memo` - 메모
- `class` - 수업 관련
- `manuscript` - 원고/초안
- `daily-note` - 일일 노트
- `article` - 글/기사
- `sermon` - 설교
- `review` - 리뷰/연구평론
- `project` - 프로젝트
- `zettel` - 제텔카스텐 노트
#### 구조/조직 타입
- `CMDS` - 커맨드스페이스 인덱스
- `organization` - 조직/기관
- `portal` - 포털 페이지
- `documentation` - 문서화/가이드
- `index` - 색인
- `CMDS` - CMDS 인덱스 페이지
#### 콘텐츠 타입
- `books` - 도서
- `research-review` - 연구 리뷰
- `idea` - 아이디어
- `resource` - 리소스
- `product` - 제품/서비스
### Tags
- 태그는 자유롭게 #태그는자유로워야지
- Nested tags 예시:
	- `#Author/Koo`
	- `#가이드/태그작성법`
	- `#가이드/목차작성법`
## Collections
### CMDS
- [[🏛 CMDS Head Quarter]]
- [[🏛 CMDS Guide]]
### Index
#index #NoteClass #maps
- [[🏷 Guideline]]
- [[🏷 Daily Notes]]
- [[🏷 Research Notes]]
- [[🏷 Project Notes]]
- [[🏷 Lecture Notes]]
- [[🏷 Review Notes]]
- [[🏷 Draft Article]]
- [[🏷 Web Clips]]
- [[🏷 Waypoint]]
- [[🏷 Meeting Notes]]
- [[🏷 People]]
- [[🏷 Organization]]
- [[🏷 Prompts]]
- [[🏷 Syntax and Codes]]
- [[🏷 Recordings]]
### Backlinks
- 백링크는 내 인지범위가 허락하는 선까지 [[]]
- 한 번에 다 할 필요는 없음
- Gen AI 사용하여 자동 연결 시킬 수 있음
	- Smart Composer - YAML, In-line
	- [[00. Inbox/GPT에게 용어정리 시키기|GPT에게 용어정리 시키기]]
	- Claude Code
## CMDS Levels
### 계층 구조
- 🏛 - Home, Guide (최상위)
- 📖 - 1st level CMDS (100-900 시리즈)
	- Space Collection
	- 1 digit (100-900)
- 📚 - 2nd level CMDS (N01-N99)
	- Spaces
	- 2 digit (N01-N99)
- (No Icon) - 3rd level CMDS
	- 상세 주제는 3rd level CMDS로 분류
### CMDS Level Example
```
📚 840 Lectures
├── 840.01 University Courses
│   ├── 840.01-A 차의과학대학교
│   │   ├── 840.01-A1 2024-1
│   │   │   └── [[생성형 AI 기초와 활용]]
│   │   └── 840.01-A2 2024-2
│   │       └── AI 융합 연구방법론
│   └── 840.01-B 한양대학교
```
## Filename Conventions
### 접두사(Prefix)
#### Wis' Rule
- `u.` - usecase #example
- `f.` - feature #operation
- `p.` - product #service
#### Input
- 📎 - Web Clips (W@)
- 🌿 - Readwise (WW@)
- 📘 - Books, Reference `#📚Book`
#### Process
- 🏷 - Index (E@)
- 📦 - Review (EE@)
- 📐 - Variables (EEEE@)
#### Output
- 🔖 - Output from YHN's Idea (R@)
- 📜 - Output from Other's Idea (RR@)
- 📈 - Code and Syntax (RRR@)
- 🎹 - Music (RRRR@)
- 🏙 - Canvas (F@)
#### References
- 📕 - Bible (EEE@)
### 접미사(Suffix)
#### Service에 따라
- `.obsidian`
- `.python`
- `.chatgpt`
- `.claude`
- `.midjourney`
#### Purpose에 따라
- `.meeting`
- `.portal`
## Folder Structure
```
00. Inbox/                      # 임시 저장 및 처리 공간
├── 01. Daily Notes/            # 데일리 노트 (01-1. Planners, 01-2. Weekly Notes)
├── 02. Clippings/              # 웹 클리핑 (02-1. Literature Notes)
├── 03. AI Agent/               # ⭐ AI 코드 작업 전용 (PRIMARY)
├── 04. Excalidraw/             # 다이어그램
├── 05. Canvas/                 # Canvas 노트
├── 06. Automation/             # 자동화 (06-1. Make.com, 06-2. n8n Lecture, 06-3. STT)
├── 07. App Sync/               # 외부 앱 연동 (07-1. Claude, 07-2. Antigravity, 07-3. Bear Notes)
├── 08. Unlisted/               # 미분류
└── 09. Legacy/                 # 레거시 컨텐츠

10. CMDS Process/               # CMDS 프로세스 워크플로우
├── 11. Connect/                # 배우고있는것들 #capture
├── 12. Merge/                  # 내주제와연결 #Areas #organize
├── 13. Develop/                # #distill
└── 14. Share/                  # 완성된산출물 #express

20. Literature Notes/           # 문헌 노트 및 리뷰
├── 21. Lit Notes (Zotero)/     # Zotero 연동 문헌
├── 21. Web Articles/           # 웹 아티클 (빈 폴더)
├── 22. Reviews/                # 리뷰 및 분석
├── 23. Sermon/                 # 설교 노트
├── 24. Web Articles/           # 웹 아티클
├── 28. Flashcards/             # 플래시카드
└── 29. Terminologies/          # 용어 정리

30. Permanent Notes/            # 영구 노트 (Evergreen)
├── 33. Essay/                  # 에세이
├── 34. Prompt and Syntax/      # 프롬프트 및 문법
└── 39. Guideline/              # 가이드라인

40. Docs/                       # 기술 문서 (Technical Documentation)
├── 41. Official Docs/          # 공식 문서, API 가이드, 제품 매뉴얼
├── 42. AI Generated/           # AI 생성 기술 문서
├── 43. Audio Files/            # 오디오 파일
├── 43. My Docs/                # 사용자 작성 기술 문서
├── 44. Transcripts/            # 트랜스크립트
└── 45. Partner Made/           # 파트너 제작 문서

50. Assets/                     # 미디어 및 자산
├── 51. Prompt/                 # 프롬프트 자산
├── 52. Workflow/               # 워크플로우 자산
└── 59. Obsidian Web Clipper/   # 웹 클리퍼 템플릿

60. Preferences/                # 개인 선호 및 라이프스타일
├── 61. Alcohol/                # 주류 노트
├── 62. Sleep/                  # 수면 기록
└── 63. Jazz/                   # 재즈 음악

70. Collections/                # Resources 컬렉션
├── 71. People/                 # 인물 데이터베이스
├── 72. Organization/           # 조직/기관
├── 74. Meetings/               # 회의록
├── 75. Spirituality/           # 영성 콘텐츠 (성경, 설교)
├── 76. Curriculum/             # 강의 커리큘럼
├── 77. Class/                  # 수업 관리
├── 78. Bases/                  # 데이터베이스 구조
├── 78. Kanban Board/           # 칸반 보드
└── 79. Portal/                 # 포털 페이지

80. References/                 # 참고 자료 및 출처
├── 81. Attachment/             # 첨부 파일
├── 82. Web Articles/           # 웹 아티클
├── 83. References/             # 일반 참고자료
├── 84. References (Zotero)/    # Zotero 참고문헌
├── 85. References (Book)/      # 도서 참고자료
├── 86. Omnivore/               # Omnivore 아티클
├── 86. References (Book, Yes24)/ # Yes24 도서
└── 89. Omnivore/               # Omnivore 추가 폴더

90. Settings/                   # 시스템 설정 및 관리
├── 91. Templates/              # 노트 템플릿
├── 92. Templates (archived)/   # 아카이브 템플릿
├── 93. Generated Text/         # AI 생성 텍스트
├── 94. System Prompts/         # AI 시스템 프롬프트
├── 95. Fonts/                  # 폰트 파일
├── 96. Index/                  # 인덱스 파일
├── 97. File Class/             # 파일 분류
├── 98. Format/                 # 포맷 정의
└── 99. Others/                 # 기타 설정
```
## Properties Template Examples
### 기본 노트 템플릿
```yaml
---
type: note
aliases: []
author:
  - "[[구요한]]"
date created: 2025-01-09T14:30
date modified: 2025-01-09T14:30
tags: []
CMDS: 
index: 
status: 
---
```
### 회의록 템플릿
```yaml
---
type: meeting
aliases: []
author:
  - "[[구요한]]"
date created: 2025-01-09T09:00
date: 2025-01-09
attendees:
  - "[[참석자1]]"
  - "[[참석자2]]"
organization: "[[조직명]]"
CMDS: "[[📚 831 Consulting]]"
index: "[[🏷 Meeting Notes]]"
status: inProgress
tags: [meeting]
---
```
### 연구 노트 템플릿
```yaml
---
type: research-review
aliases: []
author:
  - "[[구요한]]"
date created: 2025-01-09T16:45
title: 
source: 
source_url: 
doi: 
keywords: []
CMDS: "[[📚 820 Research]]"
index: "[[🏷 Research Notes]]"
status: reading
tags: [research]
---
```
### 도서 노트 템플릿
```yaml
---
type: books
aliases: []
author:
  - "[[구요한]]"
date created: 2025-01-09T11:20
title: 
subtitle: 
isbn: 
publisher: 
publish_date: 
totalPage: 
myRate: 
status: unread
CMDS: "[[📚 240 Books]]"
index: "[[🏷 Books]]"
tags: [📚Book]
---
```
### 인물 노트 템플릿
```yaml
---
type: people
aliases: []
author:
  - "[[구요한]]"
date created: 2025-01-09T10:15
email: 
mobile: 
organization: "[[조직명]]"
group: 
CMDS: 
index: "[[🏷 People]]"
status: 
tags: [people]
---
```
## Note-taking Guidelines
### Citation Style
#### 책 인용
> [!TIP] _Knowledge Management for the Future_
> 책의 내용 원본^[Koo, Y. (2021). _Knowledge Management for the Future._ New York: Oxford University Press. p.25.]
#### 논문 인용
> [!ABSTRACT] Knowledge Management in Organizations
> 조직 내 지식 관리의 중요성^[Kim, S., & Lee, H. (2023). The impact of knowledge management. _Journal of Knowledge Management_, 27(4), 1012-1035.]
#### 명언
> [!QUOTE]
> "2주 뒤에 뵙겠습니다."
> — 구요한(Yohan Koo)
## Sync Settings
### Obsidian Sync
- `.obsidian` - macOS, Windows, Android
- `.obsidian_mobile` - iOS, iPadOS
## Version History
- **v2.1** (2025-10-23): 내용 오류 및 일관성 수정
- **v2.0** (2025-09-15): Properties 표준화 및 체계 개선
	- 날짜 형식 ISO 8601 통일
	- author 필드 wikilink 형식 통일
	- status 표준값 정의
	- myRate로 평점 통일
	- totalPage로 camelCase 통일
	- tags/aliases 배열 형식 통일
	- bookends 유지
- **v1.0** (2022-05-25): 초기 버전

## 추가 참고사항
### Portal 페이지
- [[Omni-Agency.portal]]
- [[Second Brain Experts.portal]]

### Graph View 활용
- [[Obsidian Graph View를 활용하는 법.obsidain]]
#### Filters 예시
- `-tag:Waypoint`
- `-path:"01. Daily Notes"`
- `-path:"study" -path:"reading"`
- `-file:"00. Inbox" -tag:waypoint`
- `["type":curriculum]`

### 플러그인 참고
#### Supercharged
- People
- Organization
- Curriculum

### Migration 태그
노트 출처 표시용:
- `notion`
- `applenote`
- `bear`
- `pages`
- `hwp`
- `docx`

### Citation Callout 추가 예시
#### 웹 아티클
> [!LINK] How to Take Smart Notes
> Zettelkasten 방법론에 대한 상세 가이드^[Ahrens, S. (2022, March 15). _The Complete Guide to the Zettelkasten Method._ Retrieved from https://zettelkasten.de/posts/overview/]
> - **핵심**: 영구 노트(Permanent Notes) 작성법
> - **팁**: 하나의 노트에는 하나의 아이디어만

#### INFO/EXAMPLE Callout
> [!INFO] _Deep Work_
> 몰입의 기술에 대한 칼 뉴포트의 통찰^[Newport, C. (2016). _Deep Work: Rules for Focused Success in a Distracted World._ Grand Central Publishing. pp.14-15.]

> [!EXAMPLE] _Atomic Habits_
> "You do not rise to the level of your goals. You fall to the level of your systems."^[Clear, J. (2018). _Atomic Habits._ Avery. p.27.]

---
*이 가이드는 CMDSPACE 볼트의 표준 Properties 체계를 정의합니다. 모든 새로운 노트는 이 규칙을 따라 작성되어야 합니다.*