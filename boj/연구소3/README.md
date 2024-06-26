### 사용한 알고리즘/자료구조

문제에서 제시한 조건을 구현하는 문제이다.  
활성 바이러스의 가능한 조합을 순회하면서 최소 시간을 탐색했다.  
각 조합에 대해 bfs를 수행하면서 각 초에서 남은 빈칸의 개수를 확인하고, 전파가 완료되었으면 해당 초를 반환하도록 했다.

처음에는 바이러스가 다 확산되었는지 확인하기 위해 아래의 함수를 사용했다.

```python
def is_fully_spreaded(board):
    return sum([line.count(BLANK) for line in board]) == 0
```

이 함수를 통해 확인하면 매초마다 $O(n^2)$의 연산을 수행하는 셈이 된다.  
이 때문에 처음에는 시간초과가 발생했다.

이를 수정하여 처음에만 `sum([line.count(BLANK) for line in board]) == 0`으로 전체 빈칸의 개수를 세고,
이후에 빈칸에 바이러스가 확산되면 하나씩 감소시키도록 했다.
