---
layout : post
title : "Node.js -require / exports /EventEmitter / Stream"
comments: true
---

### Node.js 란
V8엔진으로 만들어진 자바스크립트 런타임

- V8 complies Javascript directly to native machine code
- 런타임 -프로그램이 구동되고 있는 환
- 이벤트 기반 및 논브로킹 I/O 모델
- 논블로킹 - 다음 함수의 실행이 현재 함수의 종료를 기다리지 않는다

<br/>
<br/>
### require / exports

- require()는 module.exports를 리턴한다.
- exports는 module.exports를 refer하고 있으며, shortcut에 불과하다
- require 함수로 모듈을 불러온다
- 한번 로딩(require)된 모듈은 require.cache라는 객체에 캐싱됩니다

<br/>
<br/>

### EventEmitter

- 이벤트를 내보내는 모든 객체는 EventEmiter 클래스의 인스턴스이다
- 이 객체는 하나 이상의 함수를 이름을 넣어 이벤트로 사용할 수 있는 eventEmiter.on() 함수를 사용할 수 있다
- eventEmitter.emit()는 eventEmiter.on()으로 등록한 이벤트를 호출한다

<br/>
<br/>

### Stream 방식

- 파일안의 데이터를 덩어리(chunk)로 잘게 쪼개 데이터의 stream 에 얹어서 읽어들이는 방식
- 메로리나 속도 측면에서 효율적
- Buffer로 수집됨
- createReadStream / createWriteStream



