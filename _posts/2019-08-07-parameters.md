---
layout : post
title : "JavaScript -parameter"
comments: true
---

### JavaScript parameter 정리
<br/>
<br/>
#### arguments
- arguments 객체는 모든 함수 내에서 이용가능한 지역 변수
- 인덱스로 접근 가능, 각 인수를 설정하거나 재할당 가능
- Array 아님, length 제외하고 속성 없음, array로 반환 불가능

```
function myConcat(separator) {
  var args = Array.prototype.slice.call(arguments, 1);
  return args.join(separator);
}

// "red, orange, blue" 반환
myConcat(", ", "red", "orange", "blue");

// "elephant; giraffe; lion; cheetah" 반환
myConcat("; ", "elephant", "giraffe", "lion", "cheetah");

// "sage. basil. oregano. pepper. parsley" 반환
myConcat(". ", "sage", "basil", "oregano", "pepper", "parsley");
```

<br/>
<br/>


#### Rest parameters
- 정해지지 않은 수의 인수를 배열로 나타냄
- 마지막 파라미터 앞에 ...을 붙여 나머지 인수를 배열로 대체
- 마지막 파라미터만 사용 가능
- Array 인스턴스로 메서드 적용 가능

```
function myFun(a, b, ...manyMoreArgs) {
  console.log("a", a); 
  console.log("b", b);
  console.log("manyMoreArgs", manyMoreArgs); 
}

myFun("one", "two", "three", "four", "five", "six");

// a, one
// b, two
// manyMoreArgs, [three, four, five, six]
```
<br/>
<br/>
#### Default parameters
- 매개변서에 기본값 넣기 가능 
- 문자열 / 숫자 / 객체 등 어떤 타입도 가능

```
function getRoute(des, dep ='ICN'){
  return des +":" dep;
}
getRoute('PEK') // 'PEK:ICN'
```


