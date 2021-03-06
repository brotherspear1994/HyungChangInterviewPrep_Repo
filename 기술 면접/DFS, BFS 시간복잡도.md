#  DFS와 BFS 알고리즘의 시간복잡도



## DFS 시간 복잡도

---

DFS 하나에 for loop을 V 만큼 돌기 때문에, O(V) 시간이 필요함.

정점을 방문할 때 마다 DFS를 부르는데, V개의 정점을 모두 방문하므로

DFS의 전체 시간복잡도 = V * O(V) = O(V^2)

---

모든 정점을 방문해야 하므로 dfs함수는 총 V번 호출된다.
그런데 그 함수 내부의 for문에 의해서 각각은 O(V)의 시간복잡도를 가지므로
전체를 모두 1번씩 탐색하는 경우 V x O(V) = O(V^2)의 시간복잡도를 가진다.

---

> 내 결론: 모든 정점을 방문해야 하므로 V개의 정점만큼 있을 때 총 V 번이 호출된다. 다시 한 노드(정점)을 기준으로 for문을 돌리며 모든 정점을 탐색해야 하므로 전체 시간 복잡도는 V 곱하기 O(V)가 돼서 O(V*2)이 된다.



## BFS 시간 복잡도

너비 우선 탐색의 시간 복잡도는 깊이 우선 탐색과 다를 것이 없습니다. 모든 정점을 한 번씩 방문하며, 정점을 방문할 때마다 인접한 모든 간선을 검사하기 때문이지요. 따라서, 인접 리스트로 구현된 경우에는 O(|V|+|E|), 인접 행렬로 구현했을 경우 O(|V|^2)의 시간 복잡도를 갖게 됩니다.

* 참고) E는 지수 시간(상수)를 의미한다.

