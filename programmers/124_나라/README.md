처음에는 빈 문자열("")에서 시작해서, 하나씩 이어 붙이는 식으로 했는데(result = code_dict[n % 3]+result) 시간 초과가 발생했다.  
이를 해결하기 위해 배열에 append한 후 나중에 join을 통해 문자열로 통합하는 방식을 택했다.
