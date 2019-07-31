---
layout: post
title: '[Python] 백준 알고리즘 3단계 - for문'
date: 2019-06-21
update: 2019-06-21
author: Jihyun
cover: '/assets/img/2019-06-18-python-algorithm-cover.png'
tags: Python Algorithm
---


> 백준 단계별 풀이 - 3단계(for문) 문제를 풀이한다.


## 3단계 for문

### 2741. N찍기
자연수 N이 주어졌을 때, 1부터 N까지 한 줄에 하나씩 출력하는 프로그램
```python
# 입력 : 5
# 출력:  1
#       2
#       3
#       4
#       5
n = int(input())
for i in range(n):
    i += 1
    print(i)
```
```python
n = int(input())
arr = [i for i in range(1, n+1)]
print('\n'.join(map(str, arr)))
```
* '\n'.join(): 문자열, 리스트, 튜플 등의 사이에 '\n'를 삽입한다.

### 2741. 기찍N (거꾸로)
자연수 N이 주어졌을 때, N부터 1까지 한 줄에 하나씩 출력하는 프로그램
```Python
n = int(input())
arr = [i for i in range(n, 0, -1)]
print('\n'.join(map(str, arr)))
```
* for i in range(10, 0, -1)
* for i in reversed(range(1, n+1)


### 2739. 구구단
N을 입력받은 뒤, 구구단 N단을 출력하는 프로그램
```Python
n = int(input())
for i in range(1, 10):
    print(n,'*',i,'=',n*i)
```

### 2438. 별 찍기-1
```Python
n = int(input())
for n in range(1, n+1):
    for i in range(1, n+1):
        print('*', end='')
    print('\n', end='')
```
* end='': print의 매개변수로 넣으면, 개행이 되지 않고 한 줄로 출력한다.

```Python
for i in range(int(input())): print('*'*(i+1))
```

### 2588번. 곱셈
![image](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)
1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램

```Python
n = int(input())
m = input()
arr = [int (i) for i in m]
print(n*arr[2], n*arr[1], n*arr[0], n*arr[2]+n*arr[1]*10+n*arr[0]*100, sep='\n')
```
* 두 번째 자연수(m)를 문자열로 받은 후, 각 자릿수로 인덱싱하였다.

```Python
n = int(input())
m = input()
for _ in m[::-1]:
    print(n * int(_))
print(n*int(m))
```
* m[::-1]: 문자열 리스트 m을 처음부터 끝까지, 반대로 반복한다.
#### 관련글
- [Python 백준 알고리즘 1단계 - 입/출력 받아보기](https://jihyun-dev.github.io/2019/06/19/python-algorithm-1.html)
- [Python 백준 알고리즘 2단계 - 사칙연산](https://jihyun-dev.github.io/2019/06/20/python-algorithm-2.html)

#### **Reference**
- Baekjoon Online Judge: https://www.acmicpc.net
