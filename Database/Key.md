## [데이터베이스] Key

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FducEzK%2FbtsqKAnKOvG%2FskMTfwGwWQEf1zyr8aoxa0%2Fimg.png">

### 키(Key)란?

- 데이터베이스에서 검색, 정렬시 **Tuple을 구분할 수 있는 기준**이 되는 Attribute

### Candidate Key (후보키)
- Tuple을 **유일하게 식별**하기 위해 사용하는 속성들의 부분 집합 (기본키로 사용할 수 있는 속성들)
- ex) 학번, 주민등록번호 등
- 2가지 조건 만족
    - **유일성** : Key로 하나의 Tuple을 유일하게 식별할 수 있음
    - **최소성** : 꼭 필요한 속성으로만 구성

### Primary Key (기본키)
- 후보키 중 선택한 **Main Key**
- **Null 값을 가질 수 없음** (개체 무결성의 첫 번째 조건)
- 동일한 값이 **중복될 수 없음** (개체 무결성의 두 번째 조건)
- ex) 학번, 주민등록번호 등

### Alternate Key (대체키)
- 후보키 중 **기본키를 제외**한 나머지 키 = 보조키
- ex) 학번 - 기본키 -> 주민등록번호 - 대체키

### Super Key (슈퍼키)
- **유일성**은 만족하지만, 최소성은 만족하지 못하는 키
- 뭉쳤을 경우 **유일성**이 생김
- 흩어지지만 몇몇 속성들은 독단적으로 유일성 있는 키로 사용할 수 없음
- ex) 학번 + 주민등록번호 + 이름 - 슈퍼키 -> 이름 단독 사용 x

### Foreign Key (외래키)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fcd8H2Y%2FbtsqJBHtDjK%2F3QrLK2gnoKe3NCdRpESQPk%2Fimg.png">

- 다른 릴레이션의 기본키를 **그대로 참조**하는 속성의 집합
- 외래키로 지정시 참조 테이블의 기본키에 없는 값은 입력할 수 없음