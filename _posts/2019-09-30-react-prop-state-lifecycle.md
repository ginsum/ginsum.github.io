---
layout : post
title : "React - props, state, life cycle"
comments: true
---

##React - props, state, life cycle

<br/>
<br/>
### component

componet 정의 방법
1. javaScript 함수 작성
2. ES6 class 사용하기
<br/>

### props
- 부모 component가 자식 component 에게 주는 값
- 자식 component는 props를 받아오기만 하고 받아온 props를 직접 수정할 수는 없음
- class 문법 사용할때는 자식의 constructor 안에 super(props)를 작성해야 함
<br/>

### state
- 동적 데이터를 다룰 때 사용한다
- class 문법을 사용해 정의 한다
- constructor 안에 설정할 수 있다
- state의 값을 바꾸기 위해서는 this.setState를 사용한다. 
- setState를 쓸 경우 component가 리렌더링 되도록 되어있다
<br/>

### LifeCycle

-componentDidMount
1. componet가 화면에 나타날 때 호출
2. DOM을 사용하는 외부라이브러리 연동
3. componet에서 필요로 하는 데이터 요청 axios, fetch 등 통해 Ajax 요청
4. SetTimeout, setInterval 등
5. DOM에 관련 작업 : 스크롤 설정, 크기 읽어오기
<br/>

-shouldComponentUpdate
1. prop 혹은 state가 변경되었을때 리렌더링을 할지 말지 정하는 메소드
2. component 최적화 작업에 유용
3. 현재 component가 업데이트 되지 않아도 부모가 리렌더링 되면 자식도 render() 함수 호출
4. 불필요한 경우엔 조건에 따라 false 반환하면 reder 함수 호출 하지 않음 (기본값 true)
<br/>


-componemtWillUnmount
1. componet가 DOM에서 사라진 후 실행되는 메소드


