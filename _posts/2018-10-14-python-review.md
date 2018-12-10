---
layout: post
title: 'Python 기본 문법'
date: 2018-10-14
update: 2018-11-13
author: Jihyun-ella
cover: '/assets/img/2018-10-14-python-review-cover.png'
tags: Python
---


> 파이썬으로 알고리즘 학습하기 전에, 기본 문법을 먼저 복습하며 정리한다.


## 1. 주석

```python
print("Hello, comment?") #This is comment line.
```

## 2. 변수
변수란, **'변할 수 있는 수'** 를 뜻한다.

```python
a = 1, b =2, c =3 # 변수에 값 대입
```

### 2.1. 변수명 규칙
- 사용 가능: 영문(대/소문자), 숫자, 언더바
- 사용 불가: 공백, 숫자로 시작, Python Keyword


### 2.2 Python Keyword
```
False, None, True, and, as, assert, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield
```  


## 3. 숫자
정수(2진수, 8진수, 10진수, 16진수), 실수, 복소수 등을 표현할 수 있다.
```python
i = 1 # 정수
pi = 3.14 # 실수
complex = 1+2j # 복소수
hex_i = 0xFF # 16진수(10진수 255)
oct_j = 0o10 # 8진수(10진수 8)
bin_k = 0b1000 # 2진수(10진수 8)
```

## 4. 문자
큰옴표, 작은따옴를 사용하여 표현한다.
```python
"큰따옴표 문자열"
```
```
'큰따옴표 문자열'
```
```python
'작은따옴표 문자열'
```
```
'작은따옴표 문자열'
```



## 5. 연산자(양수)
```python
10+3 # 더하기
10-3 # 빼기
10*3 # 곱하기
10/3 # 나누기
10//3 # 나눈 몫
10%3 # 나눈 나머지
10*(2+3) # 안쪽의 괄호 먼저 계산
a+b+c # 변수의 연산
```
## 6. 비교 연산자
양쪽의 값을 비교할 때, 비교 결과가 참일 때는 True, 거짓일 때는 False를 나타낸다.

|Operator|Description|
|:---:|:---|
|==|값이 같다|
|!=|값이 다르다|
|<|왼쪽이 오른쪽보다 작다|
|>|왼쪽이 오른쪽보다 크다|
|<=|왼쪽이 오른쪽과 작거나 같다|
|>=|왼쪽이 오른쪽과 같거나 크다|

## 7. 출력
화면에 출력하기 위해서 print() 함수를 사용한다.
```python
print("Hello, I'm Jihyun!") # 문자열 출력

age = 24 # 변수에 값을 저장
print("I'm", age, "years old.") # 연속 출력은 쉼표(,)를 사용
```

## 8. 조건문
if, if-else, if-elif-else를 사용한다. 블록을 구분하기 위한 들여쓰기를 주의한다
```Python
if 비교:
  True일 때 문장
else:
  False일 때 문장
```
예제
```Python
a = 10
if a % 2 == 0:
    print(a, "은(는) 짝수입니다.")
elif a % 2 == 1:
    print(a, "은(는) 홀수입니다.")
else:
    print("계산 오류")
print("예제 종료")
```
```
10은(는) 짝수입니다.
예제 종료
```

## 9. 반복문
반복문에는 for 명령과 while 명령이 있다.

### - for
n=0부터 n=2까지(**3은 제외**), 3번 반복
```python
for n in range(3):
    print(n)
```
```
0
1
2
```
m=1부터 n=2까지(**3은 제외**), 2번 반복
```python
for m in range(1, 3):
    print(m)
```
```
1
2
```
리스트 a 안의 값을 차례로 반복
```Python
a = [1, 3, 5, 7, 9]
for x in a:
  print(x)
```
```
1
3
5
7
9
```

### - while
i=1부터 1씩 증가하여 3까지 출력
```Python
i=1
while True:
  print(i)
  if i == 3: break
  i+=1
```
```
1
2
3
```

### 10. 함수
```python
def 함수이름(파라미터):
  실행 코드
  return 결과값(생략 가능)
```
```Python
def even_or_odd(n):
  if n % 2 == 0:
    print("This is even")
    return
  print("This is odd")
```
```
>>> even_or_odd(10)
This is even
>>> even_or_odd(13)
This is odd
```
