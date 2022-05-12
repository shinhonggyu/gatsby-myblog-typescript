---
date: '2020-08-23'
title: 'SPA, CSR, SSG, ISR, SSR'
categories: ['WEB', 'React', 'JAMstack']
summary: 'Pre-redering'
thumbnail: './question.jpg'
---

React.js  
브라우저에서 Java Script가 모든 렌더링을 책임진다.

CSR -> 유저 request -> 서버는 빈 html과 link를 보낸다 -> 브라우저는 HTML & JS 를 다운받는다 -> 유저는 빈화면을 보고 JS load가 되면 클릭할수있다.

Next.js , Gatsby.js 같은 JAMstack 프레임워크
Pre-rendering (서버가 렌더링을 책임진다).

git push -> build -> create generate file -> store CDN

SSG -> build타임때 HTML이 생성되어 cdn 에 저장된다.  
유저 리퀘스트 -> 서버는 static HTML과 조금의 데이터를 함께 보낸다.  
-> HTML을 렌더링하고 JS를 다운을 받는다 -> 유저는 바로 볼수있고 JS 다운이 되면 반응할수있다.

외부 데이터가 있을때 getStaticProps => build시에 서버에서만 실행 클라이언트 번들 포함하지않는다.  
개발환경에서는 클라이언트 와 서버에서 실행

ISR -> HTML is generated at a specific Interval

SSR -> 유저가 매번 request 할때마다 new HTML이 생성된다.
