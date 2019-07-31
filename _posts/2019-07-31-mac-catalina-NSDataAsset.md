---
layout: post
title: '[Mac] Catalina - NSDataAsset 오류 해결기'
date: 2019-06-28
author: Jihyun
cover: '/assets/img/2019-07-31-mac-catalina-NSDataAsset-cover.png'
tags: Javascript D3.js
---

<center> 'NSDataAsset'가 충돌되는 오류 해결방법을 찾는다. </center><br><br>

# **발생한 오류**  
---
![NSDataAsset-msg](/assets/img/2019-07-31-mac-catalina-NSDataAsset-msg.png)
'objc[28993]: Class NSDataAsset is implemented in both /System/Library/PrivateFrameworks/UIFoundation.framework/Versions/A/UIFoundation (0x120faa160) and /System/Library/Frameworks/AppKit.framework/Versions/C/AppKit (0x120099028). One of the two will be used. Which one is undefined.'<br>
장고 프로젝트 실행중에 시스템 라이브러리(?)에서 ’NSDataAsset’이 두 경로에서 서로 충돌된다는 오류가 발생하였다.

---


### Reference
- https://apple.stackexchange.com/questions/364498/library-conflict-in-macos-catalina-uifoundation-vs-appkit  <br>
구글링해보니, 나와 같은 오류에 관한 질문이 올라와있다. 그러나 뾰족한 답변은 없었다.<br>

- https://developer.apple.com/documentation/xcode_release_notes/xcode_11_beta_5_release_notes <br>
xcode 11 beta 5 버전의 릴리즈 노트를 검색해보니, ’NSDataAsset’과 관련된 사항을 찾아볼 수 있었다.

### 해결 방법
![NSDataAsset](/assets/img/2019-07-31-mac-catalina-NSDataAsset.png)
며칠 전 새로운 베타버전(10.15, 19A512f)이 올라와서 업데이트를 하니, 오류가 뜨지 않는다. 해결~!



---
<!-- #### 관련글
- [GitHub 블로그 만들기 2 - Jekyll 테마 가져오기](https://jihyun-dev.github.io/2018/10/19/github-blog-2.html) -->

#### **Reference**
- D3.js 시작하기: http://webframeworks.kr/getstarted/d3js/
- tutorialspoint: https://www.tutorialspoint.com/d3js/
