### 사용한 알고리즘 자료구조

문제에서 제시한 조건을 구현하는 시뮬레이션 문제이다.  
각 칸의 온도 현황을 저장하는 2차원 리스트 board,  
각 칸의 상하좌우에 벽이 있는지를 저장하는 $R \times C \times4$ 크기의 3차원 리스트 walls를 사용했다.

온풍기를 통해 각 칸에 더해지는 온도의 양은 게임이 진행되어도 동일하게 유지된다.  
따라서 각 칸에 더해지는 양을 미리 계산해서 2차원 배열 heat_amount에 저장하고,  
각 회차에는 이 값을 참고해서 더해주도록 작성했다.

이를 계산하기 위해 heat(hr, hc, d, heat_amount) 메서드를 사용했다.  
이는 (hr, hc) 위치에 d 방향을 바라보고 있는 온풍기가 있을 때,  
이 온풍기로부터 추가되는 온도의 양을 heat_amount의 각 칸에 더해주는 메서드이다.  
is_valid(r, c, d)는 (r,c)에서 d 방향으로의 이동이 가능한지를 확인하는 메서드이다.  
둘 사이에 벽이 있지 않은지, 칸의 경계를 초과하진 않는지를 검증한다.

spread는 열을 확산시키는 메서드이다.  
각 칸에 더해지거나 빠지는 양을 spread_board에 계산해두고,
모든 칸의 확산을 계산한 후에 board에 그 결과를 반영시킨다.
