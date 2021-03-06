# 자료구조 9강 트리


## 트리
- 비선형 자료구조 : 하나의 자료 뒤에 여러개의 자료가 존재할 수 있는 것
- 나무 형태의 계층형
- 루트노드로 시작, 나머지 노드들이 간선으로 연결 
- 예) 분류체계, 컴퓨터 폴더구조, 의사결정 구조

### 트리 정의
1) 한개 이상의 노드로 이루어진 유한 집합
2) 루트노드와 서브트리로 구성

### 트리용어
1) 루트노드 : 트리의 최상위 노드
2) 차수 degree : 한 노드가 가지고 있는 서브트리 수 (= 간선의 수)
3) 트리의 차수 : 트리에 있는 노드들의 차수 중에서 최대 차수
4) 단말노드 terminal node/ leaf node : 차수가 0인 노드
5) 비단말노드 nonterminal node : 차수가 1이상인 노드
6) 노드의 레벨 : 루트가 0이고 하위노드로 내려가면서 1씩 증가
7) 부모노드 parent node : 임의의 노드에 연결된 바로 위 레벨의 노드
8) 자식노드 child node : 임의의 노드에 연결된 바로 밑 레벨의 노드들
9) 조상노드 ancestor node : 루트노드에서 임의의 노드까지의 경로를 형성하는 모든 노드들
10) 자손노드 descendent node : 임의의 노드 하위에 연결된 모든 노드들
11) 형제노드 sibling node : 같은 부모 노드를 가진 노드들
12) 포리스트 forest : 루트를 제거한 서브트리들의 집합

### 이진트리 정의
- 모든 노드가 정확하게 두 개의 서브트리를 지님
- 서브트리는 공백이 될 수 있음 
- 왼쪽 서브트리와 오른쪽 서브트리를 분명하게 구별

#### 일반트리와의 차이점
- 노드의 차수가 2로 제한
- 공백트리를 인정
- 왼쪽 서브트리와 오른쪽 서브트리의 순서를 구분

#### 이진트리 종류
1) 포화이진트리 Full Binary Tree : 노드 수가 최대로 꽉 차 있는 이진트리 (높이가 h인 노드의 개수 : 2^(h+1) - 1)
2) 완전이진트리 Complete Binary Tree : 마지막 레벨에 존재하는 노드들이 왼쪽부터 채워져 있는 이진트리
3) 편향이진트리 Skewed Binary Tree : 자식 노드들이 한쪽 방향으로만 치우친 이진 트리

#### 이진트리 표현
##### 순차표현
1) 배열을 이용한 이진트리의 순차표현
  - 포화이진트리의 각 노드에 번호를 붙여서 1차원 배열의 인덱스로 사용
  - 인덱스 0은 실제로 사용하지 않고, 인덱스 1을 항상 루트 노드를 나타냄
  - 노드가 공백인 곳의 숫자는 사용하지 않음 
2) 순차 표현의 장점 : 임의의 노드 i의 부모, 왼쪽 자식, 오르쪽 자식의 인덱스를 쉽게 식별 가능
3) 순차 표현의 단점 : 편향이진트리의 경우 저장공간 낭비 심함

##### 연결 표현(동적 표현)
1) 구조체와 포인터를 사용한 동적메모리할당 eg) node |left|data|right

#### 이진트리 순회

##### 순회 Traversal
- 트리에 있는 노드들의 데이터 값을 일정한 순서로 하나씩 찾아가는 과정
- 모든 노드를 순회하게 되면 순회한 순서에 따라 트리에 있는 데이터를 선셩으로 만들 수 있음
- 트리를  순회할 수 있는 6가지 조합 : LDR | LRD | DLR | DRL | RLD | RDL

1) 중위순회 inorder  traversal LDR
2) 후위순회 postorder traversal LRD
3) 전위순회 preorder traversal DLR


