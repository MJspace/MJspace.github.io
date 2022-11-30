# 프로젝트를 Build한 과정
## MJspace blog 접속 사진

<[![screenshot](/img/screenshot.png)](https://MJspace.github.io/)


### 블로그 구현을 위한 세팅
- git bash 설치
- Jekyll 설치
- Disqus 가입

## 1.Repository 생성
- 깃허브에서 MJspace.github.io 이름의 repo 생성

## 2.Local-Remote Repository 연동
- 1에서 생성한 repository의 주소를 복사 후 clone 한다.
```
 git clone https://github.com/MJspace/MJspace.github.io.git blog
```
## 3.문서 작성 후 커밋
- 마크다운 파일을 작성 후 git status로 현재 상태 확인 후 git add로 변경파일 추가
```
git commit -m "change"
```
## 4.git push로 원격 저장소에 반영
- git branch -M main으로 현재 branch 이름 main으로 변경
- git status로 현재 상태 파악 후 git add로 변경파일 추가
- git push origin main으로 main에 로컬 변경사항 push

## 5.Jekyll 사이트 생성
- 현재 디렉토리에 Jekyll을 설치 후 bundle exec jekyll serve 실행 
- 바꾸고 싶은 기본 값->_config.yml파일에서 바꾼 후 commit 후 push

## 6.포스트
- _posts 폴더에서 포스팅 진행
- 깃, 깃허브, 마크다운 등 공부한 내용 쓰고자 새로운 문서 생성 후 commit과 push

## 7. 사이트 테마 변경
- Lanyon 테마 적용할 예정
- 테마를 git clone해서 로컬을 받아옴
- 변경된 파일을 git에 반영

## 8.댓글 기능
- Disqus 세팅
- _config.yml에 'disqus'와 'MJspace'라는 key-value 값 추가
- _layouts를 페이지에 맞게 수정
- 댓글 허용하고 싶은 문서에 comments: True로 지정

## 9.Google analythics
1. 가입 및 계정 생성
 - google anlytics 사이트에 접속하여 계정 생성 및 설정
 - 속성 이름 설정 시 자신이 사용하는 블로그 주소를 입력해야 함

2. 측정 ID
- 웹 스트림 세부정보에 나오는 측정 ID를 복사해 놓음

3. GitBlog 설정
- _config.yml 파일을 수정하는데 이때 provider에는 "google-gtag"를 입력해주고, tracking_id에는 복사해 놓은 추적 ID를 입력해 줌
- _includes>google-analytics.html 파일에 아래 코드를 추가하여 줌

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-250352818-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-250352818-1');
</script>
```

## 10.파비콘 설정
- 원하는 이미지 파일 다운
- https://realfavicongenerator.net/ 에서 사진 압축폴더 변형 후 다운로드 한 후 assets>favicon.ico 폴더에 사진 정리
- Generate your Favicons and HTML code 버튼을 눌러 얻은 코드를  github.io 폴더 > _includes 폴더 > head.html에 수정
