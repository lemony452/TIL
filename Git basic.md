# GIT 기본

**README.md**

-  프로젝트 설명 문서
-  github 
-  sw 함께 배포
- 마크다운을 이용해 작성
- 관통 pjt 할때 쓰기

---

**REPOSITORY(REPO)**

- 특정 디렉토리 버전 관리하는 저장소
- git init  명령어로 로컬(현재 사용중인 컴퓨터) 저장소를 생성
- .git 디렉토리에 버전 관리에 필요한 모든 것


---
**COMMIT**

3개의 영역(working directory - > staging area - > repository)을 바탕으로 동작


1. WORKING DIRECTORY

    : 내가 작업하고 있는 실제 디렉토리

2. STAGIGNG AREA

    : 관리하고 싶은 특정 파일만 버전으로 관리하는 곳

3. REPOSITORY
   
    : 커밋들이 저장되는 곳

​	*단계* 1 ) git add : untracked 파일 - > staged 파일

​	*단계* 2 ) git commit : staged 파일 - > committed 파일

​	*단계* 3 ) 수정 : committed 파일 - > modified 파일 

---

VIM

1. command mode

2. edit mode : instert 누르기

   저장한뒤 나오기 : esc - > :wq

---
**GIT** **명령어**

git status : git의 현재 상태를 확인하는 명령어

git log --oneline : 한줄로 git history  보기

git diff : 두 commit의 차이



- git과 local repo의 연결 : git remote add "레포별명" "레포주소"  = > git remote origin [remote repo주소]
- 현재 등록된 git repo 확인 : git remote -v 

- local에서 git 으로 업로드 : git push "레포별명" "브랜치명" = > git push origin master

- git에서 local로 다운 : git pull origin master (git repo에 있는 버전과 동일한 버전으로 다운, .git폴더가 있어야 하고 remote 주소 정보가 있어야 함)

- github repo를 local로 복제 : git clone github주소 (.git 파일과  remote 주소도 같이 복제됨)

> clone과 pull 의 차이점 정리하기!!

git repo 삭제 : setting - delete this repo

 *git commit 싸이클 순서 : pull -> 공부 -> add -> commit -> push
*

---

**TIL**

git remote add origin [remote repo주소]

git push origin master

git pull orgin master

git clone

# README 파일
반드시 대문자로 작성!!

# 이미지
![레모니 이미지](./img/lemony.jpg)