---
title: "개발 용어사전 ② 개발 도구·환경 — npm부터 Git까지"
date: 2026-07-21 14:00:00 +0900
categories: [개발 용어사전, 개발 도구]
tags: [npm, nodejs, nvm, ide, git, markdown]
---

개발 용어 Q&A 두 번째 편. 코딩할 때 매일 만나는 도구와 환경을 정리했습니다. 🛠️

## Q. npm이 뭐예요?

**A.** Node Package Manager. JavaScript 패키지(라이브러리)를 설치·관리하는 도구예요. 앱스토어에서 앱을 설치하듯, 남이 만든 코드 부품을 가져다 씁니다. 📦

## Q. Node.js는 언어인가요?

**A.** 아니요, **언어가 아니라 실행 환경**이에요. 원래 JavaScript는 브라우저 안에서만 돌았는데, Node.js 덕분에 컴퓨터·서버에서도 JS를 실행할 수 있게 됐어요.

> JavaScript(배우)가 브라우저(극장)뿐 아니라 스튜디오(Node)에서도 연기하게 해주는 거예요. 🎬
{: .prompt-info }

## Q. nvm은요?

**A.** Node Version Manager. Node의 여러 버전을 설치하고 휙휙 전환하는 도구예요. 게임 카트리지를 갈아 끼우듯 버전을 바꿀 수 있죠. 🎮

## Q. Python의 pip, uv는 뭔가요?

**A.** Python 패키지 관리 도구예요. `pip`은 기본, `uv`는 Rust로 만든 **초고속** 신형이에요. pip이 기본 자동차라면 uv는 최신 전기 스포츠카예요.

## Q. IDE, LSP, diff — 한 번에 정리하면?

**A.**

| 용어 | 뜻 | 한 줄 |
|------|-----|-------|
| **IDE** | Integrated Development Environment | 편집·실행·디버깅을 모아둔 "주방" 🍳 |
| **LSP** | Language Server Protocol | 자동완성·오류표시를 표준화한 규격 |
| **diff** | difference | 두 코드의 달라진 부분(+/−)만 보여줌 |

> diff는 틀린그림찾기예요 — 다른 부분에만 동그라미. 📝
{: .prompt-tip }

## Q. 마크다운(.md)은 뭐예요?

**A.** `#`, `**굵게**`, `-` 같은 간단한 기호로 서식을 넣는 쉬운 문서 문법이에요. 최종적으로 HTML로 변환돼요. 복잡한 요리(HTML) 대신 간단한 라면 같은 거죠. 🍜 (이 블로그 글도 마크다운으로 씁니다.)

## Q. .env, PR, .DS_Store는?

**A.**
- **.env** — 비밀번호·API 키 같은 민감정보를 담는 파일. 코드와 분리된 **금고** 🔐. 절대 Git에 올리면 안 돼요(`.gitignore`에 추가).
- **PR (Pull Request)** — 내 코드 변경을 원본에 합쳐달라는 요청. "제 부분 검토해 주세요" 하고 제출하는 조별 과제 같은 거예요.
- **.DS_Store** — macOS가 폴더 보기 설정을 저장하려 자동 생성하는 숨김 파일. 프로젝트와 무관하니 Git에서 무시하세요.

> 비밀번호·키는 `.env`에 넣고 `.gitignore`로 제외하는 게 보안의 기본이에요.
{: .prompt-warning }

---

*다음 편: 프로그래밍 언어 (Python, JavaScript, TypeScript)*
