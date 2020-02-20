---
title:  "Github 사용하기"
excerpt: "Github 사용하기"

categories:
  - Github
tags:
  - Github.git
last_modified_at: 2020-01-30T08:06:00-05:00
---

##목차

- Github 용어
- Github 사용법
- Git 명령어 정리
#
#
#



#### Github 용어

######1. Local repository, Remote repository

repository(저장소)는 파일이나 디렉토리 등을 저장하는 장소 입니다. 

Local repository : 자신의 컴퓨터 (하드웨어)
Remote repository : 서버 네트워크에 있는 원격 저장소

#
#

######2. Commit, Push, Pull, Clone, branch

Commit 

파일을 변경 하거나 추가 삭제 했던 변경 내용을 기록하는 작업

Push

파일을 변경 하거나 추가 삭제 했던 내용을 저장하는 작업

Pull

Remote에 저장된 파일을 Local로 가져오는 것(Github ID/Password 필요)

Clone

Pull과 비슷하지만 클라이언트 상에 아무것도 없을 때 원격에 있는 프로젝트를 내려받을 때  사용 (저장소의 내용을 다운로드 받고 자동으로 init도 된다.)

branch

한 프로젝트를 기본 베이스로 여러 사람이 협업 할 때 사용한다. 기본적으로 master  branch가 있으며 master에서 여러 갈래로 나뉘어 질 수 있다. A 버전이 있으면 A-1, A-2, A-3 등 여러 버전을 동시에 작업 할 수 있게 해준다.

#
#
#
#
#
#


####Github 사용법

- 프로젝트 폴더 생성
- git init
- github에서 new repository 생성
- git remote add origin new repository url
- git add .
- git commit -m "initial Commit."
- git push origin master

#
#
#
#
####Git 명령어 정리 


git init : git 생성하기
git clone git_path : 코드가져오기
git checkout branch_name : 브랜치 선택하기
git checkout -t remote_path/branch_name : 원격 브랜치 선택하기
git branch branch_name : 브랜치 생성하기
git branch -r : 원격 브랜치 목록보기
git branch -a : 로컬 브랜치 목록보기
git branch -m branch_name change_branch_name : 브랜치 이름 바꾸기
git branch -d branch_name : 브랜치 삭제하기
git push remote_name — delete branch_name : 원격 브랜치 삭제하기 ( git push origin — delete gh-pages )
git add file_path : 수정한 코드 선택하기 ( git add * )
git commit -m “commit_description” : 선택한 코드 설명 적기 ( git commit -m “내용”)
git push romote_name branch_name : add하고 commit한 코드 git server에 보내기 (git push origin master)
git pull : git서버에서 최신 코드 받아와 merge 하기
git fetch : git서버에서 최신 코드 받아오기
git reset — hard HEAD^ : commit한 이전 코드 취소하기
git reset — soft HEAD^ : 코드는 살리고 commit만 취소하기
git reset — merge : merge 취소하기
git reset — hard HEAD && git pull : git 코드 강제로 모두 받아오기
git config — global user.name “user_name ” : git 계정Name 변경하기
git config — global user.email “user_email” : git 계정Mail변경하기
git stash / git stash save “description” : 작업코드 임시저장하고 브랜치 바꾸기
git stash pop : 마지막으로 임시저장한 작업코드 가져오기
git branch — set-upstream-to=remote_path/branch_name : git pull no tracking info 에러해결