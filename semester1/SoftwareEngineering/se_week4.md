# 소프트웨어공학 4강 소프트웨어 설계 및 설계 방법론(1)

### 소프트웨어 설계 활동
프로그램을 구현하기 전에 소프트웨어를 구성하는 요소와 구조를 저의해 구현의 기반을 만드는 활동
- 아키텍처 설계 : 구조설계/ DB 설계/ 인터페이스 설계 => 전반적인 구조
- 상세설계 : 컴포넌트 설계/ 자료구조 설계/ 알고리즘 설계 

### 소프트웨어 설계 방법의 유형
- 구조적 소프트웨어 설계 : Function중심 설계, Function과 Data가 분리되어 있음
- 객체지향 소프트웨어 설계 

### 소프트웨어 아키텍쳐 설계 활동
상위수준에서 소프트웨어 구성 요소들 간의 관계로 구성된 전체적인 구조를 설계하는 활동

### 소프트웨어 아키텍처 설계 활동
상위 수준에서 소프트웨어 구성요소들 간의 관계로 구성된 전체적인 구조를 설계하는 활동

### 소프트웨어 상세 설계 활동
아키텍처 설계에서 도출된 소프트웨어 구성요소(컴포넌트, 모듈)들의 내부 데이터와 알고리즘 등을 설계하는 활동

## 구조적 소프트웨어 설계
어떠한 절차를 거쳐서 작업을 수행하는가, 어떠한 입출력 자료를 생성하는가에 초점을 두며, 프로세스 지향 설계라고도 부름
- Highly Cohesion 높은 응집력
- Loosley Coupling 낮은 결합도

### 구조적 소프트웨어 아키텍쳐 설계 : Task Model (동적인 구조)
소프트웨어 요구사항 분석 모델을 실현하기 위해 소프트웨어 아키텍처의 동적인 관점에서 태스크 혹은 쓰레드 구조를 기술하는 기법

### 구조적 소프트웨어 아키텍쳐 설계 Module Structure (정적인 구조)
태스크 모델을 기반으로 소프트웨어 아키텍처의 정적인 관점에서 모듈의 전반적인 구조를 설계하는 기법

### 구조적 소프트웨어 상세 설계
- Structure Chart : 태스크와 모듈에 할당된 데이터 흐름도의 흐로세스들을 구현하기 위한 제어구조를 표현하는 하향식 기법