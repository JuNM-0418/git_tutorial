# GitHub

## 기본적인 용어

커밋(commit)

파일을 추가하거나 변경 내용을 저장소에 저장하는 작업



푸시(push)

파일을 추가하거나 변경 내용을 원격 저장소에 업로드하는 작업



로컬 저장소

기본적으로 로컬 저장소에서 작업을 수행



원격 저장소

로컬 저장소에서 수행한 작업의 결과를 원격 저장소에 저장한다.



브랜치(branch)

SW 개발을 하면서 새로운 기능 추가 및 버그 수정을 하면서

이러한 병렬로 수행되는 여러 버전 관리를 위해 브래치라는 기능을 사용한다.



## GitHub 사용법

GitHub에 저장소 작성(git init) 또는 복제(git clone)

파일의 작성, 편집

파일의 생성, 변경, 삭제를 git 인덱스에 추가 (git add)

변경 결과를 로컬 저장소에 커밋(git commit)

로컬 저장소를 푸쉬해 원격 저장소에 반영(git push)



```
# git 저장소를 새로 만드는 명령
git init

# git 원격 저장소에 반영하기 전에 원격 저장소의 정보를 추가
git remote add origin https://github.com/JuNM-0418/git_tutorial

# 파일 추가하기
git add .

# 파일 이름 직접 입력
git add helloworld.java

# 파일이나 디렉토르의 추가 또는 변경을 저장소에 기록하는 작업.
git commit -m "first_commit"

# 로컬 저정소의 변경 사항을 원격 저장소에 반영하기 위해 실행하는 명령
git push origin master
```



## 브랜치(branch)

브랜치의 생성, 이동

브랜치에서의 개발 작업

브랜치에 푸시

브랜치에서 풀

브랜치 병합

브랜치 삭제



```
# 브랜치 목록 확인, 현재 브랜치에 *이 붙는다.
git branch

# 브랜치 생성
git branch subdir01

# 지점 이동
git checkout subdir01

# 브랜치 생성과 지점 이동을 동시에 한다
git checkout -b subdir01

# 작업 이후, 브랜치 푸시
git add hello.py
git commit -m "add file hello"

# subdir01에 푸시, 이후 확인하면 subdir01에만 hello.py가 있는 것을 확인할 수 있다.
git push origin subdir01

# 브랜치 풀


# 브랜치 병합(메인 master로 subdir01을 병합하는 방법)
git checkout master
git merge subdir01
git push origin master

# 브랜치 삭제
git branch -d subdir01
```



## 자주 사용하는 명령어

```
# 저장소의 상태를 확인, 현재 브랜치의 이름과 추가, 변경된 파일 및 디렉토리 목록을 표시
git status

# 파일이나 디렉토리를 인덱스에 추가하는데 사용
git add

# 인덱스에 추가 된 파일이나 폴더의 내용을 저장소에 쓸 때 사용하는 명령어
git commit

# 브랜치에 대해 다양한 작업을 수행하기 위해 사용하는 명령어.
git branch

# 브랜치를 삭제하는 명령어
git branch -d

# 브랜치를 전환 할 때 사용하는 명령어
git checkout

# 브랜치 추가와 전환을 동시에 하는 명령어
git checkout -b

# 로컬 저장소의 커밋 히스토리를 탐색하는 데 사용하는 명령
git log

# 저장소의 파일 내용에서 검색하고자 할 때 사용하는 명령어
git grep "검색 단어"

# 기존 원격 저장소를 로컬에 다운로드하기 위하여 사용하는 명령어.
git clone 주소

# 원격 저장소를 조작하는 데 사용하는 명령으로 아래와 같이 사용
# 원격 저장소의 이름 목록을 표시
git remote
# 원격 저장소에 대한 자세한 목록보기
git remote -v
# 원격 저장소를 추가
git remote add 저장소이름 주소
# 원격 저장소를 제거
git remote rm 저장소이름

# 로컬 저장소의 커밋을 취소하기 위하여 사용하는 명령어
git reset

# 현재 브랜치에 다른 지점에서의 변경 사항을 병합하는데 사용하는 명령이다.
git merge
# 분기 bug-fix를 master 브랜치에 병합
git checkout master
git merge bug-fix

# 원격 브랜치의 변경 사항을 캡쳐하기 위해 사용
git pull
# 로컬 저장소의 master 브랜치에 원격 저장소 origin의 master 브랜치를 가져온다.
git checkout master git pull origin master
```

