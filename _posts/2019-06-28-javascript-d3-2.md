---
layout: post
title: '[Javascript] D3.js - 2. Multi-Line Chart'
date: 2019-06-28
author: Jihyun
cover: '/assets/img/2019-06-27-d3-cover.png'
tags: Javascript D3.js
---

<center> D3.js을 이용해 Multi-Line Chart를 그려보자 </center><br><br>

<!-- # **1. Select**  
---
#### * ** selection 이란?**
한 개 이상의 문서요소(div, h1, p, span 등)를 선택하는 함수
#### * ** select 종류**
D3.js는 select(), selectAll()의 두 함수를 지원한다. -->

---
### 1) node, npm, bower 설치
**D3을 설치** 하려면 bower이 필요하다. 그리고 bower을 사용하려면 node와 npm이 필요하다.
* **node 및 npm 설치**
```bash
brew install node
```
설치가 완료되면 다운된 버전을 확인한다. (나의 경우는 12.4.0)
```bash
cd ~
vi .bash_profile
```
.bash_profile 파일에 아래의 내용을 붙여넣기한다.
```bash
export NODE_PATH="/usr/local/lib/node_modules"
export PATH="/usr/local/Cellar/node/노드버전/bin:$PATH"
```
노드 버전은 위에서 확인한 버전(나의 경우는 12.4.0)을 쓰면 된다. 그 후 esc -> :wq 입력하여 저장하고, 터미널을 재시작한다.
```bash
node -v
npm -v
```
위의 명령어로 설치를 확인한다.
![settings-npm](/assets/img/2019-06-28-javascript-d3-settings-npm.png)

* **bower 설치**
```bash
npm install -g bower
```
![settings-bower](/assets/img/2019-06-28-javascript-d3-settings-bower.png)

### 2) D3 설치
```bash
bower install d3 --save
```
![settings-bower](/assets/img/2019-06-28-javascript-d3-install-d3.png)


# **3. D3.js 예제**
설치가 잘 되었나 간단한 예제를 통해 확인한다.
```HTML
<script type = "text/javascript" src = "https://d3js.org/d3.v4.min.js"></script>
```
d3을 로드해준다.
```HTML
   <body>
      <div>
         Hello World!    
      </div>

      <script>
         alert(d3.select("div").text());
      </script>
   </body>
```
![settings-bower](/assets/img/2019-06-28-javascript-d3-example-d3.png)
위와 같은 알림창이 뜬다면 잘 작동하는 것이다!


---
<!-- #### 관련글
- [GitHub 블로그 만들기 2 - Jekyll 테마 가져오기](https://jihyun-dev.github.io/2018/10/19/github-blog-2.html) -->

#### **Reference**
- D3.js 시작하기: http://webframeworks.kr/getstarted/d3js/
- tutorialspoint: https://www.tutorialspoint.com/d3js/
