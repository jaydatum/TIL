# TIL day 3

# Git, Github 특강 3일차

## 1. Branch

> Branch : git 버전 관리의 핵심

### 1.1 Branch란?

![branch](../images/TIL day 3/branch-16432992470501.png)

- 여러 갈래로 작업 공간을 나누어 **<u>독립적으로 작업</u>**할 수 있는 Git의 도구 
- 장점
  1.  브랜치는 독립공간이므로 원본(master)에 대해 안전함
  2.  하나의 작업이 곧 하나의 브랜치이므로 체계적인 개발 가능
  3. Git은 브랜치를 만드는 속도가 빠르고 용량이 적게든다.

### 1.2 git branch

> 브랜치 조회, 생성, 삭제 등의 명령어

```bash
# 브랜치 목록 확인
$ git branch

# 원격 저장소의 브랜치 목록 확인
$ git branch -r

# 새로운 브랜치 생성
$ git branch <브랜치 이름>

# 특정 커밋 기준으로 브랜치 생성
$ git branch <브랜치 이름> <커밋 ID>

# 특정 브랜치 삭제
$ git branch -d <브랜치 이름> # 병합된 브랜치만 삭제 가능
$ git branch -D <브랜치 이름> # (주의) 강제 삭제 (병합되지 않은 브랜치도 삭제 가능)
```

### 1.3 git switch

> 브랜치 전환 명령어

```bash
# 다른 브랜치로 이동
$ git switch <다른 브랜치 이름>

# 브랜치를 새로 생성과 동시에 이동
$ git switch -c <브랜치 이름>

# 특정 커밋 기준으로 브랜치 생성과 동시에 이동
$ git switch -c <브랜치 이름> <커밋 ID>
```



## 2. Branch Merge

> 브랜치 작업내용 master에 반영

### 2.1 git merge

- 분기된 브랜치들을 하나로 합침
- `git merge <합칠 브랜치 이름>` 의 형태로 사용
- <u>**메인 브랜치로 switch한 뒤 merge 해야 한다.**</u>

```bash
# 1. 현재 branch1과 branch2가 있고, HEAD가 가리키는 곳은 branch1 입니다.
$ git branch
* branch1
  branch2

# 2. branch2를 branch1에 합치려면?
$ git merge branch2

# 3. branch1을 branch2에 합치려면?
$ git switch branch2
$ git merge branch1
```



### 2.2 Merge Conflict

-  merge하는 두 브랜치에서 `같은 파일의 같은 부분`을 수정한 경우 충돌(conflict) 발생
- 사용자가 직접 내용을 선택해서 conflict 해결

![merge_conflict2](../images/TIL day 3/merge_conflict2-16433263151972.png)![img](../images/TIL day 3/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fb31206af-b48f-4193-8b5f-f9c068f8c0be%2F.png)

## 3. Pull Request : 실제 협업 시 (Pull only)

![pull_request](../images/TIL day 3/pull_request-16433265051173.png)



## 코드 모음

```bash
# add한 파일 삭제
$ git rm --cached a.txt

# 이전 버전으로 되돌리기
$ git restore --staged a.txt

# 두 버전의 수정사항 확인하기
$ git diff 해쉬값1 해쉬값2

# 직전 커밋 메시지 수정
$ git commit --amend

# 커밋 관련 로그 확인
$ git reflog
```



## reset : 협업 시 쓰지 않는다

- hard : 작업물 / 커밋 모두 지운다 (시간역행)
- mixed : add 전 단계까지 날림 / 커밋 날림
- soft : add까지는 되어 있는 상태 / 커밋 날림