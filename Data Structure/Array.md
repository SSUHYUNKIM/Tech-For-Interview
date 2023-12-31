## 배열(Array)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbHOFDT%2FbtsrCwkQ8Xm%2FkFBdMpSfFHY2aSqflTkOt1%2Fimg.png">

> **같은 타입의 데이터**를 여러개 **나열**한 선형 자료구조

### 특징
- 연속적인 메모리 공간에 **순차적으로 데이터를 저장**
- 선언된 값은 다시 배열을 선언하지 않으면 **변경할 수 없음**
- **동일한 데이터 유형**을 가짐
- **연속된 메모리에 단일 블록화**하여 데이터를 저장
- **인덱스**를 통해서 배열에 있는 요소에 접근할 수 있음
- **요소(element)**: 배열을 구성하는 **각각의 값**
- **인덱스(index)**: 배열에서의 **위치**를 가리키는 숫자
    - **0**부터 시작
    - 마지막 인덱스는 **배열의 요소의 개수 - 1**

### 시간 복잡도(Time complexity)

|               | **시간 복잡도**   | 
| :-----------------: | :------:  |
| **읽기** | **O(n)** |
| **삽입** | **O(n)** |
| **삭제** | **O(n)** |
| **탐색** | **O(n)** |

### 장점
- **인덱스**를 통해 모든 요소에 **빠르게 접근**
- **기록 밀도가 1**이기 때문에 **공간 낭비가 적음**
- **간단**하고 **사용하기 쉬움**
- **참조**를 위한 **추가적인 메모리가 필요하지 않음**
- **연속적**이므로 **메모리 관리가 편리함**

### 단점
- 배열을 선언 한 후에는 할당 된 정적 메모리 때문에 **크기를 변경할 수 없음**
- **삽입 및 삭제에 비용이 많이 듦**
    - 중간에 특정 요소를 삽입 및 삭제하는 경우 항상 메모리가 순차적으로 이어져 있어야 하기 때문에 삽입 및 삭제된 요소로부터 위에 있는 **모든 요소들을 이동**시켜주어야 함
- 삽입과 삭제가 동적으로 발생하는 상황에서 **적절한 배열의 크기를 미리 결정하는 것이 어렵고**, 이로 인해 **오버플로나 저장공간의 낭비를 초래**할 수 있음
    - 배열의 크기가 대부분 **정적으로 결정**되기 때문

### 배열을 사용하는 경우
- 순차적인 데이터를 저장하며 **값보다는 순서**가 중요할 때
- **다차원 데이**터를 다룰 때
- 어떤 특정 요소를 **빠르게 읽어야** 할 때
- **데이터 사이즈가 자주 바뀌지 않으며 요소가 자주 추가되거나 삭제되지 않을 때**