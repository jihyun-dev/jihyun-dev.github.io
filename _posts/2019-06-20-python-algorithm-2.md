---
layout: post
title: '[Python] 백준 알고리즘 2단계 - 사칙연산'
date: 2019-06-20
update: 2019-06-20
author: Jihyun
cover: '/assets/img/2019-06-18-python-algorithm-cover.png'
tags: Python Algorithm
---



> 백준 단계별 풀이 - 2단계(사칙연산) 문제를 풀이한다.


## 2단계 if문

### 1330. 두 수 비교하기
자연수 N이 주어졌을 때, 1부터 N까지 한 줄에 하나씩 출력하는 프로그램
```python
a, b = map(int, input().split())
print('<' if a < b else '>' if a > b else '==')
```
* inline elif 사용

### 9498. 시험 성적
시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램
```Python
n = int(input())
print('A' if 90<=n<=100 else 'B' if 80<=n<=89 else 'C' if 70<=n<=79 else 'D' if 60<=n<=69 else 'F')
```
```Python
print("FFFFFFDCBAA"[int(input())//10])
```
* 입력값을 10점으로 나눈 후, 문자열 리스트의 인덱스로 출력한다.
* 도대체 이런 생각은 어떻게 하는걸까,........

### 2753. 윤년
연도가 주어졌을 때, 윤년이면 1, 아니면 0을 출력하는 프로그램
(윤년은 연도가 4의 배수이면서, 100의 배수가 아닐 때 또는 400의 배수)

```Python
n = int(input())
print(1 if n%4 == 0 and n%100 != 0 else 1 if n%400 == 0 else 0 )
```
```Python
print(int((n%4 == 0 and n%100 != 0) or n%400))
```

### 2884. 알람 시계
입력 시간보다 45분 일찍 맞춰지는 알람 시계 프로그램
```Python
# 입력: 10 10
# 출력: 9 25
h, m = map(int, input().split())
m -= 45
if m<0:
    h -= 1
    if h<1:
        h = 23
        m = 60+m
    else:
        m = 60+m
elif m == 0:
    m = 0
print(h, m)
```

### 10817. 세 수
세 정수 A, B, C가 주어지고, 두 번쨰로 큰 정수를 출력하는 프로그램
```Python

```

#### 관련글
- [Python 백준 알고리즘 1단계 - 입출력과 사칙연산](https://jihyun-dev.github.io/2019/06/19/python-algorithm-1.html)
- [Python 백준 알고리즘 3단계 - for문](https://jihyun-dev.github.io/2019/06/20/python-algorithm-3.html)

#### **Reference**
- Baekjoon Online Judge: https://www.acmicpc.net
