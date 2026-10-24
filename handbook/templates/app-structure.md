# 앱 구조

> 한눈에: 프로킷으로 만든 앱은 웹 앱 하나와 여럿이 함께 쓰는 부품 묶음(패키지)으로 나뉘어요. 화면만 만드는 프로젝트는 `apps/web`과 `packages/ui`를 고쳐요. 서버 폴더와 DB 폴더는 만들어지지만 쓰지 않아요.


| 위치 | 하는 일 | 맡는 prokit 스킬 |
|---|---|---|
| `apps/web` | Next.js App Router 화면과 라우트 핸들러(`/api/rpc`, `/api/auth`) | `prokit-ui` |
| `packages/ui` | 화면에서 함께 쓰는 shadcn 컴포넌트 | `prokit-ui` |
| `packages/api`, `packages/auth`, `packages/db` | 서버와 DB 폴더예요. 화면만 만드는 프로젝트에서는 쓰지 않아요 | 없음 |
| `packages/config` | 앱과 패키지가 함께 쓰는 공유 설정(tsconfig) | 없음 |

## 내 요청은 어디를 바꾸나

> [!TIP]
> 처음에는 폴더 이름을 몰라도 돼요. "할 일에 마감일 붙여줘"처럼 말하면 에이전트가 아래 위치 가운데 필요한 곳을 골라 고치고, 그 위치에 맞는 스킬을 읽어요.

| 이런 요청 | 바뀌는 곳 |
|---|---|
| 화면 모양, 문구, 버튼 | `apps/web`, `packages/ui` |



## 자세히

- **Next.js 문서**: 에이전트는 설치된 Next.js 판의 문서(`node_modules/next/dist/docs`)를 먼저 읽어요. 학습한 옛 API를 그대로 쓰는 일을 줄이려는 거예요.

## 관련 문서

- [템플릿이 더하는 것](what-it-adds.md)
- [prokit 스킬](../skills/prokit-skills.md)
- [설치된 프로젝트의 폴더 구조](../reference/project-structure.md)
- [케이스 A\~F·H와 대조표](../concepts/cases.md)
