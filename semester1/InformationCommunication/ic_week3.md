# 정보통신개론 3주차 전송기술과 교환기술(1)

## 전송방식의 유형

- 직렬전송
- 병렬전송
-----------------
- 단방향
- 양방향
  - 반이중 eg 무전기
  - 전이중 eg USB
-----------------------
- 동기식 전송 synchronous 약속한 패턴을 이용하여 데이터의 송수신 타이밍을 일치시킴
- 비동기식 전송 asynchronous

## 아날로그와 디지털 전송의 특징
- 아날로그 신호 : 부드러운 곡선을 그리며 연속적으로 변화하는 신호
- 디지털 신호 :   0과 1 두 비트를 이용해 모든 정보들을 나타내는 신호
------------------------------------------------
- 아날로그 정보 => 디지털 신호 (ADC) : 표본화, 양자화, 부호화 기법(PCM)
- 디지털 정보 => 디지털 신호
## 다중화 전송방식
- 정보의 다중화 Multiplexing
- 하나의 전송회선에 여러 개의 전송신호를 모아서 함께 전송하는 것
- 적은 비용으로 많은 데이터를 전송하기 위해 사용
- 송신측 : 여러 장치 신호들을 통합하여 하나의 전송회선을 통해 전송
- 수신측 : 통합된 신호를 여러 개의 신호로 각각 분리 (역다중화)
----------------------------------------
- FDM 주파수 분할 다중화 방식
  - 아날로그 전송에서 주로 사용
- 주파수 분할 역다중화 Frequency Division Demultiplexing 
  - 주파수 대역통과 필터를 이용하여 신호를 분리 

- TDM 시분할 다중화 방식
- 시분할 역다중화 방식

- CDM 
