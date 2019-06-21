---
layout: post
title: 'Python 백준 알고리즘 2단계 - 사칙연산'
date: 2019-06-20
update: 2019-06-20
author: Jihyun
cover: '/assets/img/2019-06-18-python-algorithm-cover.png'
tags: Python, Algorithm
---


> 백준 단계별 풀이 - 1단계(입/출력 받아보기) 문제를 풀이한다.


## 2단계 사칙연산 도전하기

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

### 2839. 설탕 배달
3kg와 5kg의 설탕을 가장 적은 수의 봉지로 배달하려고 한다. <br>
설탕의 무게를 입력받고,<br>
이 값이 3, 5kg의 두 봉지로 조합이 가능하다면, 가장 적은 봉지의 수를 출력하고,
조합이 되지 않는다면 -1을 출력한다.

입력의 경우의 수:
1. 5와 3의 배수 or 5의 배수 => 가장 큰 봉지(5)로 최대한 많이 담는다. => total % 5 = 0<br>
2. 3의 배수 => total % 3 = 0 <br>
3. 그 외 => -1

```python
total = int(input())
bag = 0

while total % 5: # (1) 가장 큰 5kg 봉지로 담아본다. 5의 배수이면 while문을 빠져나간다.
    total -= 3 # (1) 5의 배수가 아니므로 3kg 봉지로 담아본다.
    bag += 1 # (2)3kg의 한 봉지만큼 증가
print(-1 if total<0 else total % 5 + bag)
# (3) total에 3을 계속 빼서 음수가 되면 조합이 되지 않으므로 -1 출력
# 그렇지 않다면 5kg 봉지 수 + 3kg 봉지 수 출력
```

#### 관련글
- [Python 백준 알고리즘 1단계 - 입/출력 받아보기](https://jihyun-dev.github.io/2019-06-19-python-algorithm-1)

#### **Reference**
- Baekjoon Online Judge: https://www.acmicpc.net
