# 데이터 구조 / 메서드



> **데이터 구조 활용**

- 메서드를 활용
- 메서드는 클래스 내부에 정의한 함수, 객체의 기능 역할

```python
# 데이터 구조.메서드()

List.append(10)
String.split()
```

> **문자열**

- 모든 문자열 str은 변경 불가능!!

```python
word = 'ssafy'
print(id(word)) # 메모리 주소 2584805085808
word = 'test'
print(id(word)) # 메모리 주소 2584805080880

'''
실제로 word 안에 값이 바뀐 것이 아니라 아예 다른 새로 만든 것!!

'''
```

> **문자열 조회/탐색 및 검증 메서드**

| s.find(x)   | x의 첫번째 위치를 반환, 없으면 -1 반환 ⇒ 오류가 발생X |
| ----------- | ---------------------------------- |
| s.index(x)  | x의 첫번째 위치를 반환, 없으면 오류 발생O          |
| s.isalpha() | 알파벳 문자 여부(한국어 포함)                  |
| s.isupper() | 대문자 여부                             |
| s.islower() | 소문자 여부                             |
| s.istitle() | 타이틀 형식 여부                          |

```python
print('apple'.find('p')) # 1
print('apple'.find('y')) # -1
print('apple'.index('y')) # 오류 발생!
```

> **문자열 변경 메서드**

| s.replace(old, new)            | 대상 글자를 새로운 글자로 변경해 반환                   |
| ------------------------------ | --------------------------------------- |
| s.strip([chars])               | 공백이나 특정 문자를 제거                          |
| s.split(sep=None, maxsplit=-1) | 공백이나 특정 문자를 기준으로 분리                     |
| ‘separator’.join([iterable])   | 구분자로 iterable을 합침                       |
| s.capitalize()                 | 가장 첫 번째 글자를 대문자로 변환                     |
| s.title()                      | 띄어쓰기 기준으로 단어의 첫번째 글자는 대문자, 나머지는 소문자로 변환 |
| s.lower()                      | 모두 소문자로 변경                              |
| s.upper()                      | 모두 대문자로 변경                              |
| s.swapcase()                   | 대↔소문자 서로 변경                             |

```python
print('a,b,c'.split(',')) # ['a', 'b', 'c']
print('a b c'.split()) # ['a', 'b', 'c']
print(type('a b c'.split())) # <class list>

print(' '.join(['3', '5'])) # 3 5
print('*'.join('ssafy')) # s*s*a*f*y

msg = 'hI! Everyone, I\\'m ssafy'

print(msg.capitalize()) # Hi! everyone, i'm ssafy
print(msg.title()) # Hi! Everyone, I'M Ssafy
print(msg.upper()) # HI! EVERYONE, I'M SSAFY
print(msg.lower()) # hi! everyone, i'm ssafy
print(msg.swapcase() # Hi! eVERYONE, i'M SSAFY
```

> **리스트 메서드**

| L.append(x)            | 마지막에 항목 x를 추가                         |
| ---------------------- | ------------------------------------- |
| L.insert(i, x)         | 리스트 인덱스 i에 항목 x를 삽입                   |
| L.remove(x)            | 리스트 가장 왼쪽에 있는 항목 첫번째 x를 제거            |
| L.pop()                | 리스트 가장 오른쪽에 있는 항목을 반환 후 제거            |
| L.reverse()            | 원본 순서를 반대로 뒤집기, None                  |
| L.sort()               | 원본 리스트를 정렬, None                      |
| L.count(x)             | 항목 x의 개수 세기                           |
| L.pop(i)               | 인덱스 i에 있는 항목을 반환 후 제거                 |
| L.extend(m)            | 순회형 m의 모든 항목들을 리스트 끝에 추가 (+= 과 같은 기능) |
| L.index(x, start, end) | 리스트에 있는 항목 중 가장 왼쪽에 있는 항목 x의 인덱스를 반환  |
| L.clear()              | 모든 항목을 삭제                             |

> **튜플(Tuple)**

- 여러 값을 순서가 있는 구조로 저장할 때 사용

- 생성 후 값 변경이 불가(불변 자료형)
  
  ⇒ 값에 영향을 미치지 않는 메서드만 지원

```python
day_name = ('월', '화', '수', '목')
print(day_name*2)
print(id(day_name)) # 1818503269808
day_name += False, True
print(day_name)
print(id(day_name)) # 1818502908608
```

> **시퀀스형 연산자**

- 반복연산자(*) : 시퀀스를 반복



---

### ***비시퀀스형 데이터 구조***



> **셋(Set)**

- 중복되는 요소 없이, 순서 상관 없는 데이터 구조

| s.copy()        | set의 얕은 복사본을 반환                                            |
| --------------- | ---------------------------------------------------------- |
| s.add(x)        | 항목 x가 set에 없다면 추가                                          |
| s.pop()         | set에서 랜덤하게 항목을 반환하고, 해당 항목을 제거, set이 비어 있을 경우는 keyError 발생 |
| s.remove(x)     | 항목 x를 set에서 삭제, 항목이 존재하지 않을 경우 keyError 발생                 |
| s.discard(x)    | 항목 x가 set에 있는 경우 항목 x를 set에서 삭제                            |
| s.update(t)     | set t에 있는 모든 항목 중 set s에 없는 항목을 추가                         |
| s.clear()       | 모든 항목을 제거                                                  |
| s.isdisjoint(t) | set s가 set t의 서로소이면 True 반환                                |
| s.issubset(t)   | set s가 set t의 하위 set인 경우, True 반환                          |
| s.issuperset(t) | set s가 set t의 상위 set인 경우, True 반환                          |

```python
a = {} # <type dictionary !!>

# s.update()
a = {'사과', '바나나'}
print(a) # {'사과', '바나나'}
a.update(['딸기', '바나나', '수박']) # {'사과', '딸기', '수박', '바나나'}
print(a)

# s.remove()
a.remove('사과')
print(a) # {'바나나', '딸기', '수박'}
a.remove('사과') # 항목이 없으면 key error 발생!

# s.discard()
a.discard('사과')
print(a) # 없어도 error 발생 X

# s.pop()
a.pop()
print(a) # 임의의 원소 하나 제거 후 반환
```



> **딕셔너리(Dictionary)**

| d.clear()   | 모든 항목을 제거                                             |
| ----------- | ----------------------------------------------------- |
| d.copy()    | dict d의 얕은 복사본을 반환                                    |
| d.keys()    | dict d의 모든 키를 담은 뷰를 반환                                |
| d.values()  | dict d의 모든 값을 담은 뷰를 반환                                |
| d.items()   | dict d의 모든 키-값 쌍을 담은 뷰를 반환                            |
| d.get(k)    | 키 k의 값을 반환하는데, 키 k가 dict d에 없을 경우 None을 반환            |
| d.get(k, v) | 키 k의 값을 반환하는데, 키 k가 dict d에 없을 경우 v을 반환               |
| d.pop(k)    | 키 k의 값을 반환하고 키 k인 항목을 dict d에서 삭제하는데, 없으면 keyError 발생 |
| d.pop(k, v) | 키 k의 값을 반환하고 키 k인 항목을 dict d에서 삭제하는데, 없으면 v를 반환       |
| d.update()  | dict d의 값을 매핑하여 업데이트                                  |

```python
my_dict = {'apple': '사과', 'banana': '바나나'}
print(my_dict.get('apple')) # 사과
print(my_dict.get('pineapple')) # None
print(my_dict.get('pineapple', 0)) # 0

my_dict.update(apple='비싸!!')
print(my_dict) # {'apple': '비싸!!', 'banana': '바나나'}
```

---

### *할당(Assignment)*



> **대입 연산자 (=)**

🔶 **얕은 복사** 🔶

```python
original_list = [1, 2, 3]
copy_list = original_list
print(original_list, copy_list) # [1, 2, 3] [1, 2, 3]

copy_list[0] = 'hello'
print(original_list, copy_list) # ['hello', 2, 3] ['hello', 2, 3] !!!

'''
같은 주소를 쓰기 때문에 한쪽 리스트의 값을 변경하면 똑같이 변경됨!!

'''
```

<img src="file:///C:/Users/gij45/ssafy8/img/Untitled.png" title="" alt="Untitled.png" data-align="center">

🔶 **1차원 배열에서 얕은 복사 해결 방법** 🔶

```python
original_list = [1, 2, 3]
copy_list = original_list[:]
print(original_list, copy_list) # [1, 2, 3] [1, 2, 3]

copy_list[0] = 'hello'
print(original_list, copy_list) # [1, 2, 3] ['hello', 2, 3] !!!
```

<img src="file:///C:/Users/gij45/ssafy8/img/Untitled%20(1).png" title="" alt="Untitled (1).png" data-align="center">

🔶 **2차원 배열의 얕은 복사 문제** 🔶

```python
a = [1, 2, ['a', 'b']]
b = a[:]
print(a, b) # [1, 2, ['a', 'b']] [1, 2, ['a', 'b']]
b[2][0] = 0
print(a, b) # [1, 2, [0, 'b']] [1, 2, [0, 'b']] # 2차원 배열 안에서 얕은 복사 또 발생!!
```

<img src="file:///C:/Users/gij45/ssafy8/img/Untitled4.png" title="" alt="Untitled4.png" data-align="center">

🔶 **깊은 복사** 🔶

```python
import copy

a = [1, 2, ['a', 'b']]
b = copy.deepcopy(a)
print(a, b) # [1, 2, ['a', 'b']] [1, 2, ['a', 'b']]
b[2][0] = 0
print(a, b) # [1, 2, ['a', 'b']] [1, 2, [0, 'b']]
```

<img src="file:///C:/Users/gij45/ssafy8/img/Untitled%20(2).png" title="" alt="Untitled (2).png" data-align="center">
