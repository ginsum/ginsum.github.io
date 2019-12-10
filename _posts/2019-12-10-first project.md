---
layout : post
title : "first project Foodo"
comments: true
---


<br/>
<br/>
### Foodo
first project 회고

냉장고 재고 관리 웹 어플리케이션

--
냉장고의 식재료들을 기억하여 관리하기 어렵다는 것에서 출발한 프로젝트
재고를 한눈에 볼수 있으며, 재고 추가수정삭제가 가능하며, 수량 조절 가능, 유통기한 표기, 
해당 재료들을 바탕으로 요리 가능한 메뉴 추천 기능까지 구현 목표 -> 유투브 API 통해 추천 리스트 보여줌

--
[back-end]
node.js, express, sequelize, mysql

--
서비스 소개
https://slides.com/bangsil/deck-3#/2


--
back-end 쪽을 맡게 되어 데이터 구조 설계 작업 부터 시작하였다.
![데이터구조](<http://ginsum.github.io/images/2019-12-10-17-03-13.png>)

크게 user(회원) 와 ingredient(재료들) 목록 테이블을 구성하고, 저장되는 재고 테이블을 만들어 user와 ingredient 관계를 형성하는 것으로 구조를 만들었다. 저장되는 재고 테이블 안에는 유효기간, 수량, 메모, 냉장/냉동 여부 등의 필드를 생성해 해당 내용을 저장할 수 있게 하였다.
가지고 있는 재고를 바탕으로 메뉴 추천을 할 수 있도록 menu와 ingredient 테이블간의 관계도 형성하였다.

--
API 생성
client 쪽에 보내줄 API를 작성하였다. 크게 회원과 재고, 메뉴로 나누어 endpoint를 만들었다. 
restful 한 API를 만들지 못한 것 같아 아쉬움이 남는다.
![API](<http://ginsum.github.io/images/2019-12-10-17-38-17.png>)

--








