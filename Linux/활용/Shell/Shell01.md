# Shell

- 환경변수

- 개행 없애기 -tr -d '\n\'

- basename : 경로를 포함한 파일 이름을 인수로 받아 파일 경로를 제거하고 필요에 따라서 확장자로 삭제하여 순수하게 파일명만 남게한다.
  - [경로 + 파일이름] [확장자]
  - 확장자

- find ./ -type f -exec basename {} \; : find ./는 현재 디렉토리 이하 모든 디렉토리와 파일을 다 고르는 것. 근데 -type f 옵션을 주면 디렉토리는 제외하고 파일만 찾는다. -exec basename {} \; 옵션은 결과에서 ./ 표시되는 부분을 제외하고 파일명만 출력해준다.

- [xags](https://ko.linux-console.net/?p=229)
- sed 's/.sh//' : 뒤 확장자를 없앴다.


- [wc](https://ko.wikipedia.org/wiki/Wc_(유닉스)) 파일명 : 줄(line), 단어(word), 문자(char) 바이트
  - -l : 줄만 출력 (행)

- [sed(streamlined editor)](https://blog.naver.com/kylegglee/222305181874) "s/p1/p2/g" 파일명 : 데이터 흐름 수정
  > s/p1/p2/i : 대소문자 상관 없이 변경

- sed -e 's/^[ \t]*//' : 맨 처음 튀어나오는 공백 제거


- [ifconfig](https://www.whatap.io/ko/blog/11/) : 활성화된 네트워크 인터페이스 표시
  - -a : 모든 네트워크 인터페이스를 보여줌

- [grep](https://blog.dalso.org/linux/linux-command/8401) 파일명 : 행을 찾아줌
  - 'ether '

- cut(https://bbolmin.tistory.com/32) : 문자 자르기
  - -c - 

- 뒷 공백 없애야함

- echo
  - -n : 개행 없이

- 특수문자, 정규표현식

- "\"\\?\$*'MaRViN'*\$?\\\""

- awk(https://recipes4dev.tistory.com/171) : 
  > pattern { action } 스크립트 형식의 프로그래밍 언어로 작성됨
  - 홀수부분만 보여주기

- grep
  - -v : "^#"을 하면 #이 있는 곳 제외 (여집합)
    > 주석제거
- awk

- [cut -d](https://bbolmin.tistory.com/32)
  -f 필드(1) : 잘라낼 필드를 정한다.
- rev
- sort r (오름차순)
- xargs
- sed
  >sed로 작업한 부분만 억제해서 출력시키고 싶다면 -n옵션을 써줘야해요. 그래서 -n옵션은 p와 항상 짝짝꿍으로 사용됩니다. 

- 진법 사용
- ibase는 input, obase는 output base라 생각하면 된다.
- 5 진법 사용
- 13 진법 사용
- 23 진법
- bc : eval같은 놈이다. 앞에서 받은 문자열들을 그대로 계산한다. 위 예에서 해당 수들을 5진법으로 계산해서 합하고, 출력은 23진법으로 하면 된다.