# gcc

gcc -Wall -Wextra -Werror 합칠 파일명 -o 만들 파일

- Wall
  - 모든 모호한 코딩에 대해서 경고를 보내는 옵션
- Werror
  - 모든 경고를 컴파일을 중단하는 에러로 취급해서 경고 하나만 나와도 컴파일 중단.
- Wextra
 - Wall에 각종 추가적인 Warning옵션을 추가

> ex) gcc -Wall -Wextra -Werror *.c -o main

- main 함수
```C
void ft_print_reverse_alphabet();
int main(){
    ft_print_reverse_alphabet();
}
```

## 헤더 설정

- 환경변수
  - export MAIL=

- 설정변경 
  - ~/.zshrc