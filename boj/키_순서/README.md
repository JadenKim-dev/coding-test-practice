분류: 플루이드-와샬

두 학생 쌍들의 키 비교 결과가 주어진 상태에서, 자신이 몇번째로 큰지 알 수 있는 학생의 수를 구하는 문제이다.

두 학생 키의 비교 정보를 edge로 생각하고, 플루이드 와샬 알고리즘을 적용하여 문제를 풀 수 있다.  
각각의 edge는 키가 크다는 정보인지, 작다는 정보인지, 본인에 대한 것인지, 알려지지 않은 것인지에 대한 정보를 담게 저장했다.  
`(SMALL = -1; LARGE = 1; UNKNOWN = 0; SELF = 2)`

dist[a][k] == dist[k][b] 이고, 두 개가 동일한 정보를 담고 있다면 이를 dist[a][b]에 업데이트 해주면 된다.  
(a가 b보다 크고, b가 c보다 크면 -> a가 c보다 큼)  
(a가 b보다 작고, b가 c보다 작으면 -> a가 c보다 작음)
