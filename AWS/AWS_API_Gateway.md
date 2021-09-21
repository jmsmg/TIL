# AWS API Gateway
> 자신만에 고유한 주소가 있음

- 람다와 연결(서버리스 플랫폼)

## 구조 
- 웹을 관리할때, 중간에 Gateway를 통해 쉽게 관리함

![구조](../img/AWS_Gateway_1.png)

## 종류

- HTTP API 
  - 스테이지 / URL 호출 / 주소
  - API Gateway > 경로 or 통합 > 생성 > 링크 지정, 통합 생성 및 지정
    > 해당 주소로 들어오면 API서버로 연결 시켜줌

![경로](../img/AWS_Gateway_2.png)


- REST API
- Web Socket API

## 가격
- HTTP가 제일 저렴

---

## 공부해볼만한 주제
- 권한부여

- CORS
  > Cross-Origin Resource
  - 다른 도메인 API를 허용하지않을 수 있음(??)

- 배포
  - 자동배포 기능이 있어서 크게 필요 없음

- 모니터링