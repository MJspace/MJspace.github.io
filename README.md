# 프로젝트를 Build한 과정

### 블로그 구현을 위한 세팅
-git bash 설치
-Jekyll 설치
-Disqus 가입

## 1.Repository 생성
- 깃허브에서 MJspace.github.io 이름의 repo 생성

## 2.Local-Remote Repository 연동
- 1에서 생성한 repository의 주소를 복사 후 clone 한다.
-> git clone https://github.com/MJspace/MJspace.github.io.git blog

## 3.문서 작성 후 커밋
- 마크다운 파일을 작성 후 git status로 현재 상태 확인 후 git add로 변경파일 추가
-git commit -m "change"

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
- _config.yml에 'disqus'와 'super-corini'라는 key-value 값 추가
- _layouts를 페이지에 맞게 수정
- 댓글 허용하고 싶은 문서에 comments: True로 지정
