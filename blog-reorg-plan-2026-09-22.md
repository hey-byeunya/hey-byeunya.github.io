# hey-byeunya.github.io 재정비 계획서

**생성일**: 2026-09-22 · **대상**: `_posts/` 전체 24편

## 요약

블로그 24편 중 79%(19편)가 "개발 용어사전" 카테고리에 몰려 있고, 그중에서도 "AI" 서브카테고리 하나가 전체의 37.5%(9편)를 차지합니다. 태그는 `til` 표기·한글/영어 혼용·`ai-agent`/`agent` 표기가 갈라져 있고, 용어사전 19편은 사실상 하나의 연작인데 공식 시리즈 기능 없이 카테고리로만 묶여 있습니다.

## 우선순위

1. (쉬움) **태그 표기 통일** — 아래 3건, 파일 4개만 고치면 됨
2. (중간) **"AI" 서브카테고리 분리** — 9편이나 되니 지금 손 안 대면 계속 커짐
3. (선택) **시리즈 기능 도입** — 급하진 않지만 19편이 쌓인 지금이 적기

---

## 1. 태그 정리 _(태그 정리 담당)_

전체 24편의 태그를 훑은 결과 세 가지 구체적 불일치를 찾았습니다.

**① `til` 태그 누락 — 용어사전 1~8편만 빠짐.** [glossary-1-terminal-shell.md], [glossary-2-dev-tools.md], [glossary-3-languages.md], [glossary-4-language-concepts.md], [glossary-5-web-basics.md], [glossary-6-network.md], [glossary-7-data-security.md], [glossary-8-ai-concepts.md] (전부 2026-07-21 발행) 8편은 `til` 태그가 없습니다. 반면 같은 날 이후 발행된 [homebrew-nvm-zshrc-til.md]부터 최신 [nlp-worldmodel-til.md]까지 11편은 전부 `til`이 붙어 있습니다 — 파일명에도 `-til` 접미사가 이때부터 생겼습니다. **1~8편도 초기 시리즈였다는 점에서 `til` 태그를 소급 추가하는 게 일관성 있습니다.**

**② `ai-agent` vs `agent` 표기 혼용.** [nlp-worldmodel-til.md] 한 편만 태그가 `agent`이고, 나머지 5편([glossary-8-ai-concepts.md], [claude-agents-skill-md-til.md], [five-weeks-retrospective.md], [agent-harness.md], [agent-eval-terms-til.md], [main-quest-4-retrospective.md])은 전부 `ai-agent`입니다. `nlp-worldmodel-til.md`의 `agent`를 `ai-agent`로 바꾸는 게 맞습니다.

**③ 한글/영어 혼용 — "딥러닝" 개념.** [ml-dl-fundamentals-til.md]은 태그에 `딥러닝`·`머신러닝`(한글)을 쓰는데, [deep-learning-architectures-til.md]은 같은 상위 개념을 `deeplearning`(영어)으로 씁니다. 블로그 전체가 한글 본문 위주니 **한글 태그(`딥러닝`)로 통일**을 제안합니다.

- **충분**: true

---

## 2. 카테고리 구조 _(카테고리 구조 담당)_

실제 분포를 셌습니다: 일상 1편, 프로젝트 2편([tissue-flying-prd.md], [agent-harness.md]), 회고 2편([five-weeks-retrospective.md], [main-quest-4-retrospective.md]), **개발 용어사전 19편**.

용어사전 19편 내부 서브카테고리 분포:

| 서브카테고리 | 편수 | 해당 글 |
|---|---|---|
| AI | **9편** | [glossary-8-ai-concepts.md], [ml-dl-fundamentals-til.md], [claude-agents-skill-md-til.md], [computer-vision-til.md], [deep-learning-architectures-til.md], [generative-ai-foundation-models-til.md], [llm-training-pipeline-til.md], [agent-eval-terms-til.md], [nlp-worldmodel-til.md] |
| 개발 도구 | 3편 | [glossary-2-dev-tools.md], [homebrew-nvm-zshrc-til.md], [dev-tools-misc-til.md] |
| 데이터·보안 | 2편 | [glossary-7-data-security.md], [security-api-til.md] |
| 터미널·셸 / 프로그래밍 언어 / 언어 개념 / 웹 / 네트워크 | 각 1편 | [glossary-1], [glossary-3], [glossary-4], [glossary-5], [glossary-6] |

**"AI" 서브카테고리 하나가 전체 블로그(24편)의 37.5%를 차지합니다.** 다른 서브카테고리는 1~3편인데 AI만 9편이라 균형이 깨져 있습니다. 제안: AI를 다시 쪼개기 — 예를 들어 `AI 기초`(glossary-8, ml-dl-fundamentals) / `AI 모델 아키텍처`(computer-vision, deep-learning-architectures, generative-ai-foundation-models, llm-training-pipeline) / `AI 에이전트`(claude-agents-skill-md, agent-eval-terms, nlp-worldmodel)로 3분할하면 다른 서브카테고리들과 규모가 비슷해집니다.

- **충분**: true

---

## 3. 시리즈 구성 _(시리즈 구성 담당)_

"뒤돌아서면 까먹는 약어 & 용어 풀이: ..."로 시작하는 제목을 가진 글이 **19편 전부**입니다 (위 용어사전 19편과 정확히 일치). 이게 사실상 하나의 연작인데, 지금은 파일명으로만 흔적이 남아있습니다 — [glossary-1-terminal-shell.md]부터 [glossary-8-ai-concepts.md]까지는 파일명에 번호(`glossary-N`)가 있지만, 2026-07-23 이후 11편은 파일명이 `{주제}-til.md` 형식으로 바뀌면서 **번호가 사라졌습니다.**

Jekyll Chirpy는 `categories`의 두 번째 값을 "collection"처럼 활용하거나, `_tabs`에 시리즈 전용 인덱스 페이지를 만드는 기능을 지원합니다. 19편이 쌓인 지금이 시리즈 인덱스 페이지(예: `/glossary/`)를 하나 만들 시점으로 보입니다 — 독자가 "용어사전 전체 목록"을 한 번에 보게 됩니다.

- **충분**: false
- **부족**: Chirpy의 정확한 collection/시리즈 문법은 `_config.yml`을 직접 확인 안 해서 본인 확인 필요합니다.

---

## 4. 콘텐츠 품질 _(콘텐츠 품질 담당)_

**겹침 검토**: [glossary-8-ai-concepts.md](LLM·Agent·MCP 개념 입문)와 이후 8편(ml-dl-fundamentals부터 nlp-worldmodel까지)을 비교했을 때, 서로 다른 세부 주제(파운데이션 모델·비전·학습 파이프라인·평가 등)를 다뤄 내용이 겹치진 않습니다. glossary-8이 입문, 나머지가 심화로 자연스럽게 이어집니다.

**오래됨 검토**: [hello-world.md](2026-07-10)는 매우 짧은 자기소개 글인데, 그 이후 23편이 쌓였습니다. "앞으로 정리할 내용"이라고 예고한 목록(개발하며 배운 것·문제 해결 과정·회고)이 실제로 다 채워졌으니, 지금 글 목록을 반영해 업데이트할 만합니다.

**회고 시리즈**: [five-weeks-retrospective.md](07.24~08.28)와 [main-quest-4-retrospective.md](08.31~09.10)가 시간순으로 이어지는 회고 연작입니다. 3번째 회고가 이어질 가능성이 높으니, 이것도 시리즈 담당 항목(3번)과 함께 시리즈 인덱스에 포함을 고려하세요.

- **충분**: false
- **부족**: 본문 전체를 다 읽지 않고 앞부분(400자)만 봤기 때문에, "업데이트가 꼭 필요한지"는 본인이 각 글을 다시 읽고 판단해야 정확합니다.

---

## ⑥ 평가 체크리스트

- [x] 절마다 최소 3개 이상 구체적 파일명 인용 — 4개 절 전부 충족
- [x] 제안된 체계가 24편 전체와 충돌 안 하는지 — 카테고리 재분류안은 AI 9편 안에서만 재배치, 다른 카테고리 영향 없음
- [ ] "본인 확인 필요" 항목 — 3번(Chirpy 시리즈 문법), 4번(콘텐츠 업데이트 필요 여부) **아직 본인 판단 필요**
- [x] 우선순위 정해짐 — 위 [우선순위] 참고, 태그 정리부터 시작 권장
