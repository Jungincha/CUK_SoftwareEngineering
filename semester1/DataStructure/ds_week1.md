# 자료구조와 알고리즘

프로그램과 소프트웨어의 차이점?


## 자료구조의 개념
1) 프로그램 <br>
A computer program is a collection of instructions that performs a specific task when executed by a computer <br>
컴퓨터에서 특정 작업을 수행하는 명령어들의 집합
2) 소프트웨어 <br>
A collection of data or computer instructions <br>
목적을 수행하기 위한 하나 또는 다수의 컴퓨터 프로그램으로 구성<br>
프로그램을 비롯한 개발과정의 산출물들을 포함함

## 자료구조 정의
*문제해결을 위해 데이터 값들을 연산\(알고리즘)들이 효율적으로 접근하여 처리할 수 있도록 체계적으로 조직하여 표현하는 것*
=> 추상데이터타입의 정의 + 추상데이터타입의 구현 
- 데이터란 무엇?
- 데이터는 어떤 방식으로 컴퓨터에 표현되는가?
- 데이터를 어떤 방식으로 처리하는 것이 보다 효율적?

## 자료구조의 분류
- 광의의 자료구조
- 협의의 자료구조
  - 단순 자료구조
  - 선형 자료구조
  - 비선형 자료구조

## 추상자료형\(ADT) - Abstract Data Type
자료구조를 구조화하기 위한 방법 = 데이터값의 집합 + 데이터에 적용되는 오퍼레이션의 집합
### 추상화란?
- 구체적인 대상에서 공통적인 측면이나 중요한 성질을 뽑아내어 표현하는 과정
- 단순환, 문제의 복잡성 제어
- Data Abstraction + Procedural Abstraction
### 인터페이스
프로그램과 데이터를 분리하기 위해 operator가 인터페이스가 됨
### 객체지향의 언어
C++, Java : Class 지원

## 알고리즘
1) 좋은 소프트웨어란?
  - 적은 자원의 사용
  - 빠른 실행 시간
  - 적은 비용으로 개발/유지보수 가능
2) 알고리즘 정의
  - 특정 문제를 해결하지 위해 기술한 일련의 명령문, 절차
  - 컴퓨터에 의한 자료처리 과정을 단계별로 기술한 것

### 좋은 알고리즘의 요건
- 완전성과 명확성
- 입력과 출력
- 유한성\(무한루프X)
- 효과성

## 복잡도
### Big Omega
- [빅오표기법 설명](https://www.youtube.com/watch?v=6Iq5iMCVsXA&ab_channel=%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%EB%8C%80%ED%95%9C%EB%AF%BC%EA%B5%AD)
- 연산의 횟수를 대략적\(점근적)으로 표현
- Mathematical notation that describes algorithm efficiency
- Time & space complexity
- Describes the growth rate of algorithms
- Drop constants 상수를 과감히 버린다 2n => n
- O(1)
- O(n)
- O(n²)
- O(nm)
- O(n³)
- O(2ⁿ) 피보나치 수열
- O(mⁿ)
- O(log n) binary search 이진검색
- O(Sqrt(n))

















