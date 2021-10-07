# Linux3

## whereis, $PATH

- whereis : 실행파일의 경로를 찾아주는 명령어
  > whereis ls : ls의 실행파일 경로, man ls 경로

- $PATH : 변수, 실행파일이 실행되는 기본경로

## back ground execute (ctrl + Z, &)

- 실행중인 파일 보기
  - jobs
    - kill %번호 : 종료
    - kill -9 %번호 : 강제종료

- & : 실행하며 다른 작업 진행하기

- foreground로 당기기
  - fg

- background로 넘기기
  - ctrl + z

---
## daemon
  > 항상 켜져있음  
  
- 데몬 프로그램 경로 :/etc/init.d/

- sudo service apache2 start (아파치2 서비스 시작)

---

## Group
  > 리눅스는 다중사용자 환경

- User : 파일을 생성한 사람
- Other : User가 아닌 사람

- Group : Other들을 묶을 수 있음
  > Group으로 그룹 권한 부여 가능 

### 명령어
- useradd
  - -G 그룹명 User_name : 존재하지않는 사용자를 만들고 그룹에 넣을때 사용

- groupadd : 새로운 그룹 생성
  - 그룹이름

- usermod(user_modify) : 존재하는 사용자를 수정
  - -a -G 그룹명 수정할사용자이름
  > 그룹에 수정할 사용자가 속하게 됨

- chown 유저 그룹 파일디렉토리
  > 파일디렉토리의 유저와 그룹을 바꿈

## sed
  > 비상호대화형 스트링 편집기 : 반복된 텍스트 처리를 위해 사용가능

- 비상호대화형 스트링편집기
  - 원본을 건드리지 않음 (-i옵션 설정시 원본 수정가능)
  - 버퍼
    - 패턴 버퍼
    - 홀드 버퍼

---

## 환경변수

1. 전역변수
  - 전역 환경변수 확인
    - env

2. 지역변수
  - 지역 환경변수 확인
    - printenv 특정환경

- 할당(선언)
  - 변수 = 값

- 변수 내보내기
  - export 변수 


--- 

데몬 해야함