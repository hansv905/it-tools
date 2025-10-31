
<picture>
  <source srcset="./.github/logo-dark.png" media="(prefers-color-scheme: light)">
  <source srcset="./.github/logo-white.png" media="(prefers-color-scheme: dark)">
  <img src="./.github/logo-dark.png" alt="로고">
</picture>

<p align="center">
개발자와 IT 종사자를 위한 유용한 도구 모음입니다. <a href="https://it-tools.tech">바로 사용해보세요!</a>
</p>



## 기능 및 로드맵

추가될 기능은 [이슈](https://github.com/CorentinTh/it-tools/issues)에서 확인할 수 있습니다.

새로운 도구 아이디어가 있으신가요? [기능 요청](https://github.com/CorentinTh/it-tools/issues/new/choose)을 제출해주세요!


## 셀프 호스팅

개인 서버에서 직접 호스팅하는 방법

**Docker Hub에서 설치:**


```sh
docker run -d --name it-tools --restart unless-stopped -p 8080:80 corentinth/it-tools:latest
```

**GitHub 패키지에서 설치:**

```sh
docker run -d --name it-tools --restart unless-stopped -p 8080:80 ghcr.io/corentinth/it-tools:latest
```

**기타 솔루션:**

- [Cloudron](https://www.cloudron.io/store/tech.ittools.cloudron.html)
- [Tipi](https://www.runtipi.io/docs/apps-available)
- [Unraid](https://unraid.net/community/apps?q=it-tools)


## 기여하기

### 추천 IDE 설정

[VSCode](https://code.visualstudio.com/)와 아래 확장 프로그램을 추천합니다:

- [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (Vetur 비활성화 필요)
- [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [i18n Ally](https://marketplace.visualstudio.com/items?itemName=lokalise.i18n-ally)

아래와 같은 설정을 권장합니다:

```json
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "i18n-ally.localesPaths": ["locales", "src/tools/*/locales"],
  "i18n-ally.keystyle": "nested"
}
```


### `.vue` 타입 지원

TypeScript는 기본적으로 `.vue` 타입 정보를 처리하지 못하므로, 타입 체크 시 `tsc` 대신 `vue-tsc`를 사용합니다. 에디터에서는 [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) 확장으로 `.vue` 타입을 인식시켜야 합니다.

만약 독립형 TypeScript 플러그인이 느리게 느껴진다면, Volar의 [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669)를 활성화하면 더 빠르게 사용할 수 있습니다. 방법은 다음과 같습니다:

1. 내장 TypeScript 확장 비활성화
  1. VSCode 명령 팔레트에서 `Extensions: Show Built-in Extensions` 실행
  2. `TypeScript and JavaScript Language Features`를 찾아서 우클릭 후 `Disable (Workspace)` 선택
2. 명령 팔레트에서 `Developer: Reload Window` 실행하여 VSCode를 재시작


### 프로젝트 설정

```sh
pnpm install
```

### 개발용 컴파일 및 핫 리로드

```sh
pnpm dev
```

### 프로덕션용 타입 체크, 컴파일 및 최적화

```sh
pnpm build
```

### [Vitest](https://vitest.dev/)로 단위 테스트 실행

```sh
pnpm test
```

### [ESLint](https://eslint.org/)로 린트 실행

```sh
pnpm lint
```

### 새로운 도구 생성

새로운 도구를 만들려면, 아래 스크립트를 실행하세요:

```sh
pnpm run script:create:tool my-tool-name
```

`src/tools`에 디렉토리와 필요한 파일이 생성되고, `src/tools/index.ts`에 자동으로 import가 추가됩니다. 이후 카테고리에 맞게 도구를 등록하고 개발을 진행하면 됩니다.


## 기여자

이미 기여해주신 모든 분들께 감사드립니다!

[![contributors](https://contrib.rocks/image?repo=corentinth/it-tools&refresh=1)](https://github.com/corentinth/it-tools/graphs/contributors)


## 크레딧

[Corentin Thomasset](https://corentin.tech?utm_source=it-tools&utm_medium=readme)가 ❤️를 담아 개발했습니다.

이 프로젝트는 [vercel.com](https://vercel.com)을 통해 지속적으로 배포됩니다.

기여자 그래프는 [contrib.rocks](https://contrib.rocks/preview?repo=corentinth/it-tools)로 생성되었습니다.

<a href="https://www.producthunt.com/posts/it-tools?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-it&#0045;tools" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=345793&theme=light" alt="IT&#0032;Tools - Collection&#0032;of&#0032;handy&#0032;online&#0032;tools&#0032;for&#0032;devs&#0044;&#0032;with&#0032;great&#0032;UX | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
<a href="https://www.producthunt.com/posts/it-tools?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-it&#0045;tools" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=345793&theme=light&period=daily" alt="IT&#0032;Tools - Collection&#0032;of&#0032;handy&#0032;online&#0032;tools&#0032;for&#0032;devs&#0044;&#0032;with&#0032;great&#0032;UX | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>


## 라이선스

이 프로젝트는 [GNU GPLv3](LICENSE) 라이선스를 따릅니다.
