---
date: '2020-08-23'
title: '브라우저 렌더링 과정'
categories: ['WEB']
summary: '브라우저 렌더링 과정'
thumbnail: './macbook.jpg'
---

나도 다른 사람들처럼
url에 google.com을 입력했을때 일어나는 일이 무었인지 알아보았다.

1. HTML파일 과 CSS파일을 파싱해서 DOM Tree와 CSSOM Tree를 만든다.

2. 두 Tree를 결합하여 Render Tree를 만든다.

3. Render Tree에서 각 노드의 위치와 크기를 계산하여 배치한다 (Layout)

4. 각 노드를 화면상의 실제 픽셀로 변환하고 레이어를 만든다. (Paint)

5. 레이어를 합성하여 실제화면에 나타낸다 (Composite)
