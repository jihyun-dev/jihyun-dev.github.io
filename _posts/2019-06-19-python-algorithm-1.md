---
layout: post
title: '[Python] 백준 알고리즘 1단계 - 입출력과 사칙연산'
date: 2019-06-19
update: 2019-06-19
author: Jihyun
cover: '/assets/img/2019-06-18-python-algorithm-cover.png'
tags: Python Algorithm
---


> 백준 단계별 풀이 - 1단계(입출력과 사칙연산) 문제를 풀이한다.


## 1단계 입출력과 사칙연산

### 2557. Hello World! 출력
```python
print("Hello World!") #This is comment line.
```

### 1000. 두 정수를 입력받아 A+B 출력
```python
# 입력: 1 2
# 출력: 3
a, b = map(int, input().split())
print(a+b)
```
* 입력값이 한줄, 각각 따로 저장해야함
<br> => 입력받은 문자열을 공백 기준으로 나누는 **split()** 을 사용하여 각 변수 a, b에 저장한다.
* input()을 통해 입력받은 값은 따로 데이터 타입을 평가하지 않고, "1", "2"의 문자로 저장된다.
<br> => 따라서 내장함수 **map(f, iterable)** 을 사용하여 정수로 변환한다. (f: 함수)


### 10172. 개 그림 출력
```python
print('|\_/|')
print('|q p|   /}')
print('( 0 )\"\"\"\\')
print('|\"^\"`    |')
print('||_/=\\\\__|')
```
* 따옴표("): \" (따옴표 앞에 역슬래시 추가)
* 역슬래시(\\): \\\\ (역슬래시 앞에 역슬래시 추가)

### 10718. 주어진 문자를 반복하여 출력
```python
# 출력: 강한친구 대한육군
#      강한친구 대한육군
for n in range(2): # 0부터 1까지, 총 2번 반복
    print("강한친구 대한육군")
```

### 11718. 입력받은 그대로 출력하기(1)
```python
# 입력: (공백 미포함)
#      Hello
#      Baekjoon
#      Online Judge
#출력: Hello
#      Baekjoon
#      Online Judge
while True:
    try:
        print(input())
    except EOFError:
        break
```
* 입력 받은 값을 **한 줄씩 입/출력** 하다가, EOF에러가 발생하면 종료한다.
<br> => 시간: 64ms


### 11719. 입력받은 그대로 출력하기(2)
```python
# 입력: (공백 포함)
#      Hello
#      
#      Online Judge
#출력:  Hello
#      
#      Online Judge
import sys

str = sys.stdin.read()
sys.stdout.write(str)
```
* input()은 한 줄만 입력받음
<br> => 외장함수 **sys**의 **read**(표준 입력 스트림) EOF까지 모두 읽음, 여러 줄을 입력받을 수 있다.
* **write**(표준 출력 스트림)
<br> => 시간: 56ms

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
#### 관련글
- [Python 백준 알고리즘 2단계 - 사칙연산](https://jihyun-dev.github.io/2019/06/20/python-algorithm-2.html)
- [Python 백준 알고리즘 3단계 - 입/출력 받아보기](https://jihyun-dev.github.io/2019/06/21/python-algorithm-3.html)

#### **Reference**
- Baekjoon Online Judge: https://www.acmicpc.net
