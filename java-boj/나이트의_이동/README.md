# 백준 알고리즘 7562번: 나이트의 이동(Java)

[https://www.acmicpc.net/problem/7562](https://www.acmicpc.net/problem/7562)

## 로직

출발점과 도착점이 주어졌을 때, 최소 이동 횟수(거리)를 구하는 문제이다.  
bfs(너비우선탐색)를 이용해서 풀이했다.

dist[][] 배열에 시작점으로부터 해당점까지의 최단거리를 기록한다.  
한번 탐색이 이루어질 때마다 이전 점에 비해 하나씩 더해서 기록하는 방식을 사용했다.  
목표점에 도달할 경우 탐색을 멈추고 답을 출력한다.
