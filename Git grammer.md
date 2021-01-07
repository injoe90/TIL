# Git

> DVCS, 분산 버전 관리 시스템

##  원격 저장소 설정

```bash
$ git init
Initialized empty Git repository in C:/Users/hand1/OneDrive/바탕 화면/md/.git/
(master) $
```

* .git 숨김 폴더가 생성된다.
* (master) 브랜치 표기



## 기본 흐름

> 어떠한 작업 => $ touch 파일명

```bash
$ git status
On branch master

No commits yet
# 트래킹이 없는 파일들
# 버전에 기록된 적이 없는 파일들
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        1.txt
# 커밋을 할 파일이 없다. => SA X
# 그러나 untracked file는 있다. => WD O
nothing added to commit but untracked files present (use "git add" to track)
```



> add

```bash
$ git add . # 현재 디렉토리(하위까지)
$ git add a.txt # 특정 파일
$ git add test/ # 특정 폴더

On branch master

No commits yet
# 커밋이 될 변경사항들 (SA O)
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   1.txt
```



## commit

> 스냅샷, 버전을 새롭게 만듦

```bash
$ git commit -m '커밋메시지'
[master (root-commit) 4c2a783] Add 1.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1.txt

```

* 해시 값이 고유한 커밋을 의미한다
  * 4c2a7837a9ed92b8449d4b13db8855fc33aadf80
* 커밋 메시지는 반드시 현재 작업 내용을 나타낼 수 있도록 잘 작성하는 것이 중요하다.



## 기타 상태 명령어

> status

```bush
$ git status
```



> 커밋 히스토리(log)

```bash
$ git log # 한 줄로 간략히
$ git log -1 --online # 최근 2개의 커밋을 한 줄로
$ git log -2 # 최근 2개의 커밋
```



> github 저장소 설정

```bash
$ git status
$ git remote add origin https://github.com/injoe90/first.git
$ git push origin master
```

