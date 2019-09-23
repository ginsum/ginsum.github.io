---
layout : post
title : "javascript - prototype"
comments: true
---

## javascript - prototype

자바스크립트는 프로토타입 기반 객체지향 프로그래밍 언어이다.
<br/>
자바스크립트의 모든 객체는 자신의 부모 역할을 담당하는 객체와 연결. 이러한 부모 객체를 Prototype 객체라고 한다. <br/>
<br/>
- 모든 function 에는 프로토타입 속성을 가지고 있다.
<br/>
- constructor 객체 입장에서 자신을 생성한 객체를 가르킴
<br/> 
- prototype chain<br/>
자바스크립트는 특정 객체의 프로퍼티나 메소드에 접근할때 해당 객체에 해당 프로퍼티나 메소드가 없으면 __proto__를 따라 올라가며 검색한다.
<br/>
<br/>
![](<http://ginsum.github.io/images/2019-09-23-01.png>)