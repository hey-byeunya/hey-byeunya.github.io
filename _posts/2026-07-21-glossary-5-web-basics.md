---
title: "개발 용어사전 ⑤ 웹 기초 — GUI·CSS·DOM·JSON"
date: 2026-07-21 11:00:00 +0900
categories: [개발 용어사전, 웹]
tags: [gui, css, dom, json, web]
---

개발 용어 Q&A 다섯 번째 편. 웹을 이루는 기초 용어들입니다. (MDN 한국어 문서를 참고했어요.)

## Q. GUI가 뭐예요?

**A.** Graphical User Interface. 버튼·아이콘 같은 **그래픽으로 조작**하는 화면 방식이에요. 명령어를 키보드로 입력하는 CLI(Command Line Interface)와 대비돼요. 앱 아이콘을 눈으로 보고 탭해서 여는 게 GUI예요. 🖱️

## Q. CSS는요?

**A.** Cascading Style Sheets. 웹페이지를 **꾸미는** 언어예요(색·글꼴·배치). 집짓기로 치면 페인트·벽지·가구 배치죠. HTML(뼈대)에 CSS를 입히면 살고 싶은 집이 돼요. 🎨

## Q. DOM은 뭔가요?

**A.** Document Object Model. 브라우저가 HTML을 **프로그램이 다룰 수 있게** 바꿔놓은 나무(트리) 구조예요.

```javascript
document.querySelector("h1").textContent = "반가워요!";
```

> 웹페이지가 인형극 무대라면 — HTML은 대본, DOM은 무대에 세워진 인형들, JavaScript는 인형을 움직이는 조종사예요. 🎭
{: .prompt-info }

## Q. JSON은요?

**A.** JavaScript Object Notation. 데이터를 주고받는 **글자 형식**이에요. 객체와 닮았지만 키에 따옴표가 필수이고, 함수는 못 담아요.

```json
{
  "name": "은아",
  "age": 25,
  "hobbies": ["코딩", "독서"]
}
```

> 객체(가구)를 납작하게 포장한 배송용 설명서가 JSON이에요. 프로그램·언어끼리 소통하는 공통 언어죠. 📄
{: .prompt-tip }

---

*다음 편: 네트워크 (LAN, WAN, 사설 IP, HTTP, API)*
