# Git 사용법

## 개요
### Git 이란 무엇인가 ?


### Git 과 Github 의 차이점

### 주요 용어 정리
* Repository - 저장소
  - 저장소는 히스토리, 시간/태그(Tag)/분기(Branch)에 따른 다른 버전들을 가지고 있다. 
  - Git에서 저장소를 다른곳으로 복사하더라도 다시 완벽한 저장소가 된다. 저장소는 작업하고 있는 복사본으로 수정본들을 얼마든지 검색할 수 있도록 한다.
* Branches - 분기 와 Tags - 태그
  - Git 저장서는 모든 분기들과 태그(tags)들을 가지고 있다. 
  - 분기들중 하나는 master라고 불리는 기본 분기이다. 
  - 사용자는 작업에 필요한 어떤 한 버전의 분기를 이 기본분기로 체크아웃(Checkout)한다.  
    - 이것을 작업 카피 (Working Copy)라고 한다.
* Commit - 커밋
  - 소스 수정사항들은 저장소로 커밋할 수 있다. 
  - 이것은 지난 시간까지 추적된 것에 대한 새로운 리비전(Revision)을 만드는 것이다. 
  - 각 커밋은 저자와 커밋한 내용(어떻게 수정을 했는지, 누가 커밋 했는지)을 저장한다.
* URL
  - Git에서 URL은 저장소의 위치이다.
* Revision - 리비전
  - 소스코드의 버전을 가리킨다. 
  - Git은 SHA1 ids으로 리비전을 구분한다. SHA1 ids는 160비트 으로 긴 편이고 16진수로 표현된다. 
  - 가장 최신버전은 HEAD로 불리는 주소로 표현되며 이전 버전은 HEAD~1으로 계속 그런 방식으로 버전이름을 가리킬 수 있다.


### 사용자 설정

## Git 시작하기

### 내용 생성하기

### 그 외

#### Git 에서 fork 와 clone 의 차이
* Github 에서는 자주 fork 라는 단어를 접할 수 있다. 하지만, git 에는 fork 라는 명령어가 없다. 차이점이 있을까?
  *  fork 와 clone 의 차이
    * 결론적으로 애기하면, fork 와 clone 은 동일한 작업이다.
      - github 의 내부 문서에서 fork 라는 것은 clone 을 해서 기존의 프로젝트에 기여하기 위해 upstream 등의 remote 를 설정하고 fetch 등의 작업을 하기 위한 일련의 행위 라고 설명되어 있다.
      - 즉 fork 버튼만 놓고 보면 clone 이다.

#### 특정 파일 (커밋) 무시하기

#### Markdown 문법
http://blog.kalkin7.com/2014/02/05/wordpress-markdown-quick-reference-for-koreans/

## 출처
- http://www.dreamy.pe.kr/zbxe/CodeClip/95408
- https://nolboo.github.io/blog/2013/10/06/github-for-beginner/
