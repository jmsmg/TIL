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
  - command line
  - Triger

    ```python

    def lambda_handler(event, context):
        print(event)
        return event["left"]+event["right"]
    ```

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

## 디버깅 방법

## 가격정책


---
트리거 시작해야함