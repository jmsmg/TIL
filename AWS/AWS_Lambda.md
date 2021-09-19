# AWS Lambda
> 0.1초 단위로 빌려서 코드만 돌리고 바로 반납되는 서비스

## 사전 지식
- cloud console에서 람다 생성
- 컴퓨터 한대 용어
  - EC2 : 인스턴스
  - S3 : 버킷
  - Lambda : 함수
> 블루프린트 : 예시

### 코드
> 코드 생성창
- 코드 save 후 deploy를 눌러야 실행 가능상태가 됨

- 실행 가능 창
  - cloud console
    > Lambda 창에서 실행
  - command line
  - Trigger
    > Lambda는 다른 AWS 서비스와 연동 가능

1. Trigger
- API 게이트웨이
  - 어떤 URL에 접속했을때 Lambda가 실행 됨
- DynamoDB
  - DynamoDB에 어떤 일이 발생했을때 Lambda가 실행 됨 
- S3
  - AWS에 파일이 업로드 되었을때 Lambda함수가 실행 됨

    ```python
    def lambda_handler(event, context):
        print(event)
        return event["left"]+event["right"]
    ```
- 재귀호출
  - 다른 서비스와 연동하기 


### 테스트
- 실행결과 -> 세부정보로 이벤트 결과 확인 가능
  - 청구 기간, 결과 코드 등

- 테스트 이벤트로 이벤트 생성 가능함

    ```json
    {
    "left": 2,
    "right": 3
    }
    ```

### 모니터링
- Cloud watch 
  - 활동 집계, 사용량, 요금등 체크할때 사용
- Log stream
  - 새로운 Log 확인 가능

## 가격정책
- 함수요청 수와 기간
  > 100만건/ 40만 초
  
- 기본설정 - 편집
  - 메모리
    - 


---
트리거 시작해야함