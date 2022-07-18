# 07.18

- [x] 수업OT
- [x] 프로그래밍이란?
- [x] 파이썬과 개발환경
- [x] 기초 문법
- [x] 자료형

### 프로그래밍 학습 마인드셋

1. **개념 구조화 하기**
- 개념 정의
- 개념의 포함 관계
- 개념의 차이점
1. **직접 코딩하기**
2. **동료 학습**
- 개념 설명해주기
- 코드 에러 함께 해결하기
- 모르는 내용 서로 질문/대답하기

### 프로그래밍의 정의

1. **프로그램** : 특정 작업을 수행하는 명령어들의 모음

2. **과정**
   
   파이썬으로 소스 코드를 짜기 → 인터프리터가 파이썬을 기계어로 번역 → 프로그램 수행

3. **파이썬의 장점**
- 알고리즘 코테에 유리
- 유용한 라이브러리를 최소한으로 사용해 개발이 가능
- 인간 친화적인 언어
- OOP : 객체지향프로그래밍 언어
1. **프로그램 구성단위**
- 표현식 : 새로운 데이터 값을 생성하거나 계산하는 코드 조각
- 문장 : 특정한 작업을 수행하는 코드 전체

⇒ *모든 표현식은 문장이다!*

1. **파이썬 개발환경**

> **IDE의 기능**
> 
> - 세로 커서 (Alt + Ctrl + 화살표)
> - 특정 단어 replace (Ctrl + D)
> - 줄 바꿈(Alt + 화살표)
> - 줄 복사(Alt + Shift + 화살표)
> - 화면 Split

### 기초 문법

- 추상화(변수 사용)
  
  - 가독성 증가
  - 코드 수정 용이
  
  ```python
  Pizza_price = 10000
  print(Pizza_price*4) # 40000
  ```

- 연산자 : 우선순위 적용 계산
  
  ‘ + ’ : 덧셈
  
  ‘ - ’ : 뺄셈
  
  ‘ * ’ : 곱셈
  
  ‘ ** ’ : 거듭제곱
  
  ‘ / ’ : 나눗셈
  
  ‘ // ’ : 몫
  
  ‘ % ’ : 나머지

- 식별자
  
  변수 이름 규칙과 식별자는 변수 이름으로 작성불가!(예약어)
  
  ```python
  import keyword
  print(keyword.kwlist)
  
  # 출력
  ['False', 'None', 'True', '__peg_parser__', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
  ```

### 자료형

- int : 정수 자료형

- float : 실수 자료형
  
  부동 소수점을 고려해 실수 연산해야함!!

- 비교 연산자
  
  주로 조건문에 사용되며 값을 비교
  
  True / False 값을 리턴
  
  | 연산자    | 내용       |
  | ------ | -------- |
  | <      | 작다       |
  | ≤      | 같거나 작다   |
  | >      | 크다       |
  | ≥      | 같거나 크다   |
  | ==     | 같다       |
  | ≠      | 같지 않다    |
  | is     | 객체 아이덴터티 |
  | is not | 아닌 경우    |

- 논리 연산자
  
  - Falsy : False는 아니지만 False로 취급되는 값
    
    0, 0.0, (), [], {}, None, “”(빈문자열)
  
  - 논리 연산자 우선순위
    
    not > and > or

| 연산자     | 내용                         |
| ------- | -------------------------- |
| A and B | A와 B 모두 True 이면 True       |
| A or B  | A와 B 모두 False 이면 False     |
| Not     | True → False, False → True |

- 시퀀스형
  
  - Tuple
    
    리스트와의 차이점 : 생성 후 담고 있는 값 변경이 불가!
    
    ```python
    # 튜플은 소괄호!
    a = (1, 2, 3, 1)
    print(a[1]) # 2
    
    # 값 변경 X
    a[1] = 3 # 변경 안됨!
    
    # 단일 항목 튜플은 쉼표 넣어주기!!
    tuple_a = (1,)
    print(tuple_a) # (1,)
    ```
  
  - List
    
    여러 데이터를 저장하고 싶을 때 사용
    
    ```python
    my_list = []
    another_lsit = list()
    print(type(my_list))
    print(type(another_list))
    
    location = ['서울', '대전', '구미', '광주', '부울경']
    print(location)
    
    location[0] = '전주'
    print(location)
    ```
  
  - Range
    
    - 숫자의 시퀀스(수열)를 나타내기 위해 사용
    - 주로 반복문과 함께 사용
    
    ```python
    # 0부터 4이전 값까지
    print(list(range(4))) # [0, 1, 2, 3]
    
    # step 활용
    print(list(range(1, 5, 2))) # 1부터 5이전 값까지 2칸씩 [1, 3]
    
    # 역순
    print(list(range(4, 1, -1))) # [4, 3, 2]
    ```
  
  - 슬라이싱
    
    문자열의 특정 부분만 잘라내기
    
    ```python
    # 리스트[1:4]에서 1은 포함 4는 미포함
    print([1, 2, 3, 5][1:4]) # [2, 3, 5]
    
    # 튜플
    print((1, 2, 3)[:2]) # (1, 2)
    
    # 문자열
    print('abcd'[2:4]) # cd
    
    # 예제
    s = 'abcdefghi'
    S[::] # 'abcdefghi'
    S[::-1] # 'ihgfedcba'
    ```

- 비시퀀스형
  
  - Set
    
    - 중복된 요소 없이(중복원소X) 순서에 상관없는(인덱스X) 데이터 묶음
    - 집합 연산 가능
    - 담고 있는 요소 삽입, 변경, 삭제 가능
    
    ```python
    # Set은 중복 값 제거
    print({1, 2, 3, 1, 2}) # {1, 2, 3}
    
    # Dictionary는 빈 중괄호 {}
    blank = {}
    ```
    
    | 연산자 | 설명    |
    | --- | ----- |
    |     |       |
    | &   | 교집합   |
    | -   | 차집합   |
    | ^   | 대칭차집합 |
  
  - Dictionary
    
    - key-value 쌍으로 이뤄진 자료형
    - key : 변경 불가능한 데이터만 활용 가능(string, int, float, boolean, tuple, range)
    - values : 어떤 형태든 관계없음
    
    ```python
    dict_a = {}
    print(type(dict_a)) # <class 'dict'>
    
    dict_a = {'a': 'apple', 'b': 'banana', 'list': [1, 2, 3]}
    print(dict_a) # {'a': 'apple', 'b': 'banana', 'list': [1, 2, 3]}
    print(dict_a['list']) # [1, 2, 3]
    ```

            

- 형변환
  
  문자 ↔ 숫자 서로 변환 가능!!
  
  - 컨테이너 형변환
  
  |            | string | list    | tuple   | range | set     | dictionary |
  | ---------- | ------ | ------- | ------- | ----- | ------- | ---------- |
  | string     |        | O       | O       | X     | O       | X          |
  | list       | O      |         | O       | X     | O       | X          |
  | tuple      | O      | O       |         | X     | O       | X          |
  | range      | O      | O       | O       |       | O       | X          |
  | set        | O      | O       | O       | X     |         | X          |
  | dictionary | O      | O(key만) | O(key만) | X     | O(key만) |            |
