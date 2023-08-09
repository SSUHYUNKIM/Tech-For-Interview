## [네트워크] OSI 7 계층

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FySyF7%2FbtsqKzWGIvb%2FsLz8CRtfabcFiIjyh3Avc0%2Fimg.png">

### OSI 7 계층이란?
- 네트워크에서 통신이 일어나는 과정을 **7단계**로 나눈 것
- 국제표준화기구 (ISO: International Organization for Standardiztion)에서 네트워크 간의 호환을 위해 만든 **표준 네트워크 모델**
- 통신이 일어나는 과정을 **단계별**로 알 수 있고, 특정한 곳에 이상이 생기면 **그 단계만 수정**할 수 있음.
- 각 계층별로 **모듈화**가 되어있어서 각 계층을 하나로 보는 것이 아니라 융화시켜 **호환성에 용이**하도록 만듦.

### 제 1계층, 물리 계층 (PHYSICAL LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FP3Fww%2FbtsqJq0Gix8%2F5ca3JkViFyAgNaabPcdnJ1%2Fimg.png">

- 실제 장치를 연결하기 위한 **전기적 및 물리적 세부 사항을 정의**한 계층
- 데이터를 **전송**하는 역할만 진행
- 주로 전기적, 기계적, 기능적인 특성을 이용해서 통신 케이블로 데이터를 전송하는 **물리적인 장비**
- 사용되는 통신 단위 : **비트(Bit)**
- **Bit**는 0과 1로 나타내어지는 전기적 On/Off 상태를 의미
- ex) 리피터, 케이블, 허브 등

### 제 2계층, 데이터링크 계층 (DATA-LINK LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcpFoDw%2FbtsqILcKkrA%2FZJjvJMaKDOqbSAxkyL9Km1%2Fimg.png">

- 장치 간 신호를 전달하는 **물리계층을 이용**하여 네트워크 상의 주변 장치들 간의 **데이터를 전송**하는 역할
- 정보의 오류와 흐름을 관리하여 **안전한 통신의 흐름을 관리**
- **Mac 주소**를 통해 통신
- 프레임에 Mac 주소를 부여하고 **에러검출, 재전송, 흐름제어**를 진행
- ex) 브릿지, 스위치 등
 
### 제 3계층, 네트워크 계층 (NETWORK LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FKMglb%2FbtsqJC0HveS%2FDEmmtX2kqhR1lRmoLHW7Q0%2Fimg.png">

- 여러 개의 노드를 거칠 때마다 **경로를 찾아주는 역할**을 하는 계층
- 데이터를 목적지까지 **가장 안전하고 빠르게 전달**하는 기능을 담당
- 라우터를 통해 이동할 경로를 선택하여 **IP 주소를 지정**하고, 해당 경로에 따라 **패킷을 전달**
- **라우팅, 흐름 제어, 오류 제어, 세그먼테이션** 등을 수행
- ex) 라우터, IP
 
### 제 4계층, 전송 계층 (TRANSPORT LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FpwMFq%2FbtsqJT18JyE%2FNgubxSRhjkiMhzE8YC1SI0%2Fimg.png">

- **통신을 활성화**하기 위한 계층
- **TCP와 UDP 프로토콜**을 통해 통신을 활성화
- 포트를 열어두고, 프로그램들이 전송을 할 수 있도록 제공
- 두 지점간의 **신뢰성** 있는 데이터를 주고 받게 해주는 역할
- 신호를 분산하고 다시 합치는 과정을 통해서 **에러와 경로를 제어**
- ex) TCP, UDP

### 제 5계층, 세션 계층 (SESSION LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FM8em6%2FbtsqJq7sFkc%2FwDP6ifU9WxHvmF9MQzhKN1%2Fimg.png">

- 양 끝단의 응용 프로세스가 **통신을 관리하는 방법을 제공**하는 계층
- 데이터가 통신하기 위한 **논리적 연결**을 담당
- TCP/IP 세션 체결, 포트번호를 기반으로 **통신 세션** 구성
- ex) API, Socket

### 제 6계층, 표현 계층 (PRESENTATION LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F4t99i%2FbtsqKEjzD1X%2FqKJi9gtd3KumJKkKkVM3ZK%2Fimg.png">

- **코드 간 번역**을 담당하는 계층
- 데이터 표현에 대한 **독립성**을 제공하고 **암호화**하는 역할을 담당
- **파일 인코딩, 명령어를 포장, 압축, 암호화**
- **전송하는 데이터의 표현방식**을 결정(ex. 데이터변환, 압축, 암호화 등)
- ex) JPEG, MPEG 등 

### 제 7계층, 응용계층 (APPLICATION LAYER)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FwWGrO%2FbtsqJRiZvj5%2FXj2kJweJwsUe4arJWjJTNk%2Fimg.png">

- 응용 프로세스와 직접 관계하여 일반적인 **응용 서비스**를 수행하는 계층
- **최종 목적지**
- **사용자 인터페이스, 전자우편, 데이터베이스 관리** 등의 서비스를 제공
- ex) HTTP, FTP, DNS 등