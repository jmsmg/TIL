# Global_infra

## AWS 데이터 센터

1. Data Region(지리적으로 격리)
    - 규정준수(나라별 법규)
    - 지연시간(실제 이용자와의 거리)
    - 기능 가용성(새로운 기능이 나올때 다를 수 있음)
    - 요금(센터별로 다름)

    ![region](../img/Region.png)

2. Edge Location(Amazon Cloud Front)
    - 브라질 -> 한국
    - EC2 instance(브라질) -> 캐시 전송 -> Edge Location(한국) -> 고객

3. Provisioning
    > 사용자 요구사항에 맞게 할당, 배치, 배포하여 시스템을 사용가능하도록 준비하는 절차
    - API 호출
    - AWS Management Console
      > 브라우저 기반
    - AWS CLI(Command-Line Interface)
      - API 명령어 실행(복붙)
    - AWS SDK(Software Development Kit)
      - 개발키트

    - AWS Elastic Beanstalk
    - AWS CloudFormation

    ![cloudformation](../img/CloudFomation.png)


---

고가용성 및 내결함성
Amazon Braket

CDN
Amazon Cloud front
Route 53
AWS outposts 실물로 설치해줌
Elastic beanstalk
cloudFormation