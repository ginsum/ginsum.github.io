---
layout : post
title : "자료구조 - Stack 스택, Queue 큐, Linked List "
comments: true
---

## STACK 스택
![스택구조](<http://ginsum.github.io/images/2019-09-18-01.png>)
### 스택의 개념
한 쪽 끝에서만 자료를 넣고 뺄수 있는 선형구조(Last In First Out) 형식의 자료 구조<br/>
제한적으로 접근할 수 있는 나열 구조이며 접근 방법은 언제나 목록 끝에서만 일어난다.
<br/>
### 스택의 연산
스택은 가장 최근에 추가한 항목이 가장 먼저 제거된다.자료를 넣는 것은 Push, 꺼내는 것은 Pop 이라고 한다. 
- top() : 스택의 가장 윗 데이터를 넘겨준다.
- pop() : 스택의 가장 윗 데이터 값을 넘겨주고 해당 데이터를 삭제한다.
- push() : 스택의 가장 윗 데이터로 top이 가르키는 자리 위에 top = top +1 메모리를 생성, x 데이터를 넣는다.
- empty() : 스택이 비었다면 참, 아니면 거짓을 반환한다.<br/>

### 스택의 사용 사례
- 재귀 알고리즘
- 웹 브라우저 방문기록
- 실행취소 (undo)
- 역순 문자열 만들기
<br/>

### 스택 구현(pseudo code)
- 사용자는 임의의 사이즈를 가진 스택을 생성할 수 있다.
스택을 생성시 필요한 요소는 최대 사이즈, 스택 내 데이터의 갯수, 들어갈 데이터
1. 새로운 객체를 생성한다.
2. 최대 사이즈를 요소로 추가한다
3. 현재 스택내 데이터 갯수를 표시한다(마지막 데이터 위치 표시를 위해)
4. 들어가 있는 데이터를 추가한다.

- 사용자는 데이터 한개를 추가할 수 있다.
1. 현재 스택의 데이터가 최대 사이즈를 넘지 않는지 확인한다
2. 마지막 스택 위치에 데이터를 추가한다
3. 갯수 정보를 한개 늘린다

- 사용자는 데이터 한개를 삭제할 수 있다.
1. 현재 스택의데이터가 비어있는지 확인한다.
2. 갯수 정보를 한개 줄인다.
3. 마지막 스택 위치에 데이터를 비운다.

<br/>
<br/>
## QUEUE 큐

![큐구조](<http://ginsum.github.io/images/2019-09-18-02.png>)
### 큐의 개념
먼저 집어넣은 데이터가 먼저 나오는 FIFO(First In First Out)구조로 저장하는 자료구조<br/>
마지막에 넣은 데이터가 먼저 나오는 스택과 반대개념
<br/>
### 큐의 연산
- enQueue: 큐안에 데이터를 집어 넣는 연산.
- deQueue: 큐 안의 데이터를 끄집어내는 연산.
- peak: 큐에서 가장 위에 있는 항목 반환.
- Empty: 큐가 비어있을 때 true를 반환.
<br/>

### 큐의 사용 사례
- 프린터의 출력 처리
- 윈도 시스템의 메시지 처리기
- 프로세스 관리 등
<br/>

### 큐 구현(pseudo code)
- 사용자는 임의의 사이즈를 가진 큐을 생성할 수 있다.
큐을 생성시 필요한 요소는 최대 사이즈, 스택 내 데이터의 갯수, 들어갈 데이터
1. 새로운 객체를 생성한다.
2. 최대 사이즈를 요소로 추가한다
3. 현재 큐내 데이터 갯수를 표시한다
4. 들어가 있는 데이터를 추가한다.

- 사용자는 데이터 한개를 tail에 추가할 수 있다.
1. 현재 큐의 데이터가 최대 사이즈를 넘지 않는지 확인한다
2. 큐의 마지막 위치에 데이터를 추가한다
3. 갯수 정보를 한개 늘린다

- 사용자는 front의 데이터 한개를 삭제할 수 있다.
1. 현재 큐의 데이터가 비어있는지 확인한다. 
2. 갯수 정보를 한개 줄인다.
3. 첫번째 위치에 데이터를 지운다.


<br/>
<br/>
## Linked List
<br/>
<br/>
![Linked List 구조](<http://ginsum.github.io/images/2019-09-18-03.png>)
### Linked List의 개념
엘리먼트와 엘리먼트 사이의 연결로 리스트 구현<br/>
리스트는 노드(엘리먼트)들의 모임이며 노드는 최소 두가지 정보를 가지고 있는데 그것은 노드의 값과 다음 노드이다. 다음노드를 알고 있기 때문에 하나의 연결된 값의 모임을 만들수 있다.
<br/>
### Linked List의 연산
- .append() : 맨 뒤에 노드 추가
- .first() : 맨 앞의 노드 검색
- .next() : 다음 노드 검색
- .delete() : 현재 노드 삭제
<br/>

### Linked List 구현(pseudo code)
- 사용자는 Linked list을 생성할 수 있다.
1. 새로운 객체를 생성한다.
2. 데이터를 요소로 추가
3. 데이터 갯수를 표시.

- 사용자는 데이터 한개를 맨 뒤에 추가할 수 있다.
1. 새로운 노드를 생성
2. 새 노드를 마지막 노드의 뒤에 위치(next 사용)
3. 새 노드를 마지막 노드로 설정
4. 데이터 갯수를 증가시킴




