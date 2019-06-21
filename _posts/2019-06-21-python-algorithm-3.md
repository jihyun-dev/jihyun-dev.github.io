---
layout: post
title: 'Python 백준 알고리즘 3단계 - 사칙연산'
date: 2019-06-21
update: 2019-06-21
author: Jihyun
cover: '/assets/img/2019-06-18-python-algorithm-cover.png'
tags: Python, Algorithm
---


> 백준 단계별 풀이 - 1단계(입/출력 받아보기) 문제를 풀이한다.


## 3단계

### 10869. 사칙연산
A+B, A-B, A*B, A/B(몫), A%B(나머지)를 출력하는 프로그램
```python
# 입력 : 7 3
# 출력: 10
#      4
#      21
#      2
#      1
a, b = map(int, input().split())
print(a+b, a-b, a*b, a//b, a%b, sep='\n')
```
* 몫을 반환하는 연산자: // <br>
  나머지를 반환하는 연산자: %
* print()에서 줄바꾸기: sep=\n 추가


### 2558. 두 정수를 입력받아 A+B 출력
```python
# 입력: 1
#      2
# 출력: 3
print(int(input())+int(input()))
```
```python
sum = 0
for n in range(2):
    num = int(input())
    sum += num
print(sum)
```
* input()으로 받은 값은 문자열이므로 int로 매핑: int(input())



#### 관련글
- [Python 백준 알고리즘 1단계 - 입/출력 받아보기](https://jihyun-dev.github.io/2019/06/19/python-algorithm-1.html)
- [Python 백준 알고리즘 2단계 - 사칙연산](https://jihyun-dev.github.io/2019/06/20/python-algorithm-2.html)

#### **Reference**
- Baekjoon Online Judge: https://www.acmicpc.net
