---
date: '2022-05-31'
title: 'this'
categories: ['WEB']
summary: ''
thumbnail: './js.png'
---

객체지향 언어에서 this는 클래스로 생성산 인스턴스 객체를 가르킵니다.

1. this ?
2. this 바인딩 규칙
3. 화살표 함수의 this
4. 클래스에서의 this

객체는 상태를 나타내는 property와
동작을 나타내는 method로 이루어져 있습니다.

this를 사용하여 자신이 속한 객체나 자신이 생성한 인스턴스를 참조 할 수 있습니다.

자바스크립트에서의 this는 함수를 호출할때 동적으로 결정됩니다.

- 일반 함수 호출 (기본 바인딩) 전역객체 or undefined

- 메서드 호출 (암시적 바인딩) 호출 객체

- 생성자 함수 호출 (new 바인딩) 생성자 함수내에서의 this는 인스턴스 객체가 바인딩된다.

- Function.prototype.apply/call/bind 메서드에 의한 간접 호출 (명시적 바인딩 - this로 사용할 객체 전달)

우선순위 new > 명시적 > 암시적 > 기본

- 화살표 함수에서의 this 호출시 상위 스코프의 this에 접근
