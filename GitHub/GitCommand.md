# Github 기본 명령어

1. 폴더 생성

2. Git 관리하에 폴더 넣기(레파지토리)
   - git init

   - git config --global user.name "(내 이름)"
   - git config --global user.email "(내 이메일)"

3. Git 파일들 상태 확인
   - git status

4. Git 커밋
   - git add .
   - git commit -m "메시지"

5. Git reset, revert
   - git reset (일련번호 6자리) -- hard 
   - git revert (일련번호 6자리)

---

# Github branch 명령어

1. branch 생성
   - git branch (branch 이름)

2. branch 이동
   - git branch (branch 이름)

3. branch 병합(merge, rebase)
   > 메인 branch로 이동을 한 뒤
   - branch merge (가져올 branch 이름)

4. branch 삭제
   - git branch -D (branch 이름)

5. branch 그래프 확인 방법
   - git log --graph --all --decorate


6. branch conflict 상황


## Github 용어 전체

git config --list

--global

 git config --global core.editor "code"  
$ git config --global -e  
$ git config --global core.editor "code --wait"  
$ git config --global user.name "jmsmg"  
$ git config user.name  
$ git config --global user.mail  
 
$ git config --global core.autocrlf true

open .git  
rm -rf .git    # master end  


tracking = 스테이지에 작업파일 올리는 것 


git diff --staged  (=cached)  
git diff -h   - 도움말


VSC에서 확인 및 수정하기  
git config --global -e    -   editor 실행

difftool "vscode"  
   cmd = code --wait --diff $LOCAL $REMOTE

---------------

텍스트파일 만들기  
echo xxxxx >> a.txt  

내용 추가  
echo xxx > a.txt  

모든 txt 파일 tracking  
git add *txt  


---커밋하기  
git commit -m "커밋메시지"  

git log -> 커밋후 로그 확인  


---로컬 브랜치 생성  
git checkout -b 생성할 브랜치 이름

---생성한 로컬브랜치를 원격저장소에 푸쉬  
git push origin 푸쉬할 브랜치 이름 

---생성한 로컬브랜치를 원격저장소의 해당 브랜치와 연동  
git branch --set-upstream-to origin/feature-01

---브랜치전환  
git checkout 브랜치이름   

---브랜치 이름 변경  
git branch -m 기존브랜치이름 새로운브랜치이름  

---오리진의 마스터계정으로 내용물을 업로드  
git push -u origin master    (맨뒤가 브랜치 이름)

---강제푸쉬(원격저장소 내용 삭제됨)  
git push -u origin +master    (맨뒤가 브랜치 이름)

---로컬과 원격 저장소 연동끊기  
git remote remove origin       (origin = 원격저장소 브랜치 이름?)

---원격브랜치 삭제  
git push origin --delete 브랜치이름

---특정 브랜치에서 pull  
git pull origin 브랜치이름

---로컬-원격 저장소 연동시키기  
git remote add origin https://github.com/jmsmg/test.git

---푸쉬할 수 있는 곳 확인하기  
git remote -v 


로컬저장소(커밋까지 한 상태)에서 가져오기 <> 풀은 원격에서 가져오기  
---checkout 



myproject 폴더생성  
mkdir myproject

---현재 경로의 폴더와 파일들 확인   
ls  

---현재 경로 확인  
pwd 




---파일내용 보기  
cat 파일명 

---add와 commit을 하나의 명령어로 처리하기  
git commit -a -m "커밋메시지"        (-a = add , -m = commit)

---특정 파일에 대한 로그만 보고싶을 때  
git log -- 파일이름

---로그를 간단하게 출력  
git log --oneline


---merge로 병합하기(현재브랜치로)   
git merge 현재브랜치로 가져와서 병합할 브랜치이름 

---cmd창 에디터모드에서 탈출하기  
:wq

---cmd창 파일삭제  
del 파일이름    (.git 삭제할 때 사용)


---rebase (이력 통합 - rebase하는 브랜치이력이 전부 사라지고, rebase 대상 브랜치이력으로 통합됨)  
git rebase onto 브랜치이름  
git rebase onto origin/원격브랜치이름


---강제 pull  
git fetch --all  
git reset --hard origin/master  
git pull origin master



---pull - unrelated histories  
git pull origin 브랜치명 --allow-unrelated-histories  
















