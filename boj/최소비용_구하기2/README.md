출발지에서 도착지로 가는 최단 거리와 그 경로를 구하는 문제이다.

heapq를 사용해서 최단 거리를 구했고,  
prev 리스트에는 해당 지점까지 오는데 최단 거리가 되는 직전의 도시를 저장했다.

마지막에 prev를 통해 거슬러 올라가면서 최단 거리가 되는 경로를 구할 수 있다.

이 문제에서는 도착지점까지 갈 수 있는 경로가 여러 개 존재할 수 있는데,  
그 중에서 도시의 index number가 작은 경로가 우선순위를 가진다.  
따라서 이를 반영해주기 위해 dijkstra 메서드에 최단 거리를 갱신할 때  
if cost < distance[x] or (cost == distance[x] and dest < prev[x]) 조건을 넣어서  
이전의 비용과 동일한 경로이더라도 도시의 인덱스가 더 작다면 prev 리스트를 갱신하도록 작성했다.
