# Git 

## 개요
### Git 이란 무엇인가 ?
* Git 이란?
  - Git은 분산형 버전 관리 시스템(DVCS) 이다.
  - 만약 당신이 소스코드에 수정을 가한다면 그것에 대해 버전 관리 시스템에 마크(mark)하고 (즉 index/staging으로 add) 그러고 난 뒤 저장소로 추가(commit)한다
  - Git 은 커밋을 당신의 지역 저장소로 하도록 하며 당신의 Remote 저장소로 동기화 하도록 돕는다
* Git 과 Github 의 차이점
  - Github 는 Git 을 사용하는 프로젝트를 지원하는 웹 기반의 호스팅 서비스이다.


### 주요 용어 정리
* Repository
  - 저장소는 히스토리, 시간/태그(Tag)/분기(Branch)에 따른 다른 버전들을 가지고 있다. 
  - Git에서 저장소를 다른곳으로 복사하더라도 다시 완벽한 저장소가 된다. 저장소는 작업하고 있는 복사본으로 수정본들을 얼마든지 검색할 수 있도록 한다.
* Branches
  - Git 저장서는 모든 분기들과 태그(tags)들을 가지고 있다. 
  - 분기들중 하나는 master라고 불리는 기본 분기이다. 
  - 사용자는 작업에 필요한 어떤 한 버전의 분기를 이 기본분기로 체크아웃(Checkout)한다.  
    - 이것을 작업 카피 (Working Copy)라고 한다.
* Commit
  - 소스 수정사항들은 저장소로 커밋할 수 있다. 
  - 이것은 지난 시간까지 추적된 것에 대한 새로운 리비전(Revision)을 만드는 것이다. 
  - 각 커밋은 저자와 커밋한 내용(어떻게 수정을 했는지, 누가 커밋 했는지)을 저장한다.
* URL
  - Git에서 URL은 저장소의 위치이다.
* Revision
  - 소스코드의 버전을 가리킨다. 
  - Git은 SHA1 ids으로 리비전을 구분한다. SHA1 ids는 160비트 으로 긴 편이고 16진수로 표현된다. 
  - 가장 최신버전은 HEAD로 불리는 주소로 표현되며 이전 버전은 HEAD~1으로 계속 그런 방식으로 버전이름을 가리킬 수 있다.
* Staging Index
  - Git 은 당신이 변경사항들을 명확하게 표기하길 요구하고 저장에 적절하게 수정사항들이 표기되길 원한다. 
  - 예를들어 당신이 새로운 파일을 다음 변경사항에 적용하고 싶으면 소위 'staging index'에 그 파일들을 'add file' 명령을 이용해 넣으면 된다. 
  - Staging index는 변경사항들에 대한 완벽한 스냅샷이다.
* VCS( Version Control System ) 버전 관리 시스템
  - 파일 변화를 시간에 따라 기록했다가 이후에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템.
  - 동일한 정보에 대한 여러 버전을 관리하게 되며, 버전을 통해 시간적으로 변경 사항과 변경 사항을 작성한 작업자를 추적할 수 있다.
* DVCS( Distributed Version Control System ) 분산 버전 관리 시스템
  - 클라이언트가 파일의 마지막 스냅샷을 가져오는 것이 아니라 저장소 자체를 복제.
  - 서버에 문제가 생길 경우 이 복제물로 작업이 가능하며 서버를 복원할 수도 있다.
  - 리모트 저장소가 존재하며 리모트 저장소가 많을 수도 있다.
 
  
## Git 시작하기

### 사용자 설정
* Git에서 사용될 사용자 설정하기  
  - git config --global user.name "minku"  
* Git 에서 사용할 이메일 설정
  - git config --global user.email "minku@gmail.com"  
* push default 방식 설정
  - git config --global push.default 방식
    * 방식
      * matching 
        - 원격 저장소의 브랜치와 일치하는 모든 로컬 브랜치를 Push
      * simple
        - 현재 작업중인 브랜치만 Push
* Git 설정사항 확인
  - git config --list 

### 주요 명령어
* git init
  - 깃 저장소를 초기화한다.
  - 이것을 입력한 후에야 추가적인 깃 명령어가 가능하다.
* git status
  - 저장소 상태를 체크
* git add
  - 저장소에 새 파일을 추가하진 않는다.
  - git 의 저장소 "스냅샷" 에 포함되게 한다.
* git commit
  - 어떤 변경사항이라도 만든 후, 저장소의 스냅샷을 직기 위해 입력한다. 
* git branch
  - 새로운 브랜치를 만들고 자신만의 변경사항과 파일 추가 등의 커밋 타임라인을 만든다.
  - cat 이란 새로운 브랜치를 만들고 싶다면  
    - git branch cat
* git checkout
  - 현재 위치하고 있지 않은 저장소를 “체크아웃”할 수 있다. 
  - 이것은 체크하길 원하는 저장소로 옮겨가게 해주는 탐색 명령이다. 
  - master 브랜치를 들여다 보고 싶으면, git checkout master를 사용할 수 있고, git checkout cats로 또 다른 브랜치를 들여다 볼 수 있다.
* git merge
  - 브랜치에서 작업을 끝내고, 모든 협업자가 볼 수 있는 master 브랜치로 병합할 수 있다.
  - cat 브랜치에서 만든 모든 변경사항을 master 로 추가한다.
    - git merge cats
* git push
  - 로컬 저장소의 커밋을 원격 저장소에 반영한다. 
  - push 만 입력할 경우 자동으로 origin( github ) 로 보내게 된다.
* git pull
  - 현재 작업하고 있는 저장소의 최신 버전을 받는다.
* git clone
  - 저장소를 복제한다.



### 내용 생성하기
* Repository 를 생성하는 과정이다
  * 로컬 Repository 를 생성하여 원격 Repository 로 반영하거나 또는 원격 Repository 를 생성하고 로컬로 clone 할 수 있다.


* 로컬 저장소 생성하기
  - 원하는 폴더를 생성한다. 
    * 모든 Git 저장소는 .git 폴더에 저장되어 있으며 .git 폴더는 당신이 생성한 git 저장소 폴더안에 있다. 
    * .git 폴더는 저장소의 환결설정 정보와 저장소의 완벽한 히스토리 정보를 담고 있다. 
    - cd ~/
    - mkdir test.git
    - cd test.git
  - Git 저장소로 초기화
    - git init
  - 저장소로 파일 추가 ( 폴더만으로는 원격에 저장소가 추가되지 않는다. )
    - git add readme.md
  - 로컬 커밋
    - git commit -m "메세지"
  - 원격( remote ) 저장소에 생성한 로컬 저장소 연결하기
    - git remote add origin https://github.com/martinkang/test
  - 원격 저장소에 push 하기
    - git push -u origin master 
    - 


### 저장소 clone 하기
* 원격의 저장소 clone 하기
  - git clone https://github.com/martinkang/test 
   
  
### 파일 삭제
* 만일 버전관리를 받던 파일을 삭제했을 경우 git add 명령은 staging index 에서 파일 제거를 할 수 없다.
  - git add -A 옵션을 주면 파일 제거가 적용 된다. 

### 변경내용 Push 및 Pull 하기

### 변경사항 되돌리기( revert )
* Staging Index 에 추가되지 않았을 경우
  - checkout 을 하면 이전 버전으로 돌아갈 수 있다.
    - echo "test" > test.txt
    - git checkout test.txt
* Staging Index 에 변경내용이 적용됬을 경우 ( git add 또는 commit 시 )
  - Staging Index 의 test.txt 를 원래대로 복원한다.
    - git reset HEAD test.txt
  - Staging Index 로 부터 본래 파일을 Working Copy 로 checkout 함으로서 본래 내용을 복원한다.
    - git checkout test.txt


### 분기 및 합치기

#### 분기 ( Branches )
* 로컬 저장소의 분기 목록
  - git branch
* 모든 분기 보기 ( 원격 분기 포함 )
  - git branch -a
* 새로운 분기 생성
  - git branch test
  - git checkout test
##### 분기 삭제하기
  - git branch -d test

## 그 외

### Git 에서 fork 와 clone 의 차이
* Github 에서는 자주 fork 라는 단어를 접할 수 있다. 하지만, git 에는 fork 라는 명령어가 없다. 차이점이 있을까?
  *  fork 와 clone 의 차이
    * 결론적으로 애기하면, fork 와 clone 은 동일한 작업이다.
    - github 의 내부 문서에서 fork 라는 것은 clone 을 해서 기존의 프로젝트에 기여하기 위해 upstream 등의 remote 를 설정하고 fetch 등의 작업을 하기 위한 일련의 행위 라고 설명되어 있다.
    - 즉 fork 버튼만 놓고 보면 clone 이다.

### 특정 파일 (커밋) 무시하기
* Git에게 ".gitignore"파일을 통해 무시하고 싶은 디렉토리를  알려줄 수 있다. 
* 혹은 파일의 패턴을 알려줄 수 있다. 
  * 예를들어 git에게 "bin" 폴더를 무시하고 싶다고 알려주고 싶다면 ".gitignore"파일에 다음과 같이 쓰면 된다.
    - bin   

### Markdown 문법
- http://blog.kalkin7.com/2014/02/05/wordpress-markdown-quick-reference-for-koreans/

## 출처
- http://www.dreamy.pe.kr/zbxe/CodeClip/95408
- https://nolboo.github.io/blog/2013/10/06/github-for-beginner
- https://wikipedia.org
- http://flowerykeyboard.tistory.com/1
- http://www.dreamy.pe.kr/zbxe/CodeClip/95408
