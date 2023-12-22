<br/>
<br/>

<p align="center">
<img src="https://files.cloudtype.io/logo/cloudtype-logo-horizontal-black.png" width="50%" alt="Cloudtype"/>
</p>

<br/>
<br/>

# 클라우드타입 웨비나 #04<br/>스타트업 운영에 필요한 <br> 랜딩 & 도큐멘테이션 한 번에 해결하기 <!-- omit in toc -->

## 목차 <!-- omit in toc -->

- [🗒️ 실습 예제](#️-실습-예제)
- [🖇️ 준비사항](#️-준비사항)
- [🗒️ 실습 예제 사양](#️-실습-예제-사양)
- [🏠 랜딩페이지 배포하기](#-랜딩페이지-배포하기)
  - [GitHub 저장소 clone](#github-저장소-clone)
- [📈 Umami 배포 및 랜딩페이지 적용하기](#-umami-배포-및-랜딩페이지-적용하기)
  - [Umami 초기 계정](#umami-초기-계정)
  - [Websites 설정](#websites-설정)
  - [랜딩페이지 재배포](#랜딩페이지-재배포)
- [Notion 커스텀 페이지 배포](#notion-커스텀-페이지-배포)
  - [Notion 페이지 ID 확인](#notion-페이지-id-확인)
  - [Notion 페이지 ID 적용](#notion-페이지-id-적용)
- [📋 Ghost 블로그 배포하기](#-ghost-블로그-배포하기)
  - [Ghost 초기 설정 및 글 작성하기](#ghost-초기-설정-및-글-작성하기)
- [🦖 Docusaurus 배포하기](#-docusaurus-배포하기)
- [🟢 Uptime Kuma 배포 및 적용하기](#-uptime-kuma-배포-및-적용하기)
  - [관리자 계정 생성](#관리자-계정-생성)
- [📖 References](#-references)
- [💬 Contact](#-contact)

## 🗒️ 실습 예제

- **랜딩페이지**
  - [Nextplate by Zeon studio](https://github.com/zeon-studio/nextplate)
- **노션페이지**
  - [Next.js Notion Starter Kit by Travis Fischer](https://github.com/transitive-bullshit/nextjs-notion-starter-kit)
- **블로그**
  - [Ghost](https://ghost.org/)
- **개발 문서**
  - [Docusaurus](https://docusaurus.io/)
- **서비스 상태 모니터링**
  - [Uptime Kuma](https://uptime.kuma.pet/)
- 웹 사이트 트래픽 추적 및 분석
  - [Umami](https://umami.is/)

## 🖇️ 준비사항

- [클라우드타입 계정](https://cloudtype.io/)
- [Notion](https://www.notion.so/)
- [GitHub 계정](https://github.com/)


## 🗒️ 실습 예제 사양

- Node v18.19.0 이상


## 🏠 랜딩페이지 배포하기

### GitHub 저장소 clone

```bash
git clone https://github.com/cloudtype-examples/webinar-04-landing.git
```

## 📈 Umami 배포 및 랜딩페이지 적용하기

### Umami 초기 계정

- Username: admin
- Password: umami

### Websites 설정

Umami에서 추가한 웹 사이트의 **Tracking Code** 탭에서 코드를 복사한 후 HTML `<head>` 태그 내부에 작성합니다.

<img src="https://files.cloudtype.io/webinar/webinar-04-01.png" width="90%" alt="Cloudtype"/>

### 랜딩페이지 재배포

클라우드타입에서 랜딩페이지를 재배포 하여 Umami를 적용합니다.

<img src="https://files.cloudtype.io/webinar/webinar-04-02.png" width="90%" alt="Cloudtype"/>

## Notion 커스텀 페이지 배포

### Notion 페이지 ID 확인

Notion 페이지의 링크를 복사한 뒤 다음 표시된 부분의 페이지 ID를 확인합니다.

```
https://www.notion.so/<페이지 ID>?pvs=4
```

### Notion 페이지 ID 적용

다음의 저장소를 clone 한 뒤, `site.config.js` 의 다음 부분에 위에서 확인한 페이지 ID를 작성합니다. 

```bash
git clone https://github.com/cloudtype-examples/webinar-04-notion.git
```

```typescript
import { siteConfig } from './lib/site-config'

export default siteConfig({
  // the site's root Notion page (required)
  rootNotionPageId: '<페이지 ID>',
  // if you want to restrict pages to a single notion workspace (optional)
  // (this should be a Notion ID; see the docs for how to extract this)
  rootNotionSpaceId: null,
  ...
```


## 📋 Ghost 블로그 배포하기

### Ghost 초기 설정 및 글 작성하기

```
https://<호스트>/ghost
```

## 🦖 Docusaurus 배포하기

## 🟢 Uptime Kuma 배포 및 적용하기

### 관리자 계정 생성

배포 후 최초 접속 시 관리자 계정 생성이 진행됩니다.

<img src="https://files.cloudtype.io/webinar/webinar-04-03.png" width="90%" alt="Cloudtype"/>

대시보드에서 모니터링 대상을 추가합니다.
모니터링 주기 등 각종 설정을 상황에 맞게 변경할 수 있습니다.

<img src="https://files.cloudtype.io/webinar/webinar-04-04.png" width="90%" alt="Cloudtype"/>


## 📖 References

- [클라우드타입 Docs](https://docs.cloudtype.io/)
- [클라우드타입 FAQ](https://help.cloudtype.io/guide/faq)
- [Nextplate by Zeon studio](https://github.com/zeon-studio/nextplate)
- [Next.js Notion Starter Kit by Travis Fischer](https://github.com/transitive-bullshit/nextjs-notion-starter-kit)

## 💬 Contact

- [Discord](https://discord.gg/U7HX4BA6hu)