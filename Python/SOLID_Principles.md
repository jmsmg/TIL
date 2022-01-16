# SOLID 패턴

## Single Responsibility(단일 책임 원칙)

- 한 객체는 한가지의 책임만 있어야함

``` python
def add(num1, num2):
    return num1 + num2

def numPrint(num):
    print(num)

def addPrint(num1, num2):
    num = num1 + num2
    print(num)
    return num
```

- add 함수, numPrint 함수는 단일 책임 원칙을 지켰음
- 코드를 줄인다고 addPrint로 묶으면 단일 책임 원칙에 위배됨

``` python
class Cat:
    def __init__(self, age, name):
        self.age = age
        self.name = name

    def eat(self, food):
        pass
    
    def walk(self):
        pass
    
    def speak(self):
        pass

    # def print(self):
    #     print(f"age:{self.age} name:{self.name}")

    # def log(self, logger):
    #     logger.log(f"age:{self.age} name:{self.name}")
    #     logger.log(datetime.now())

    def repr(self):
        return f"age:{self.age} name:{self.name}"

kitty = Cat()
print(kitty.repr())
logger.log(kitty.repr())
```

- 고양이 고유의 기능이 아닌 print, log등은 삭제하고 밖으로 빼줌으로 단일책임원칙을 지킴


## Open-Closed Principle(개방 폐쇄 원칙)

- 확장에 대해서는 개방, 수정에 대해서는 폐쇄

``` python
def Animal:
    def __init__(self.a_type):
        self.a_type = a_type

def hey(animal:Animal):
    if animal.a_type == 'Cat':
        print('meow')
    elif animal.a_type == 'Dog':
        print('bark')
    else:
        raise Error('wrong a_type')
```

- 위 코드는 고양이, 개가 아닌 다른 동물을 추가하려면 '수정'이 필요함

```python
class Animal:
    def speak(self):
        pass

class Cat(Animal):
    def speak(self):
        print('meow')

class Dog(Animal):
    def speak(self):
        print('bark')

def hey(animal:Animal):
    animal.speak()
```

- hey 함수 수정 없이 밖에서 확장 가능함

