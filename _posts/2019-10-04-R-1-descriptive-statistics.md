---
layout: post
title: '[R] 1. 기술통계(Descriptive Statistics) - summary, boxplot, pairs'
date: 2019-10-04
author: Jihyun
cover: '/assets/img/2019-10-04-R-cover.png'
tags: Data Statistic R
---

<center> R을 본격적으로 학습하기 전에, 기술 통계에 관한 기초적인 분석을 한다. </center><br><br>


### R 시작하기
R을 설치하고 나면, dataset이라는 패키지가 기본으로 설치된다. 여기에는 'trees, chickwts, cars, mtcars, iris' 등의 데이터가 기본적으로 내장되어있다.<br>
데이터의 이름을 입력하면 해당 데이터의 변수들을 볼 수 있다.

```bash
>> trees
>> chickwts
>> cars
```

![basic-of-R](/assets/img/2019-10-04-trees.png)
이것들을 사용하여 가장 기초적인 데이터 분석을 실습해보자.



### 기술통계(Description Statistic)
##### **1) summary()**

summary()를 사용하면 speed, dist 각 변수에 대한 기술통계(Description Statistic)를 보여준다.

```bash
>> summary(trees)
```
![stat-summary](/assets/img/2019-10-04-stat-summary.png)

* Min. : 최소값
- 1st Qu. : 1 사분위수(Quartile), Min과 Median 중앙값, 오름차순으로 정렬했을 때 하위 25%의 값
- Median: 중앙값(중위수, 정렬했을 때 가장 중앙에 위치하는 값)
- 3rd Qu.: 3 사분위수, Median과 Max의 중앙값, 오름차순으로 정렬했을 때 상위 25%의 값
- Max. : 최대값


#### **2) boxplot()**
boxplot()을 사용하면 박스 그림을 통해 데이터의 분포를 보다 쉽게 나타낼 수 있다.
```bash
>> boxplot(trees)
```
![stat-boxplot](/assets/img/2019-10-04-stat-boxplot.png)


#### **3) pairs()**
pairs를 사용하면 산점도(Scatter, 데이터들이 얼마나 퍼져있는 지)를 쉽게 나타낼 수 있다.
```bash
>> pairs(cars)
```
![stat-pairs](/assets/img/2019-10-04-stat-pairs.png)
