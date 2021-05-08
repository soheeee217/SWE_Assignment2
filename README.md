# Github Repository Link: [SWE_Assignment2](https://github.com/soheeee217/SWE_Assignment2.git)

## 1. Git 과 Github란?  

- *Git*은 컴퓨터의 파일의 **변경사항을 추적**하고, 여러 사용자들 사이에서 파일들의 **작업을 조율**하기 위한 시스템이다.  
- *Github*는 Git에 **프로젝트 관리 지원 기능**을 추가로 제공하는 웹 호스팅 서비스이다.  
- 과거, 혹은 미래로의 **버전 간 이동**이 용이하고, **협업**에 용이하기에 많은 개발자들이 사용하고 있다.  

## 2. Git 명령어 사용  

### 2.1 Repository 생성

- 하나의 새로운 프로젝트를 시작하기 위해서 팀원들과 사용할 새로운 Repository를 생성해야 한다.
- Github에 가입/로그인 후 New를 선택한다.  
![Git New](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/Repository%20%EC%83%9D%EC%84%B11.PNG?raw=true)

- Repository name 입력하고, Create repository를 통해 Repository를 새로이 생성한다.  
![Git Create Repository](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/Repository%20%EC%83%9D%EC%84%B12.PNG?raw=true)

### 2.2 Git 저장소 만들기

> ### git init <a id= "init"></a>

- 터미널을 이용해 현재의 디렉토리에서 버전 관리를 시작하려고 한다. 이를 위해 새로운 저장소를 만든다.
- 명령은 `git init`을 사용한다.  
![Git Init](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20init.png?raw=true)

> ### git add <a id= "add"></a>

- 현재 버전관리를 위해 새 저장소를 만들었다.
- 이제 Git이 파일을 관리, 추적하게 하고자 한다.
- `git add filename` 명령을 통해 추적할 파일을 추가할 수 있다. *filename*에는 관리할 파일의 이름을 넣는다.
- 파일을 add 하게 되면 해당 파일을 스테이지에 올리게 되는데, 스테이지에 올라갔다는 것은 commit을 할 준비가 되었다는 뜻이다.
  - *commit*은 수정한 것을 저장하는 것을 의미한다. 이후에 다시 언급될 것이다.
- 예시로, ***MarkdownGuide.md***라는 파일을 add 하고자 한다. 실행 과정과 결과는 다음과 같다.  
![Git Add](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20add.png?raw=true)

> ### git commit <a id= "commit"></a>

- 현재 `git add` 명령을 통해 파일을 추가했다.
- 수정한 것 파일을 add 했고, 이를 저장하고자 한다.
- `git commit` 명령을 통해 commit을 할 수 있다. 이때, commit 한다는 것은 수정한 것을 저장한다는 의미로 생각할 수 있다.
- 이 명령에는 옵션이 존재하는데, 옵션 `ㅡm` 을 통해 commit을 하면서 간단한 메시지를 저장할 수 있다.
  - `git commit -m "message"`
  - *message*에는 적을 메시지를 작성하면 된다.
- 옵션 `--amend`를 사용해 완료한 commit을 수정할 수 있다. 정확히는 commit을 재작성 할 수 있다.
- 예시로, ***MarkdownGuide.md***를 add 한 것을 *First Commit*이라는 메시지와 함께 commit을 해보겠다. 실행 과정과 결과는 다음과 같다.  
![Git Commit](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20commit.png?raw=true)

> ### git status <a id= "status"></a>

- 지금까지 `git init`, `git add`, `git config`를 했었다.
- 이 명령들이 잘 수행되었는지 궁금해질 것이다. 그래서 이 명령 이후들의 상태를 확인하고자 한다.
- `git status` 명령을 통해 파일들의 상태를 확인할 수 있다.
- 이전에 init을 한 후에 ***MarkdownGuide.md***의 상태는 다음과 같다.
- 아무것도 add 되어 있지 않다며, add 하라고 붉은 글씨로 되어 있다.  
![Git Status after Init](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20status%20init.png?raw=true)

- ***MarkdownGuide.md*** 파일을 add한 후의 상태는 다음과 같다.
- **new file**이라는 표시와 함께 해당 파일이 commit 할 준비가 되었다고 알려준다.  
![Git Status after Add](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20status%20add.png?raw=true)

- add 했던 것을 commit 한 후의 상태는 별다른 메시지를 출력하지 않는다.  
![Git Status after Commit](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20status%20commit.png?raw=true)

### 2.2 사용자 설정

> ### git config <a id= "config"></a>

- 프로젝트에 대한 환경을 설정 하고자 한다.
- `git config` 명령을 통해 다양한 설정들을 조작할 수 있다.
- 이 명령에는 옵션이 존재하는데 옵션을 사용하지 않는 경우에는 해당 설정을 해당 프로젝트에만 적용을 하지만, 컴퓨터 내에서 진행하는 모든 프로젝트에 대한 영향은 `--global`을 사용한다.
- 예시로 전체 프로젝트에 대한 user의 이름을 *SoheeKim*으로 설정하고, 이 프로젝트에 대한 user의 이름은 *Sohee*로 설정하였다.  
![Git Config](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20config.png?raw=true)

### 2.3 커밋 히스토리 조회하기

> ### git log <a id= "log"></a>

- 현재 commit을 한번 진행한 상태이다.
- 그동안의 히스토리를 알아보고자 한다.
- `git log` 명령을 통해 그동안 commit되었던 log들, 즉 히스토리를 볼 수 있다.
- 다른 버전의 commit으로 돌아가거나, 혹은 저장소의 기록을 찾아볼 때에 `git log`에 출력되는 commit의 체크섬(commit의 고유 이름과 비슷한 개념)을 참고하여 돌아 갈 수 있다.
- 일반적으로 `git log`를 사용하면 가장 최근의 commit이 가장 먼저 나오게 된다.
- 옵션 `-2`는 가장 최근 두 개의 결과만 보여주는 옵션이 있다.
- 다양한 옵션이 존재하지만 현재 수준에서는 log내용을 모두 보아도 큰 문제가 되지 않을 것 같아 생략한다.
- 예시로 첫 commit을 한 후의 log를 출력했다. **First Commit**이라는 메시지를 통해 commit이 되었다는 것을 알 수 있다.  
![Git Log](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20log.png?raw=true)

### 2.4 리모트 저장소

> ### git clone <a id= "clone"></a>

- 현재 Github에 repository가 생성되어 있거나 다른 프로젝트의 저장소를 로컬 저장소에 복사하고자 한다.
- `git clone Repository주소` 명령을 통해 프로젝트의 히스토리를 포함하여 복사 해온다.
- 예시로 SWE_Assignment2 repository의 내용을 복사하였다.  
![Git Clone](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20clone.png?raw=true)

> ### git remote <a id= "remote"></a>

- 현재 프로젝트에 등록된 리모트 저장소를 확인하고자 한다.
- `git remote`명령을 통해 현재 프로젝트에 등록된 리모트 저장소를 확인할 수 있다.
- clone을 하지 않았거나, 따로 리모트 저장소를 추가하지 않은 경우에는 리모트 저장소가 뜨지 않을 것이다.
- `git remote add 단축이름 URL` 명령을 통해 새로운 리모트 저장소를 추가 할 수 있다.
- 예시로 *origin*이라는 이름을 통해 repository를 사용할 수 있게 되었다. 또, 현재 등록된 리모트 저장소는 *origin*이라는 것을 알 수 있다.  
![Git Remote](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20remote%20add.png?raw=true)

- 옵션 `-v`는 단축이름과 URL을 함께 볼 수 있다.  
![Git Remote -v](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20remote%20-v.png?raw=true)

> ### git push <a id= "push"></a>

- 프로젝트를 진행하다가 공유하고자 한다.
- `git push 리모트저장소 브랜치이름` 명령을 통해 Github에 공유할 수 있다.(브랜치는 이후에 다시 언급할 것이다.)
- 리모트 저장소의 내용을 Github 서버에 공유할 수 있다.
- 예시로 *origin* 이라는 리모트 저장소의 파일들을 *master*라는 브랜치에 push하였다.  
![Git Push](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20push.png?raw=true)

> ### git tag <a id= "tag"></a>

- 특정 commit을 릴리즈 할 때 버전을 tag해 표현하고자 한다.(예: v1.0)
- `git tag` 명령을 통해 그동안의 commit의 tag가 있는지 확인 할 수 있다.
- `git tag 태그명` 명령을 통해 tag를 새로이 만들 수 있다.
- 옵션 `-m`는 태그를 만들면서 메시지를 함께 저장할 수 있다.
- 예시로 *v.1.0이라는 tag를 만들었다.  
![Git Tag](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20tag.png?raw=true)

### 2.5 브랜치

> ### git branch <a id= "branch"></a>

- 현재 main 프로젝트가 있고, 이 main 프로젝트에 issue가 생겼거나, 개인적으로 새로운 기능을 추가하는 새로운 시도를 해보려고 한다.
- main을 개인적으로 새로운 시도를 해보고자 할 때, main에 직접 시도하여 main을 수정하면 팀원들에게 민폐이고, 에러가 생기게 되면 복구하기 번거로우므로 이를 시도할 새로운 테스트 공간인 branch를 만들어 내려고 한다.
- `git branch 브랜치이름` 명령을 통해 새로운 branch를 만들수 있다.
- 예시로 *new*라는 branch를 새로 만들었다.  
![Git Branch](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20branch%20new.png?raw=true)

- main 이외의 다양한 branch가 존재할 때 현재의 branch 위치를 알고자 한다.
- `git branch` 명령을 통해 현재 branch의 위치를 알 수 있다.
- \* 표시로 표시된 branch가 현재 branch의 위치이다. 예시로 현재 branch는 *master*에 위치해 있다.  
![Git Branch](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20branch.png?raw=true)

> ### git checkout <a id= "checkout"></a>

- 현재 branch가 새로 생성되었고, 새로운 시도를 해보기 위해 하위 branch로 이동하여 작업을 하고자 한다.
- `git checkout 브랜치이름` 명령을 통해 branch를 이동할 수 있다.
- 예시로 *master* branch에서 *new* branch로 이동하였다.  
![Git Checkout](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20checkout.png?raw=true)

> ### git merge <a id= "merge"></a>

- 현재 branch를 통해 이런저런 수정을 하고 테스트가 완료되었다.
  - 예시로 *master* branch와 *new* branch에 ***1.txt***라는 파일을 추가해 수정을 했었다. 이는 commit 히스토리로 남아 있다.
![Git 1.txt Change](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20merge%201txt.png?raw=true)

- 이 branch를 다른 branch와 합치고자 한다.
- branch를 병합할 때에는 병합시킬 branch로 이동 후, `git merge 브랜치이름` 명령을 통해 병합할 수 있다.
- 옵션 `--merged`는 현재 checkout 된 branch에서 병합된 branch들을 보여주고, 옵션 `--no-merged`는 현재 checkout된 branch에서 병합되지 않은 branch들을 보여준다.
- *master* branch를 *new* branch와 병합하기 위해 *master* branch에서 *new*를 병합하였다.  
![Git Merge](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20merge.png?raw=true)

### 2.6 리셋

> ### git reset --hard <a id= "reset"></a>

- 현재 commit 했던 것들 중 오류가 있어 이전의 commit으로 돌아가고자 한다.
- `git reset` 명령을 통해 이전의 commit으로 돌아갈 수 있다.
- 옵션 `--hard`는 돌아가려는 이력 이후의 모든 내용을 지워버린다.
- 돌아가고자 하는 commit의 체크섬을 log를 통해 알아내고, 해당 commit까지 reset 할 수 있다.
- 예시로 merge 한 내용이 잘못 되었다고 가정하고, merge 하기 이전의 commit까지 reset하였다. 해당 commit의 체크섬을 알아내고, reset 하였다.
- reset 한 후 log를 보면 merge 하였던 commit의 log가 사라져있다.  
![Git Reset --hard](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20reset%20--hard%201.png?raw=true)

### 2.7 또다른 브랜치 병합

> ### git rebase <a id= "rebase"></a>

- 현재 branch들을 병합하고자 한다.
- 병합을 한 후의 commit history가 깔끔했으면 좋겠다고 생각했다.
- `git rebase` 명령을 통해 commit을 깔끔하게 하면서 branch를 선형으로 병합 할 수 있다.
- `git merge`는 병합하면서 해당 내용을 병합한 유사한 새로운 branch를 만들지만 `git rebase`는 병합하면서 하나의 작업이 차례대로 수행된것 처럼 히스토리가 선형으로 된다.
- 예시로 *mastet*와 *new* 두 branch를 rebase 하였다.  
![Git Rebase](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20rebase.png?raw=true)

### 2.8 데이터 가져오기

> ### git pull <a id= "pull"></a>

- 리모트저장소에 push되었던 데이터 중 다른 데이터를 가져오고자 한다.
- `git pull 리모트저장소 브랜치이름` 명령을 통해 리모트저장소의 내용을 해당 branch에 저장할 수 있다.
- `git pull`은 `git push`와 반대되는 것으로 `git push`는 공유를 하는 기능이고,  `git pull`공유된 프로젝트를 가져가져오는 기능이다.
- 예시로 *origin*의 내용을 *new* branch에 저장하였다.  
![Git Pull](https://github.com/soheeee217/SWE_Pic/blob/soheeee217-patch-1/git%20pull.png?raw=true)

## 3. 명령어 사용 여부 표

|명령어|사용여부|링크|
|:---:|:---:|:---:|
|add          |O|[add](#add)|
|branch       |O|[branch](#branch)|
|checkout     |O|[checkout](#checkout)|
|clone        |O|[clone](#clone)|
|commit       |O|[commit](#commit)|
|config       |O|[config](#config)|
|init         |O|[init](#init)|
|log          |O|[log](#log)|
|merge        |O|[merge](#merge)|
|pull         |O|[pull](#pull)|
|push         |O|[push](#push)|
|rebase       |O|[rebase](#rebase)|
|remote       |O|[remote](#remote)|
|reset --hard |O|[reset --hard](#reset)|
|status       |O|[status](#status)|
|tag          |O|[tag](#tag)|
