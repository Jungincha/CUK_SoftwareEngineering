# 자료구조 12강 가중치그래프

## 가중치 그래프 Weighted Graph 정의
- 그래프의 간선에 가중치가 부여된 그래프
- 가중치가 부여된 무방향 그래프의 신장트리비용은 신장트리를 구선하는 모든 간선들의 가중치의 합
- 간선에 가중치를 주고, 이들의 최고, 최대 비용을 가지는 경로를 찾아냄으로써 효율적인 네트워크 설계할 수 있음 

## 최소비용 신장트리
- 트리를 구성하는 간선들의 가중치를 합한 것이 최소가 되는 신장 트리
- 크루스칼, 프림, 솔린 알고리즘 (모두 Greedy Method 사용)
