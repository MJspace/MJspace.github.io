---
layout: post
title: "google_analytics"
date:   2022-11-29 16:48:10 +0900
categories: jekyll update
comments: true
---

# Google-analytics
:구글에서 제공하는 웹사이트 트래픽을 추적 보고하는 서비스

 ## 가입 및 계정 생성
 - google anlytics 사이트에 접속하여 계정 생성 및 설정
 - 속성 이름 설정 시 자신이 사용하는 블로그 주소를 입력해야 함
 - 그 외 설정은 자유롭게 자신의 기호에 따라 설정해주면 됨
 - 약관에 동의하고 설정 완료

## 측정 ID
- 웹 스트림 세부정보에 나오는 측정 ID를 복사해 놓는다.


## GitBlog 설정
- _config.yml 파일을 수정하는데 이때 provider에는 "google-gtag"를 입력해주고, measurement_id에는 복사해 놓은 추적 ID를 입력해 줌
- _includes>head.html 파일에 아래 코드를 추가하여 줌


```html
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id={{ site.google_analytics }}"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', '{{ site.google_analytics }}');
    gtag('config', G-8MDJ2LV3WK);
</script>
```