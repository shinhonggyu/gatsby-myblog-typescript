---
date: '2022-05-30'
title: '내주변 카페 찾기'
categories: ['Web', 'SEO', 'Next.js', 'SSG', 'CSR', 'API', 'Airtable']
summary: '내 주변 커피집을 찾을수있는 웹.'
thumbnail: './coffee-stores.png'
---

첫번째 페이지의 상점들은 getStaticProps로 정적 페이지 입니다.

버튼을 클릭할경우 geolocation api 로 사용자의 위치 정보를 가져온다음

FOURSQUARE_API 로 내주변의 상점을 useEffect를 활용해 클라이언트 사이드 렌더링을 합니다.

가져온 상점들은 context로 글로벌 상태로 저장합니다.

각 상점 페이지에서는 미리 getStaticPaths로 빌드시 pre-render 된 상점은 바로 DB에 저장하고

이외에는 useEffect로 클라이언트 상태 context에서 id가 일치하는 상점을 가져와 렌더링한 후 Airtable DB에 저장합니다.

그리곤 useSwr 훅 으로 상점을 가져와 DB와 동기적으로 클라이언트 사이드 렌더링을 합니다.

upVote 버튼으로 좋아요를 누를수있고 db와 동기화됩니다.

[https://discover-coffee-stores-pi.vercel.app/](https://discover-coffee-stores-pi.vercel.app/)
