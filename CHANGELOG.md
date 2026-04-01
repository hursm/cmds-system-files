---
type: documentation
aliases:
  - System Files Changelog
  - 시스템 파일 변경 로그
author:
  - "[[{your-name}]]"
date created: 2026-04-01T11:30
date modified: 2026-04-01T11:36
tags:
  - CMDS
  - system
  - changelog
CMDS: "[[📚 501 Obsidian]]"
---

# CMDS System Files — Changelog

> 5개 시스템 파일(CLAUDE.md, AGENTS.md, CMDS.md, 🏛 CMDS Head Quarter, 🏛 CMDS Guide)의 변경 이력을 추적합니다.

---

## v3.0 — 2026-04-01 (Architecture Upgrade)

**영감**: Claude Code 소스 코드 아키텍처 분석 → 9개 패턴 적용

### 신규 파일 생성
- `.claude/rules/indentation-rules.md` — YAML 2spaces / MD tab 공통 규칙
- `.claude/rules/frontmatter-standard.md` — 필수 6프로퍼티 + 포맷 규칙
- `.claude/rules/file-creation-rules.md` — 출력 경로, 네이밍, 프로젝트 폴더 규칙
- `.claude/rules/wikilink-rules.md` — 옵시디언 위키링크 문법 + YAML 인용 규칙
- `.claude/rules/directory-structure.md` — 볼트 폴더 구조 + CMDS 카테고리

### 전체 파일 공통 변경
1. **`precedence` 추가** — 파일 간 우선순위 명시 (1=CLAUDE → 5=HQ)
2. **`memory-type` 추가** — Claude Code memdir 타입 매핑 (feedback/user/reference)
3. **`required-for` / `optional-for` 추가** — 에이전트 스코핑 (어떤 작업에 이 파일이 필수/선택인지)
4. **`token-estimate` 추가** — 토큰 예산 의식 (AI가 어떤 파일을 우선 로드할지 판단)
5. **`changelog` 추가** — 각 파일 frontmatter에 버전 이력 내장
6. **`<!-- STATIC -->` / `<!-- DYNAMIC -->` 마커** — 캐시 가능 영역 vs 갱신 필요 영역 구분
7. **`## Essential (Post-Compact)` 섹션** — 컨텍스트 압축 후 복구용 핵심 규칙 요약

### 파일별 변경

#### CLAUDE.md (v2.1 → v3.0)
- 중복 규칙을 `@.claude/rules/` 로 분리 (@include 5개)
- Critical Rules 섹션: 인라인 규칙 → @include 참조로 전환
- Pre-Flight Checklist 유지 (빠른 확인용)
- Directory Structure: @include로 교체
- File Creation Rules: @include로 교체
- Note Types 통계 업데이트 (최신 수치 반영)
- Related System Files에 precedence 번호 추가
- `[[wikilink]]`는 옵시디언 탐색용으로 유지, `@include`는 AI 로딩용으로 분리
- 토큰 약 21KB → 예상 ~14KB (rules 포함 시 동일하나 공유 가능)

#### AGENTS.md (v1.0 → v2.0)
- 중복 규칙 60% 제거 → @include 4개로 교체
- Critical Rules 전체를 @include 기반으로 전환
- Directory Structure를 @include로 교체
- 고유 섹션만 유지: Note Types, Status Values, File Prefixes, Templates
- 토큰 약 9KB → 예상 ~5KB (rules 포함 시 동일하나 공유 가능)

#### CMDS.md (v2.0 → v2.1)
- frontmatter 강화: precedence(3), memory-type(user), required-for, token-estimate
- Essential (Post-Compact) 섹션 추가 — 5개 핵심 컨텍스트
- `<!-- STATIC -->` 마커 추가 (System Documentation Overview 이전)
- `<!-- DYNAMIC -->` 마커 추가 (Vault Statistics 이전)
- changelog 필드 추가

#### 🏛 CMDS Head Quarter (→ v1.1)
- frontmatter 강화: precedence(5), memory-type(reference), required-for, token-estimate
- version, changelog 필드 추가

#### 🏛 CMDS Guide (v2.1 → v2.2)
- frontmatter 강화: precedence(4), memory-type(reference), required-for, token-estimate
- tags 정리: 불필요한 태그 제거 (태그는자유로워야지, maps, example, service)
- changelog 필드 추가

### @include vs [[wikilink]] 사용 원칙

| 용도 | 문법 | 예시 |
|------|------|------|
| **AI가 내용을 인라인 로드** | `@path` | `@.claude/rules/indentation-rules.md` |
| **옵시디언 내부 탐색/링크** | `[[name]]` | `[[🏛 CMDS Guide]]` |
| **양쪽 모두 필요** | 둘 다 사용 | `@CMDS.md → [[CMDS.md]]` |

- `@include`: AI 에이전트가 파일 내용을 실제로 읽어야 할 때 (규칙, 구조 정의)
- `[[wikilink]]`: 사용자가 옵시디언에서 클릭하여 이동할 때 (탐색, 참조)
- Related System Files 같이 양쪽 다 필요한 경우: `@파일 → [[파일]]` 형태로 병기

---

## v2.1 — 2026-03-30 (Frontmatter Standard)

### 변경 사항
- 5개 파일 모두 frontmatter에 `description`, `audience`, `scope` 추가
- AI Documents: `type: documentation` 통일
- Human Documents: `type: CMDS` 유지
- 백업/공유 폴더를 `40. Docs/47. CMDS Docs/`로 이동
- system-docs-updater 스킬에 frontmatter 표준 섹션 추가

---

## v2.0 — 2026-03-15 (Full Review)

### 변경 사항
- 5개 파일 전면 리뷰 및 통계 갱신 (5,344+ → 10,000+)
- CLAUDE.md: 백업 경로 오타 수정, GenAI Chats 추가
- CMDS.md: PhD Candidate → PhD ABD, AI Tools 갱신, 50. Assets 섹션 추가
- 🏛 CMDS Head Quarter: CMDS Process 설명 추가, Vault Folders 섹션 추가
- 🏛 CMDS Guide: 폴더 구조 현행화, 새 type 추가
- AGENTS.md: 볼트 규모 갱신
- 백업/공유 파일 동기화
- 에세이 시리즈 9편 작성
- 웹페이지 v3 배포 (system.cmdspace.work)
- ChatGPT 시스템 프롬프트 생성

---

## v1.0 — 2025-09-27 (Initial)

### 생성
- CLAUDE.md 최초 작성
- 이후 AGENTS.md, CMDS.md, Guide, HQ 순차 추가

---

## 파일 위치 참조

| 구분 | 경로 |
|------|------|
| **정본 (5개)** | 볼트 루트: `/CLAUDE.md`, `/AGENTS.md`, `/CMDS.md`, `/🏛 CMDS Head Quarter.md`, `/🏛 CMDS Guide.md` |
| **공통 규칙 (5개)** | `.claude/rules/indentation-rules.md`, `frontmatter-standard.md`, `file-creation-rules.md`, `wikilink-rules.md`, `directory-structure.md` |
| **백업** | `40. Docs/47. CMDS Docs/cmds-system-files/` (`_backup.md`) |
| **공유본** | `40. Docs/47. CMDS Docs/cmds-system-files-share/` (`_share.md`) |
| **웹 배포** | [system.cmdspace.work](https://system.cmdspace.work) |
| **GitHub** | [johnfkoo951/cmds-system-files](https://github.com/johnfkoo951/cmds-system-files) |
| **변경 로그** | 이 파일 (`40. Docs/47. CMDS Docs/cmds-system-files/CHANGELOG.md`) |
