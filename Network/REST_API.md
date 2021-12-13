# REST_API
  > Representational State Transfer - Application Programming Interface
  - HTTP에서 필요한 자원에 접근할 때 웹의 장점을 최대한 활용하기 위한 아키텍쳐
  - 컴퓨터 상호간에 상호 운용성을 제공하는 방법 중 하나

## WEB

- Q : 어떻게 인터넷에서 정보를 공유할 것인가?
- A : 정보들을 하이퍼 텍스트로 연결한다.
  - 표현형식 : HTML
  - 식별자 : URI
  - 전송 방법 : HTTP

## REST란?

- 분산 하이퍼미디어 시스템(예: 웹)을 위한 아키텍쳐 스타일
  - 아키텍쳐 스타일 : 제약조건의 집합

### REST를 구성하는 스타일
  - client-server
  - stateless
  - cache
  - uniform interface
    - 
  - layered system
  - code-on-demand (optional) : 서버에서 코드를 클라이언트한테 보내서 실행이 가능해야함 (javascript)

## 구성요소

1. HTTP Method
  - GET : 조회
  - POST : 데이터 생성
  - PUT : 데이터 전체 수정
  - PATCH : 데이터 일부 수정
  - DELETE : 데이터 삭제

2. URL : 데이터 접근
 
3. Representation : 자원의 표현
 
## Resource

- Resource

![Resource](../img/REST_API_1.png)


- Request

![Request](../img/REST_API_2.png)

---

- REST Client 활용