### git rm - 파일삭제하기
- git rm <code>git rm</code> 명령으로 Tracked 상태의 파일 삭제한 후(정확하게 Staging Area)에서 삭제하는것) 커밋해야한다 
- 이 명령은 워킹 디렉토리에 있는 파일도 삭제하기 때문에 실제로 지워짐
- git rm --cached test.txt : Staging Area에서만 제거하고 워킹 디렉토리에 있는  파일은 제거 하지않을때

### git push - 변경된 내용 푸쉬(발행하기)
- git push -u origin master
	- origin : 리모트 저장소
	- master : 브랜치
	- u : 원격저장소로부터 업데이트를 받은 후 push를 한다는 의미 
- 변경이 될때마다 
	- pull > commit > push
	
### git 자주 사용되는 명령어 정리
```
$ git branch -> 로컬 branch 확인 
$ git branch -r 서버 branch 확인 
$ git checkout -b 브랜치명 브랜치를 만들고 바로 이동 
$ git branch -d(D) test 브랜치 삭제 
$ git status 현재상태(머지나 추가사항) 확인 $ git add 경로 에러를 해결하고 추가하여 에러해결 
$ git stash 임시저장 
$ git stash pop 임시저장한파일 불러오기 $ git remote prune origin 깃랩에서 삭제한거 서버와 동기화 
$ git push origin :브랜치네임 서버에서 삭제하기
$ git remote
$ git push origin dev 
$ git config http.postBuffer 104857600 git오류시 해결 
$ git merge --squash dev 
$ git merge --no-ff feature-  : 새로운 가지 따서 merge(관리상 용이) 
$ git clone 주소 
$ git remote set-url origin 주소 : gitlap 저장소 변경시 설정 
$ git remote -v : gitlap 저장소 주소 확인 // 고아 브랜치 만드는 방법 
$ git checkout master $ git checkout --orphan c_YYMMDD_CAMPAIGNNAME $ git rm -rf . $ git push origin c_YYMMDD_CAMPAIGNNAME  
```

### git log 확인
- $ git log --pretty=format:"%h,%ar,%an : %s" --graph
