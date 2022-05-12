---
date: '2020-08-24'
title: 'var, let, const의 차이점'
categories: ['JS']
summary: 'var, let, const의 차이점'
thumbnail: './js.png'
---

var 는 선언과 초기화(undefined)가 동시에 이루어진다.

let과 const는 global(window)에 저장되지 않는다.

let과 const도 호이스팅(선언문이 마치 최상단에 끌어올려진듯한 현상)  
되지만 TDZ의 영향을 받아 에러가 발생한다.

let과 const는 block scope 이고 var는 function scope 이다.
