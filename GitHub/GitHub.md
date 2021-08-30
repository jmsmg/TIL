습관적으로 git log 타이핑

레파지토리 생성

근본 연결

git remote add origin (레파지토리 주소)

git remote -v(연동 됐나 확인)

git branch

git add . -> commit 까지만

git branch

git checkout -b gon (로컬에 gon branch를 만듬)

> fatal: refusing to merge unrelated histories 근본이 다르다

---pull -unrelated histories
git pull origin 브랜치명 --allow-unrelated-histories

---생성한 로컬브랜치를 원격저장소에 푸쉬

git push origin 푸쉬할 브랜치 이름
git pull origin 브랜치이름

---생성한 로컬브랜치를 원격저장소의 해당 브랜치와 연동 
git branch --set-upstream-to origin/gon   (defalut값을 gon branch로 지정)

git log --oneline ( 로그 편하게)

git pull origin gon

원격끼리 합치기 pull request


---

git pull origin(원격) gon(브랜치이름) --allow-unrelated-histories      // 히스토리 관계없이 당겨옴

git checkout -b 이름    // 로컬에 브랜치생성

git branch --set-upstream-to origin/gon