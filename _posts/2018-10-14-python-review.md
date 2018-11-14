---
layout: post
title: 'Python 기본 문법 정리!'
date: 2018-10-14
update: 2018-11-13
author: Jihyun-ella
cover: 'https://user-images.githubusercontent.com/43994376/47008979-53f96700-d176-11e8-9fa5-caa20a5c00a3.png'
tags: Python
---


> 파이썬으로 알고리즘 학습하기 전에, 기본 문법을 먼저 복습하며 정리하자.

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


## 4. 연산자(양수)
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

## 5. 출력
화면에 출력하기 위해서 print() 함수를 사용한다.
```python
print("Hello, I'm Jihyun!") # 문자열 출력

age = 24 # 변수에 값을 저장
print("I'm", age, "years old.") # 연속 출력은 쉼표(,)를 사용
```

## 6. 비교
