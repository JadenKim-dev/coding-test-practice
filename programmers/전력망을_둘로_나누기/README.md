https://programmers.co.kr/learn/courses/30/lessons/86971

문제에서도 설명하고 있듯이, 그래프(트리) 자료구조를 사용하면 된다.  
전선으로 주어진 wires를 각각의 간선으로 간주한다.  
wires의 각각의 전선을 제외해보면서 각 경우에 2개의 싸이클이 만들어지는지, 각 싸이클에 포함된 노드의 개수가 몇 개인지 확인하면 된다.  
이때 find 연산에는 경로압축기법을 사용하여 시간복잡도를 개선시켰다.
