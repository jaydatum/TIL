# TIL day 1



# Git, Github 특강 1일차



## 1. What/why Git&Github

> 공부한 내용을 정리하여 포트폴리오로 활용할 수 있고 실제 업무 시에 버전관리를 위해 반드시 사용하는 협업을 위한 도구

- Git을 이용한 버전 관리
  - Git : (분산) 버전 관리 프로그램 / Github : 서비스
  - 버전 관리 : 소프트웨어의 특정 상태를 관리하는 것 → 실무에서의 협업 tool
- 포트폴리오 작성
  - 오늘부터 TIL과 잔디심기!!  (티스토리에서 이사가야 되나..)

## 2. CLI 기초

> Git Bash로 Linux 명령어를 위한 CLI 실습 

- CLI (Command Line Interface) : 터미널을 통해 사용자와 컴퓨터가 상호작용하는 방식 ex) cmd
- GUI (Graphic User Interface) : 그래픽을 통해 사용자와 컴퓨터가 상호작용하는 방식
- Interface : 사용자가 컴퓨터와 서로 소통하는 접점

## 3. Git Bash

> Bash는 명령어 입력전 항상 어디서 열었는지 반드시 체크할 것!

### 3.1 git bash의 사용 이유

- 명령어의 통일 : windows에서도 UNIX 계열 운영체계 터미널 명령어 사용할 수 있음
- 개발시에는 UNIX계열 명령어를 더 많이 쓰기 때문이다.

### 3.2 Git bash 구동

- 윈도우 탐색기에서 C:/사용자(Users)/현재 사용자 계정 로 이동
- C:/사용자(Users)/현재 사용자 계정 로 이동
- Git Bash 창에 아래 화면처럼 HOME 폴더를 의미하는 ~ 표시만 있다면 정상 (홈폴더)

1. 루트 디렉토리 (Root directory, /)
   - 모든 파일과 폴더를 담고 있는 최상위 폴더 → 보통 c 드라이브
2.  홈 디렉토리 (Home directory, ~)
   - Tilde 라고 하며 현재 로그인 사용자 홈 폴더 의미 → 보통 C:/사용자(Users)/현재 사용자 계정 

## 4. Git Bash 명령어 정리

1. start . open . 폴더/파일을 여는 명령어
   - 상대경로 : 내 위치 기준 / 절대경로 : 루트 디렉토리 부터 모든 경로 작성
2. date : 시간 알려줌
3. ls (list segments) : 현재 디렉토리 내의 폴더& 파일 보여줌
   - ls -a : all 숨김 폴더& 파일까지 보여줌
4. ctrl + i : 스크롤 내리기 (내역은 남아있음)
5. clear :  모든 창 클리어
6. 배쉬 창 화살표 키 : 최근 기입 확인
7. ctrl a,e : 앞, 뒤 이동
8. touch : 파일 만들기 a.txt
9. mkdir : 폴더 만들기
10.  cd (change diretory)
    - . 현재위치
    - .. 현재위치에서 상대경로로 상위 디렉토리 이동
11. ctrl + insert : 복사
12. ctrl + insert : 붙여넣기
13. mv : 이동(이미 있는 거) + 이름 바꾸기 (없는 거)
14. rm : remove
    - 파일 삭제 : rm a.txt
    - 폴더 삭제 : rm -r test

> '*' : asterisk, wildcard : all
>
> 절대 rm -rf* 홈 디렉토리에서 입력하지 말것!! (대참사....)



## 5. 마크다운(markdown) 문법 정리

> notion, github 사용 시 용이하게 사용될 수 있음 : 공부 더 해보자!!

1. '#' : 문서의 논리적 흐름 대제목, 소제목
   - 주의 : 글씨 크기를 키우기 위해 사용하지 않는다
2. 인용문 : '>' 꺽쇠
3. 리스트 : * or - tab으로 안으로 간다. shit tab 밖으로 나온다
4. 이미지 : '![]()'
5. 링크 : '[]()[보여질제목](실제링크)'
6. 수평선 : '---'
7. 표 만들기 : 파이프 스페이스, 파이프 스페이스, 파이프 엔터



## 6. Git 명령어 정리

1. git init
   - 현재 폴더를 git이 관리하는 폴더로 만들어줘
   - 홈 폴더에서는 기입하지 않는다! (홈폴더 안의 모든 폴더를 git이 관리하게 되므로)
   - 딱 최초 한 번 만 기입한다.
2. git status : 중간 중간 상태확인
   - 현재 상황을 보고 싶어! : Untracked / Modified / Working tree clean
3. git add a.txt (특정 파일) / git add . (전부 다올리기)
4. git commit -m '메시지' : 찰칵! 후 저장소로 간다
   - 컨벤션(convention) : 메시지를 작성하는 일종의 규약!! → 협업 시 중요!!
   - ex ) numpy/bugfix/SO167 , feature/frontend/jira
5. git log : 최종 단계의 버전확인
   - 버전들 확인할래!
