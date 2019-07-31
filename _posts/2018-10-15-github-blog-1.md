---
layout: post
title: '[GitHub] 깃헙 블로그 만들기 1 - GitHub Pages, Jekyll 개념'
date: 2018-10-15
author: Jihyun
cover: '/assets/img/2018-10-15-github-blog-1-cover.png'
tags: Jekyll Github Web
---

<center> GitHub Pages와 Jekyll의 기본에 대해 알아보자</center><br><br>

# **1. GitHub Pages**  
---
### * [Github Pages](https://pages.github.com)란?
 Github에서 무료로 제공하는 **웹 호스팅 서비스**

#### * **Web Hosting**
웹 서비스 구축에 필요한 서버 공간을 빌려주는 서비스 이다. 웹 호스팅 서비스를 이용하지 않는다면 서버 구축, 전용 회선 임대 등을 직접해야 한다.
<br>
<br>


# **2. Jekyll**
---
### * [Jekyll](https://jekyllrb.com)이란?
지킬 또한 Github에서 개발한 **정적 웹사이트 생성기** 이다. 또 다른 툴로는 대표적으로 워드프레스가 있다. 지킬은 HTML, Markdown 등으로 작성된 텍스트를 미리 정해놓은 규칙에 따라 **정적 웹사이트** 로 변환시켜준다. 정적 및 동적 웹사이트에 대한 개념은 [링크된 글](https://jihyun-ella.github.io/2018/10/16/static-dynamic-websites.html)에서 확인할 수 있다.

#### * Jekyll 설치
jekyll은 ruby로 작성된 사이트 생성기이다. 따라서, jekyll을 사용하기 위해서는 ruby도 설치되어 있어야 한다. 아래와 같이 터미널에 명령어를 입력하여 ruby와 jekyll을 설치할 수 있다.
```bash
brew install ruby // 맥의 경우, 시스템 루비가 기본적으로 설치되어 있음
gem install jekyll // 루비의 gem 패키지 인스톨러를 통해 지킬 설치
```
<br><br>

---
#### 관련글
- [GitHub 블로그 만들기 2 - Jekyll 테마 가져오기](https://jihyun-dev.github.io/2018/10/19/github-blog-2.html)

#### **Reference**
- Github Page: https://pages.github.com  
- Jekyll: https://jekyllrb.com
- Web Hosting: https://opentutorials.org/course/3084/18891
