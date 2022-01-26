# TIL day 2

# Git,Github 특강 2일차

git checkout 해쉬값 : 해쉬값 버전으로 가기

-   git checkout head~3 : 위로부터 세번째 항목으로 가기
-   git checkout master : 체크아웃에서 마스터로 나오기

git remote add origin : 브릿지 잇기

git remote -v : 연결된거 확인

git push origin master : git에 master에 올리기

.gitignore : add 하지 않을 목록을 포함한 폴더 

-   add 하기 전에만 효력이 있다.
-   git add . 이용하여 올릴 때 특정 파일은 제외할 수 있도록
-   vim : git commit 만 입력했을 
-   i : insert 입력 → ignore added 
-   esc : 모드 빠져나가기
-   :wq : 저장하고 종료

git init : 절대 홈 폴더에서 x / 1회만 기입

git clone : 홈 폴더 가능 / 1회만 기입 → 폴더 채로 복사해온다. / 이미 연결된 상태(remote -v)

-   전체 진행상황을 다 가져올 때 / 다른 피씨에 그대로 복사할 때

git pull origin master : pull 땡기기