---
layout : post
title : "자료구조 - Graph, Tree, Binary Search Tree, Hash Table "
comments: true
---

## Graph

![Graph구조](<http://ginsum.github.io/images/2019-09-18-04.png>)
### Graph의 개념
노드와 간선을 하나로 모아놓은 자료 구조. 일반적인 자료 구조로 연결되어 있는 객체 간의 관계를 표현하는 자료 구조이다.<br/>
ex) 지도, 지하철 노선도의 최단 경로, 도로
<br/>
### Graph의 종류
무방향 그래프, 방향 그래프, 가중치 그래프, 부분 그래프
<br/>
### Graph의 표현
1. 인접 행렬 : 이차원 배열  
2. 인접 리스트 : 연결 리스트 통한 사용
<br/>

<br/>
<br/>
## Tree

![Tree구조](<http://ginsum.github.io/images/2019-09-18-05.png>)
### Tree의 개념
노드로 이루어져 있는 자료 구조
1. 트리는 하나의 루트 노드를 갖는다
2. 루트 노드는 0개 이상의 자식 노드를 갖는다
3. 자식 노드 또한 0개 이상 자식 노드 가진다
<br/>
### Tree의 특징
1. 트리는 그래프의 한 종류이다.
2. 사이클이 없는 하나의 연결그래프
3. 또는 DAG(Directed Acyclic Graph 방향성이 있는 비순환 그래프)의 한 종류
<br/>
### Tree의 종류
1. 이진트리 : 각 노드가 최대 두개의 자식을 갖는 트리
2. 이진탐색트리 : 모든 노드가 트정 순서를 따르는 속성을 갖는 트리
3. 균형트리 : O{logN}시간에 insert와 find를 할 수 있을 정도로 균형이 잘 잡혀있는 경우
<br/>
### Tree 구현
1. 인접배열 이용 : 1차원 배열에 자신의 부모 노드만 저장하는 방법 / 이진 트리일 경우 2차원 배열에 자식노드를 저장하는 방법
2. 인접 리스트 이용 : 가중치가 없는 트리일 경우 / 가중치가 없는 트리일 경우

<br/>
<br/>
## Binary Search Tree

![Binary Search Tree 구조](<http://ginsum.github.io/images/2019-09-18-06.png>)
### Binary Search Tree의 개념
이진탐색(binary search)와 연결리스트(linked list)를 결합한 자료구조의 종류. 이진탐색의 효율적인 탐색 능력을 유지하면서도 빈번한 자료 입력과 삭제가 가능 
<br/>
### Binary Search Tree의 속성
1. 각 노드의 왼쪽에는 해당 노드값보다 작은 값을 지닌 노드들로 이루어짐
2. 각 노드의 오른쪽에는 해당 노드의 값보다 큰 값을 지닌 노드로 이루어짐
3. 중복된 노드가 없음
4. 왼쪽 서브트리, 오른쪽 서브트리 또한 이진탐색트리
<br/>


### Binary Search Tree의 연산
핵심연산은 검색(retreive), 삽입(insert), 삭제(delete) 세가지. 이밖에 이진탐색트리 생성(create), 이진탐색트리 삭제(destroy), 비어있는지 확인(isEmpty), 트리순회(tree traverse)등의 연산이 있음.
<br/>
## Hash Table
![Hash Table 구조](<http://ginsum.github.io/images/2019-09-18-07.png>)
### Hash Table의 개념
hash는 내부적으로 배열 사용하여 데이터 저장하여 빠른 검색 속도를 가짐. 특별한 알고리즘을 이용하여 저장할 데이터와 연관된 고유 숫자를 만들어 낸 뒤 인덱스로 사용함
<br/>
### Hash Function
고유 인덱스 값을 설정하는 알고리즘을 hash method 혹은 hash function 이라고 하며, 이 메소드에 의해 반환된 데이터의 고유 숫자값은 hashcode라고함. 보통 좋은 hash function은 hash table 성능 향상에 필수적
<br/>
### 충돌처리 방식
1. separate chaining 방식
linked list를 이용하는 방식. 각 인텍스에 데이터를 저장하는 linked list에 대한 포인터를 가지는 방식
만약 동인 인덱스로 충돌 발생하면 그 인덱스가 가르키고 있는 linked list 에 노드를 추가하여 값을 추가한다.
2. Open addressing 방식
인덱스 충돌처리에 대해 hash table 빈공간을 사용하는 방식으로 seperate chaining 방식에 비해 메모리 덜 사용함.
linear Probing / Quadratic probing / Double hashing probing 방식이 있다.