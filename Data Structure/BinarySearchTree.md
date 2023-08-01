## [자료구조] 이진 탐색 트리(Binary Search Tree)

<img src="https://blog.kakaocdn.net/dn/VyE0K/btsgvW1JKM6/ZZlNokxzgMvayaBG5KzepK/img.png">

### 이진 탐색 트리


|   시간복잡도  | 탐색               | 삽입,삭제               | 
| :-----------------: | :------:  | :------:  |
|이진탐색| O(logN) | 불가능 |
|연결리스트| O(N) | O(1) |

<br>

 - 이진 탐색의 장점과 연결 리스트의 단점을 보완하기 위해 이진 탐색과 연결 리스트를 결합한 자료구조

 - 이진 탐색의 효율적인 탐색 능력을 유지하면서 빈번한 자료 입력과 삭제가 가능

### 이진 탐색 트리의 특징
 - 각 노드에 중복되지 않는 **유일한 키(key)** 존재

 - 루트노드의 왼쪽 서브 트리는 해당 노드의 키보다 **작은 키** 를 갖는 노드

 - 루트노드의 오른쪽 서브 트리는 해당 노드의 키보다 **큰 키** 를 갖는 노드

 - 좌우 서브 트리도 모두 **이진 탐색 트리**

 - 중복된 노드 x

 ### 시간 복잡도

 - 트리의 높이가 h라고 할 때, O(h)

 - 노드의 개수 N이 주어졌을 때 균등 트리 일 경우, O(logN)

 ### worst case

 <img src="https://blog.kakaocdn.net/dn/b9t53I/btsgujcdvBi/5cI6ZckEKL3z0uk2MyGs8k/img.png">

<br>

 - 편향 트리의 시간 복잡도: O(N)