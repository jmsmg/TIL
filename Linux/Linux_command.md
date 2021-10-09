# Most Frequency Command Line

## directory

- pwd : 현재 디렉토리 확인

- ls : 목록 확인
  - -la : 숨김파일까지 표시
  - -p : 파일 앞에 / 표시
  - -t : 순차 정렬

- man : 매뉴얼 보기
  > man : 한글 사이트 https://nxmnpg.lemoda.net/ko/

---
## file

- rm : 삭제
  - rf : 그 디렉토리까지 삭제

- touch : 빈파일 생성
  - -t : 날짜수정
  - -h : 심볼릭링크 날짜 수정

- mkdir : 폴더 생성

- mv : 이동

- cp : 카피

- chmod 숫자 : 권한수정(퍼미션)

- echo

---
## output

- cat : 읽기
  - -e : 끝줄에 $가 표시됨 

- less : cat과 유사하나 뒤로 이동이 가능

- more : cat과 유사하나 위아래로 움직일 수 있음

---
## search

- head : 처음 10줄만 표시

- tail : 마지막 10줄 표시
  - -n : 줄 갯수 지정 가능

- grep : 원하는 행을 찾아줌
  - -V : 일치하지 않는 행 검색
  - -i : 대소문자를 구분하지 않고 일치하는 문장 검색 

---
## redirection

- < : input
- &#62; : output
- &#62;&#62; : append output
- | : pipeline

---
## environment variable

- wc 파일 : 줄, 단어, 글자수 
  > ex) cat file.txt | grep Thomas | wc -l 

- ifconfig : 네트워크 정보

- bc : 계산기
  > ex) echo "1 + 2" | bc

- find : 찾기
  - . : 현재폴더와 그 하위폴더
  - /경로
  - -name "이름"
  - -type : 파일타입
    - f : 일반파일
    - d : 디렉토리
  - -name "이름" : 파일이름으로 찾기
  - -exec 명령어 {} \; :
    > {}는 find에서 찾은 결과 대상

  
- env : 환경변수 목록
  - $

- export

- sort : 정렬(ASCII기반으로 대문자가 먼저)

- cut : 잘라내기
  - -d 
  - -f 숫자 : 필드 검색

- sed /parameter1/parameter2 : 데이터 흐름 수정
  - s/p1/p2(substitute)
  
  - /p1/p2 (delete)

- tr "A" "B" (A를 B로 대체)

- rev : 반대로 표기
  > 파이프라인으로 보통 연결됨

---

- ln : 심볼릭링크, 하드링크 설정
  - -S : 소프트링크

- file
  - -m : 매직파일 테스트파일 : 파일테스트
  - -C -m (파일명) : 파일 컴파일

- diff : 비교

- patch : 패치
  - -pNUM : 경로 지정
    > patch -p1 a < b.diff  

- find : 찾기
  - . : 현재폴더와 그 하위폴더
  - -type : 파일타입
    - f : 일반파일
    - d : 디렉토리
  - -name "이름" : 파일이름으로 찾기
  - -exec 명령어 {} \; :
    > {}는 find에서 찾은 결과 대상
