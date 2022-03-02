# 데이터베이스 개념

[Fundamentals of Database System](https://iran-lms.com/images/images/Books/PDF/Fundamentals-of-Database-Systems-Pearson-2015-Ramez-Elmasri-Shamkant-B.-Navathe.pdf)

## 데이터와 정보
- Data : facts, symbols
- Information : data that are processed to be useful
- Knowledge : application of data information \(pattern)
- Wisdom: appreciation of 'why'

데이터: 현실세계를 관찰하거나 측정하여 수집한 사실

### 데이터의 특징
- 객곽전 사실
- 다른 데이터와의 상호관계 속에서 더 큰 가치 가짐

### 데이터의 유형
- 범주형 데이터
- 수치형 데이터

### 정보
유용하게 사용할 수 있도록 데이터를 처리한 것\(Relationship)

### 지식
- 데이터와 정보로부터 도출한 패턴
- 판단과 예측이 가능

### 지혜
근본적인 원리에 대한 이해  

## 데이터베이스 
A collection of related data 서로 관련 있는 데이터들의 모임

### 데이터베이스 Why?
1) 데이터를 중복시키지 않는다 \(중복성 x, 일관성)
2) 데이터의 독립성 증진
<br>
=> DBMS\(Database Management System) 데이터베이스 관리체계 필요성 ↑

### 정보시스템 관점에서 정의
- 통합된 데이터 Integrated
- 저장된 데이터 Stored
- 운영 데이터 Operational
- 공용 데이터 Shared

### 데이터베이스 특성
- 실시간 접근성
- 동시공용
- 계속적인 변화\(OLTP - Online Transaction Processing)
- 내용에 의한 참조\(ex: 키워드에 의한 검색) <-> 주소에 의한 참조\(ex: C언어의 변수 접근)

### 데이터베이스 구축 목적
- 서로 다른 형태의 데이터의 통합화
- 중복된 데이터의 일관성 유지
- 데이터의 정확성을 보장하는 무결성 유지\(데이터베이스에 저장된 데이터 값과 그것이 표현하는 현실 세계의 실제 값이 일치하는 정확성)
<br>ex) 은행 잔고가 0밑으로 내려가서는 안된다
- 데이터 중복의 최소화
- 업무상 데이터의 공유
- 데이터의 보안성 달성
- 데이터의 논리적, 물리적 독립성
- 데이터의 표준화 달성

## 데이터베이스 구성요소
### 데이터베이스 스키마
데이터베이스의 논리적 정의, 데이터 구조와 제약조건에 대한 명세\(Specification)
#### 스키마의 구성요소
- 개체 entity 
- 속성 attribute
- 관계 relationship
- 제약조건 constraint
<br>
3단계 데이터베이스 구조 <br>
![alt text](https://blog.kakaocdn.net/dn/bvqMrR/btqN02bgEod/pkZLTK4VDB99FQrFckK2X1/img.png)

#### 데이터 독립성
- 논리적 데이터 독립성 
- 물리적 데이터 독립성

### 데이터베이스 사용자
- 일반사용자
- 응용프로그래머
- 데이터베이스 관리자 DBA

#### DBA 역할
- 데이터베이스 설계와 운영
- 데이터 표준 관리 및 행정 불편 해소
- 시스템 감시 및 성는 분석

### 데이터베이스 언어
데이터베이스를 정의하고 접근하기 위한 목적으로 만들어진 언어
- 데이터 정의어 ex) 테이블 생성, 변경
- 데이터 조작어 ex) 데이터의 검색, 삽입, 삭제, 변경
- 데이터 제어어 ex) 데이터보안, 무결성, 데이터회복, 병행수행

















