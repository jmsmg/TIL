# Django

## django 세팅 순서

### 1. 가상환경 세팅

- 가상환경 설치
  - python - m venv venv : venv라는 이름의 가상환경 생성

- 가상환경 접근
  - source venv/bin/activate : 가상환경 실행
  - deactivate : 가상환경 종료

- 패키지 확인
  - pip list

### 2. django 설치

- 가상환경 접근
- pip install django
- django-admin startproject (프로젝트명) .
  - 현재 폴더에 (프로젝트명)의 폴더가 하나 생성됨
  -

### 사용 명령어 정리

- python
  - -V : 버전 체크
  - -m venv (이름) : (이름)의 가상환경을 만듬

- source
  - (activate의 경로)

- pip
  - list : 설치된 pip 패키지
  - install django==버전

- django-admin
  - startproject 프로젝트명 .