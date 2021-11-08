# 파이썬 문법

## algorithm
  > 문제에서 일정한 패턴을 발견하고, 패턴을 토대로 문제를 해결하는 절차

![압축 알고리즘](../img/Python_01.png)

## interacive shell
  > interpreter : C 언어

- interactive mode : 인터프리터와 대화하듯 코드를 처리

![REPL](../img/Python_02.png)

## 숫자 자료형

- 강제 전환 : int, float, complex
  - int(숫자)
  - int(계산식)
  - int('문자열')

![숫자](../img/Python_03.png) 

- 거듭제곱 : **

### 나눗셈 

- 나눗셈
  - / : 정수 / 정수 = 실수
  - // : 정수 // 정수 = 정수
    > floor division

- divmod (quotient, remainder) : 몫과 나머지 함께 구하기
  - 몫과 나머지가 튜플 형태로 나옴

- type() : 자료형 알아내기
  - type(숫자)
  - type(계산식)
  - type('문자열')

### 진수표현 base, decimal

- 2진수 : 0b (binary)
- 8진수 : 0o (october)
- 16진수 : 0x (hexa)

### 실수 계산
  > 실수값은 오차가 있음

## 변수와 입력

``` python
  # 기본 할당
  x = 10

  # 빈 변수
  x = none

  # 순차적 할당
  x, y = 10, 20
 
  # 마지막 10을 x,y,z에 할당
  x = y = z = 10
```

- del 변수 : 변수 삭제

- 할당과 동시에 연산
  - -=
  - +=
  - *=
  - /=

- 입력값 변수 저장
  - input('입력하세요')
    > input으로 입력받은 값은 항상 str
  ``` python
  a, b = input().split('기준 문자열') # 입력받은 값을 기준으로 분리

  print(a + b) # 스트링 형태이므로 원하는 연산 결과가 나오지않음

  #########

  a, b = map(int, input('숫자를 입력하세요').split()) # map을 활용해서 입력값을 int형으로 만듬

  print(a+b)
  ```

## 출력

- print 하나로 여러개 출력

``` python
print(1, 2, 3)
# 사이사이 공백으로 1 2 3으로 출력됨

print(1, 2, 3, sep=', ') #sep 옵션 사용하여 출력 구분값 지정가능 separate

print(1, 2, 3, sep='\n') #개행도 가능
print(1, end='') # 끝부분 지정 일반적으로 개행
```

## boolean과 비교 연산자 

- True False
  - is는 메모리 주소를 가르킴
  - id() : 객체의 메모리주소를 불러옴
  - is, is not은 객체가 같은지 확인

- 논리연산자와 우선순위
  - not
  - and
  - or

---

## Built_function

- List
  - append : 리스트 끝에 원소 추가(변수 자체를 넣음(리스트 안에 리스트도 가능))
  - extend : 리스트 끝에 모든 원소 추가(iterable의 각 항목을 넣음)
    > [append vs extend](https://m.blog.naver.com/wideeyed/221541104629)

  - copy : 원본에 영향을 주지않기 위해 사용
  - clear : 리스트 안에 원소 모두 삭제
    > copy(deep copy)를 한 함수는 사라지지않음

  - count(a) : 리스트 안에 원소 a의 갯수 반환
  - index : 리스트 값의 위치를 반환

  - insert(a,b) : 리스트의 a위치에 b원소 삽입
  
  - pop : 리스트의 지정한 위치에 원소 삭제(위치를 지정)
  - remove : 리스트에 들어있는 원소 삭제(원소를 지정)

- format()
  - format(value, format_spec)
  - 형식 지정자가 제어하는 주어진 값의 형식화 된 표현을 출력

- filter(functiom, iterable)
  - iterable의 각 요소가 tru인지 아닌지 확인후 출력

- Map(function, iterable, ...)
  - 주어진 function을 iterable의 각 항목에 적용하고 결과 목록을 출력


---


### 1. Comprehension

- List Comprehension

    ```python
    [expression for item in list]
    ```

- Set Comprehension
- Dict Comprehension
- Generator Expression

> https://codechacha.com/ko/python-comprehension/


