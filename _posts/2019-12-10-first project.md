---
layout : post
title : "first project Foodo"
comments: true
---
[first project 회고]
### Foodo - 냉장고 재고 관리 웹 어플리케이션
2019.11 2주간 진행
<br/>
---
- 냉장고의 식재료들을 기억하여 관리하기 어렵다는 것에서 출발한 프로젝트
- 재고를 한눈에 볼수 있으며, 재고 추가수정삭제가 가능하며, 수량 조절 가능, 유통기한 표기하여 사용자 편의성을 높였다.
- 해당 재료들을 바탕으로 요리 가능한 메뉴 추천 기능까지 구현 목표 -> 유투브 API 통해 추천 리스트 보여주었다.
<br/>
<br/>
---
#### [back-end]
<br/>
node.js, express, sequelize, mysql
<br/>
<br/>
---
#### 서비스 소개
<br/>
https://slides.com/bangsil/deck-3#/2
<br/>
<br/>

---
back-end 쪽을 맡게 되어 데이터 구조 설계 작업 부터 시작하였다.
<br/>
#### 구조 설계
<br/>
![데이터구조](<http://ginsum.github.io/images/2019-12-10-17-03-13.png>)
<br/>
크게 user(회원) 와 ingredient(재료들) 목록 테이블을 구성하고, 냉장고에 보관되는 재고 테이블(user-ingredient)을 만들어 user와 ingredient 관계를 형성하는 것으로 구조를 만들었다. 저장되는 재고 테이블 안에는 유효기간, 수량, 메모, 냉장/냉동 여부 등의 필드를 생성해 해당 내용을 저장할 수 있게 하였다.
<br/>
가지고 있는 재고를 바탕으로 메뉴 추천을 할 수 있도록 menu와 ingredient 테이블간의 관계도 형성하였다.
<br/>
<br/>
---
#### API 생성
client 쪽에 보내줄 API를 작성하였다. 크게 회원(/users)과 재고(/ingredients), 메뉴(/menus)로 나누어 endpoint를 만들었다. 
restful 한 API를 만들지 못한 것 같아 아쉬움이 남는다.
<br/>
![API](<http://ginsum.github.io/images/2019-12-10-17-38-17.png>)
<br/>
<br/>
---
#### Database 생성
<br/>
sequelize로 각각 테이블별로 Models 파일을 만들고 user-indegrients 와 ingredients 관계 테이블을 만들기 위해 association 사용하였다.
쿼리문에서 join을 이용해보았지만 sequelize에서는 어떻게 적용해야 하는지 처음에는 알수가 없어서 많이 공부해야 하는 시간들이었다. ingredients와 user- indegrients 이 일대다 관계였기 때문에 hasmany와 belongsTo를 사용하여 association을 설정해주어 userId 필드가 생성되었고, find할때 include 를 사용하여 user 정보를 함께 불러올수 있었다.
<br/>
<br/>
---

#### ENDPOINT 작성
<br/>
회원(/users)과 재고(/ingredients), 메뉴(/menus)로 나누어 라우터로 분기한 후 각각 필요한 endpoint별 기능들을 작성하였다. 재고 부분 같은 경우 CRUD가 가능하도록 기능을 모두 만들어주었는데 처음 작성했을때와 시간이 흐른뒤 새로운 기능이나 빠뜨린 기능을 추가 하면서 API request와 response가 달라진 부분들이 있었는데 그 부분을 front 쪽에 제때 전달하지 못하면서 버그가 발생하는 일이 있었다. 다시 한번 API 작성의 중요성에 대해 생각할 수 있었으며 같은 실수를 반복하지 않기 위해 노력하였다.
<br/>
<br/>
#### 





