### 사용한 알고리즘/자료구조

키를 회전 및 이동시켜가며 lock을 풀 수 있는지 확인하는 문제이다.  
이차원 list를 이용한 구현 문제이다.

먼저 lock을 가운데 위치한 $(3*N)\times(3*N)$ 크기의 2차원 리스트 board를 만든다.  
이 떄 키의 가장 왼쪽 위쪽의 위치를 (1, 1) ~ (2*N-1, 2*N-1)로 이동시켜가며,
각 위치에서의 원래의 키, 90도 회전 키, 180도 회전 키, 270도 회전 키를 모두 확인해보는 식으로 구현했다.
