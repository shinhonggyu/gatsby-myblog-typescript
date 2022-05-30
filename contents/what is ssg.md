---
date: '2022-05-28'
title: 'What is Static Site Generation?'
categories: ['SSG', 'ISR', 'SSR', 'CSR']
summary: 'How Next.js Uses SSG for Dynamic Web Apps'
thumbnail: './SSG.png'
---

정적 웹사이트는 웹 자체만큼이나 오래되었습니다.

오늘날 자바스크립트의 부상으로 정적웹사이트를 보다 동적으로 만들수있게 되었습니다.

정적 생성은 빌드 시 웹 또는 앱을 컴파일하고 렌더링하는 프로세스를 설명합니다.

우리가 전통적으로 알고 있는 자바스크립트 기반 웹앱은 브라우저에서 런타임에 React또는 scripts 같은 라이브러리를 실행하여 작동합니다.

브라우저가 페이지를 수신하면 일반적으로 콘텐츠가 많지않은 단순한 HTML 입니다.

그런다음 모든 콘텐츠를 페이지로 당겨오는(pull) scripts를 실행합니다.
hydration 이라고도 합니다.

Next.js 같은 툴은 빌드시 컴파일타임에 페이지를 렌더하고 cdn 에 저장합니다.
이를 통해 첫 번째 로드 시 전체 콘텐츠를 제공 할 수 있습니다.

기본적으로 Next.js는 가능한 모든 페이지를 정적으로 생성하려고 시도합니다.

앱이 데이터를 가져오는 방법을 감지하여 이를 수행합니다.

Next.js는 getStaticProps, getServerSideProps, getStaticPaths, ISR 등의 데이터를 가져오는 API를 제공합니다.

그리고 이 API의 사용방법에 따라 Next.js는 앱을 빌드하는 방법을 결정합니다.

만약 getStaticProps만 사용하여 데이터를 가져오는 경우,
Next.js는 빌드 시 해당 데이터를 가져와 완전한 정적 페이지를 남깁니다.

만약 getServerSideProps를 사용할경우 Next.js는 앱이 해당 페이지를 렌더링하기 위해 서버가 필요하다는것을 알게됩니다.

서버 구성을 자동으로 처리하는 Vercel과 같은 배포 솔루션과 함께 Next.js는 누군가 서버에서 페이지를 요청할때 데이터를 로드합니다.
