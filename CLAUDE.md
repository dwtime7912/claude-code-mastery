# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 언어 및 커뮤니케이션 규칙

- **기본 응답 언어**: 한국어
- **코드 주석**: 한국어로 작성
- **커밋 메시지**: 한국어로 작성
- **문서화**: 한국어로 작성
- **변수명/함수명**: 영어 (코드 표준 준수)

## 프로젝트 개요

개발자 웹 이력서 프로젝트. 단일 페이지 스크롤 방식(SPA 스타일)으로 구성된 정적 웹사이트.

**기술 스택:** HTML5, CSS3, Vanilla JavaScript, Tailwind CSS

## 아키텍처

빌드 도구 없는 순수 정적 파일 구조. Tailwind CSS는 CDN 방식으로 적용.

```
resume/
├── index.html      # 진입점 — 모든 섹션 포함
├── style.css       # Tailwind 외 커스텀 스타일
├── main.js         # 스크롤 애니메이션, 다크모드 토글, 햄버거 메뉴
└── assets/images/  # 프로필 이미지 등 정적 자산
```

**페이지 섹션 순서:** Hero → About → Skills → Projects → Experience → Education → Contact

## 개발 방법

별도의 빌드 과정 없음. 브라우저에서 `index.html`을 직접 열거나 로컬 서버로 실행:

```bash
# Python 로컬 서버 (resume/ 디렉토리 내에서 실행)
python -m http.server 8080

# VS Code Live Server 확장 사용 시
# index.html 우클릭 → "Open with Live Server"
```

## 디자인 컨셉

| 항목 | 내용 |
|------|------|
| 폰트 | Noto Sans KR (한글), Inter (영문) |
| 색상 테마 | 다크 네이비 + 포인트 컬러 (파랑/보라) |
| 다크모드 | Tailwind `dark:` 클래스 + JS 토글 |
| 애니메이션 | 스크롤 진입 시 페이드인 효과 |

## 참고 문서

- 단계별 개발 계획: [ROADMAP.md](./ROADMAP.md)
