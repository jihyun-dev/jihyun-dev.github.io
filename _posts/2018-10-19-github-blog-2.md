---
layout: post
title: 'GitHub 블로그 만들기 2 - Jekyll 테마 가져오기'
date: 2018-10-19
author: Jihyun
cover: '/assets/img/2018-10-15-github-blog-1-cover.png'
tags: Jekyll Github Web
---
<center> Jekyll 테마를 사용하여 GitHub Page 블로그를 만들어보자 </center><br><br>

# **1. Jekyll 테마 가져오기**  
---
### 1) 지킬 테마사이트(http://jekyllthemes.org) 에서 원하는 테마를 선택한다.
![지킬 테마사이트 메인](/assets/img/2018-10-19-github-blog-2-jekyll-main.png)
<center> 해당 테마의 Demo를 통해 확인해볼 수 있다.</center>
![지킬 테마 데모사이트2](/assets/img/2018-10-19-github-blog-2-jekyll-demo.png)

### 2) 선택한 테마를 나의 GitHub repository(저장소)에 가져온다.
Homepage를 클릭하면, 해당 테마의 저장소로 이동할 수 있다.
![지킬 테마 가져오기1](/assets/img/2018-10-19-github-blog-2-jekyll-theme1.png)
해당 테마의 저장소를 Fork하여, 나의 저장소로 가져온다.
![지킬 테마 가져오기2](/assets/img/2018-10-19-github-blog-2-jekyll-theme2.png)
테마가 나의 GitHub repository로 옮겨진 것을 확인할 수 있다.
![](/assets/img/2018-10-19-github-blog-2-jekyll-theme2.png)
저장소 이름 아래 쪽 setting을 클릭한다.

### 3) 나의 repository 이름을 변경한다.
**주의** GitHub ID와 repository 이름을 **같게 설정** 해야 한다.
![repository 이름 변경](/assets/img/2018-10-19-github-blog-2-jekyll-repo-name.png)

### 4) ID.github.io 로 접속해본다.
데모사이트와 같은 코드를 그대로 가져왔지만, 나의 블로그 URL에서는 404 에러가 발생한다.
![404에러](/assets/img/2018-10-19-github-blog-2-jekyll-404.png)
➡︎ 원인: 테마의 코드 속 **URL이 나의 블로그 주소(ID.github.io)와 일치하지 않아서 발생** 한 것이다. <br>
➡︎ 해결: URL과 관련된 해당 라인을 수정하면 간단하게 해결할 수 있다.
<br><br>

# **2. GitHub repository와 로컬 저장소 연결하기**

테마 소스 코드를 수정하려면, GitHub repository와 나의 로컬 저장소를 연결해야 한다.

---
### 1) 터미널에서 repository clone
원하는 위치에 디렉토리를 만들고, 그 곳에 repository를 clone한다.
```bash
> mkdir 로컬저장소_이름
> cd 로컬저장소_이름
> git clone 레포지토리_주소
```

참고) repository 주소는 아래에서 복사해온다.
![reposity 주소 복사](/assets/img/2018-10-19-github-blog-2-jekyll-repo-url.png
)

내 로컬 저장소(myblog)에 레포지토리(jihyun-ella.github.io)가 연결된 것 확인할 수 있다.
![clone 결과](/assets/img/2018-10-19-github-blog-2-jekyll-repo-clone.png)

### 2) URL 등 설정 바꾸기
config.yml, index.html 등 로컬에서 설정 코드를 바꿔준다.
![기타 설정 바꾸기](/assets/img/2018-10-19-github-blog-2-jekyll-settings.png)

로컬에서 수정한 코드를 저장하고, GitHub repository로 commit과 push를 해준다.
```bash
git add .
git commit -m "커밋 내용"
git push -u
```
![](/assets/img/2018-10-19-github-blog-2-commit.png)

push가 완료되면, 블로그 url 및 기타 설정한 부분이 바뀐 것을 확인할 수 있다.
![정상 작동하는 블로그](/assets/img/README-img.png)

---

#### 관련글
- [GitHub 블로그 만들기 1 - GitHub Pages, Jekyll 개념](https://jihyun-ella.github.io/2018/10/15/github-blog-1.html)

#### **Reference**
- Jekyll: https://jekyllrb.com
