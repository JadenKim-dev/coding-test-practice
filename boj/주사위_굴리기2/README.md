### 사용한 알고리즘/자료구조

문제에서 제시한 조건을 구현하는 시뮬레이션 문제이다.

먼저 각 칸에 도착했을 경우 얻게 되는 점수를 계산해서 scores 이차원 리스트에 저장했다.  
각 칸에서 얻게 되는 점수는 게임이 진행되어도 변하지 않기 때문에, 미리 구해서 저장해두는 게 효율적이다.  
bfs를 이용해서 연속해서 이동할 수 있는 칸을 구했다.

주사위를 이동시키는 과정에서는 주사위의 위치 (r, c), 주사위의 방향 d,  
주사위의 동쪽, 북쪽, 바닥의 숫자를 저장하는 east, south, bottom 변수를 사용했다.  
남쪽 = 7-북쪽, 서쪽 = 7-동쪽, 위쪽 = 7-바닥 으로 구할 수 있기 때문에 3개의 변수만 사용했다.
