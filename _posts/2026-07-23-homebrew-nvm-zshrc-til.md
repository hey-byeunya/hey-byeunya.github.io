---
title: "뒤돌아서면 까먹는 약어 & 용어 풀이: Homebrew, nvm, .zshrc"
date: 2026-07-23 12:06:34 +0900
categories: [TIL, 용어]
tags: [til, homebrew, nvm, zshrc, shell]
---

오늘은 macOS에서 웹 개발 환경(Node.js, npm, Git, nvm)을 세팅하다가 만난 개념들을 정리했어요.

## Q. Homebrew(brew)가 뭐예요?

**A.** macOS용 **패키지 관리자**예요. `brew install node`처럼 명령 한 줄이면 소프트웨어를 다운로드·설치·경로 설정까지 알아서 해줘요.

> 앱스토어가 GUI로 앱을 설치해준다면, Homebrew는 **터미널로 개발 도구를 설치해주는 앱스토어**라고 생각하면 쉬워요.
{: .prompt-tip }

오늘은 이걸로 Node.js와 npm을 한 번에 설치했어요.

## Q. nvm(Node Version Manager)은 왜 필요해요?

**A.** Node.js **버전을 여러 개 설치해두고 필요할 때 골라서 쓸 수 있게** 해주는 도구예요. 프로젝트마다 요구하는 Node 버전이 다를 수 있는데, nvm이 있으면 `nvm use 18`, `nvm use 20`처럼 바로 바꿔 쓸 수 있어요.

> 신발장에 여러 사이즈 신발을 걸어두고, 그날 필요한 걸 꺼내 신는 것과 비슷해요. 👟
{: .prompt-info }

`nvm install --lts`처럼 LTS(Long Term Support, 오래 안정적으로 지원되는 버전)를 바로 설치할 수도 있어요.

## Q. .zshrc는 뭐고, 왜 설정을 추가했는데 바로 안 됐어요?

**A.** `.zshrc`는 zsh 셸이 **터미널을 새로 열 때 딱 한 번 읽는 설정 파일**이에요. nvm을 쓰려면 이 파일에 "nvm을 불러와라"는 코드를 넣어줘야 하는데, 오늘 딱 그 상황을 겪었어요.

문제는 **이미 열려 있던 터미널**이었어요. `.zshrc`를 고쳐도, 이미 켜져 있는 터미널은 그 파일을 다시 읽지 않아서 `nvm: command not found`가 계속 떴던 거죠.

> `.zshrc` 수정은 **다음에 여는 터미널부터** 적용돼요. 지금 쓰는 터미널에 바로 반영하려면 `source ~/.zshrc`를 실행하세요.
{: .prompt-warning }

`source ~/.zshrc`는 "이 설정 파일을 지금 이 셸에서 다시 읽어줘"라는 명령이에요. 새 터미널을 여는 것과 똑같은 효과를 즉시 낼 수 있어요.

---

**오늘 함께 나온 용어**: Homebrew · nvm · LTS · .zshrc · source
