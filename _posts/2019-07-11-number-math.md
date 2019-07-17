---
layout : post
title : "JavaScript - Number/ Math"
comments: true
---

### JavaScript Number/ Math Mathods 정리
<br/>
<br/>
#### number.isInteger(value)
- arguments : 정수인지 아닌지 여부를 검사할 값
- return value : 정수를 판단한 결과 (Boolean)

```
Number.isInteger(0);         // true
Number.isInteger(1);         // true
Number.isInteger(-100000);   // true

Number.isInteger(0.1);       // false
Number.isInteger(Math.PI);   // false

Number.isInteger(Infinity);  // false
Number.isInteger(-Infinity); // false
Number.isInteger("10");      // false
Number.isInteger(true);      // false
Number.isInteger(false);     // false
Number.isInteger([1]);       // false
```
<br/>
<br/>
#### parseInt(value) /parseFloat(value)
- arguments : 형 변환 하기 위해 파싱될 값
- return value : 정수 도는 소숫점 숫자

```
parseInt("15");     // 15
parseInt("15.123"); // 15
parseInt("15*3");   // 15
parseInt("-15");    // -15
parseInt("Hello")   // NaN
parseFloat("3.14"); // 3.14
```
<br/>
<br/>
#### parseInt(value, radix)
- parseInt는 진법으로 변환할 때도 사용
- radix가 필요없는 10진법 변환일 경우에도 명시적으로 10을 넣어주는 것을 권장

```
parseInt(" 0xF", 16); // 15
parseInt(" F", 16);   // 15
parseInt("17", 8);    // 15
parseInt(15.99, 10);  // 15
```
<br/>
<br/>
#### num.toFixed([digits])
- arguments : 소숫점 뒤에 나타낼 자릿수 (optional, 기본값은 0)
- return value : 숫자를 나타내는 문자열

```
var numObj = 12345.6789;

numObj.toFixed();   // '12346': 반올림하며, 소수 부분을 남기지 않습니다.
numObj.toFixed(1);  // '12345.7': 반올림합니다.
numObj.toFixed(6);  // '12345.678900': 빈 공간을 0으로 채웁니다.
```

