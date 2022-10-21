# Git과 GitHub 사용법
> * Git?
>    * Git은 **[버전 관리 시스템(Version Control System)](https://ko.wikipedia.org/wiki/%EB%B2%84%EC%A0%84_%EA%B4%80%EB%A6%AC)** 중 하나로 2005년 리누스 토르발스(리눅스 커널 개발자)가 처음 개발했다.
>       * VCS로는 Git, SVN(Subversion), CVS 등이 있다. 
>       * **버전 관리 시스템**은 파일의 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템으로, 소프트웨어 엔지니어링에서는 필수적인 요소이며 주로 소스 코드의 변경사항을 기록하고 관리하기 위해 사용한다.
>     * 쉽게 생각하면 Git은 로컬 저장소이다.
> * GitHub?
>    * GitHub는 Git을 관리해주는 웹 호스팅 서비스 중 하나로 가장 높은 점유율을 가지고 있다.
>       * GitHub는 2008년에 설립되었고, 2018년에는 MS에 인수되었다. 
>       * GitHub 웹 서비스는 Ruby on Rails를 기반으로 만들어졌다.
>       * GitHub 외에도 GitLab, Bitbucket 등의 Git 기반 버전 관리 호스팅 서비스들이 있다. 
>   * GitHub를 사용하려면 우선 컴퓨터(로컬)에 Git이 설치되어있어야한다.
>   * 쉽게 생각하면 GitHub는 로컬 저장소의 내역을 원격으로 관리해주는 원격 저장소이다.

## 설치하기
1. [Git 다운로드 페이지](https://git-scm.com/downloads)에서 Download for Windows 버튼 눌러 다운로드 받기
   * 가장 최근 버전의 Windows용 64bit Git이 다운로드 된다.
2. 기본 branch명 설정 부분을 제외한 나머지는 기본 설정으로 설치한다.
   * 예전에는 master라는 명칭을 사용했었지만, 노예 제도를 연상시킨다는 이슈가 있어 최근에는 거의 대부분 main 이라는 명칭을 사용한다고 한다. 그러므로 기본 branch명 설정 시 main으로 설정하도록 체크하고 설치하자 
   * (관련 이미지 넣을 예정)
   * `$ git config --global init.defaultbBranch main` 명령어로 나중에 변경하는 것도 가능하다.
3. 설치 후 Windows 탐색기 or 폴더 내에서 마우스 오른쪽을 클릭 하면 2가지 메뉴가 나타난다.
   1. Git GUI here : GUI(Graphical User Interface) 방식으로 Git 사용
   2. Git Bash here : CLI(Command Line Interface) 방식으로 Git 사용

## 사용하기
### [Git 사용자 정보 설정]
커밋 시 사용자 정보가 기록되기 때문에 설정이 잘 되어있는 지 확인해야한다.
```
$ git config --global user.name 'catveloper24-7'
$ git config --global user.email dkdmsl32@naver.com
$ git config --list //설정 되어있는 사용자 정보를 확인
```

### [GitHub의 Pages 기능]
Github에서 제공하는 정적 웹사이트 호스팅 서비스인 GitHub Pages를 이용하면 저장소(repository)에 있는 파일들을 웹 브라우저 상에서 실행해볼 수 있다.
* repository > Settings > Pages 메뉴에서 보여주고자하는 branch를 설정해야한다. (ex : main)
* 주소는 `https://{계정명}.github.io/{폴더명}/{파일명}`으로 기본 설정되며, 원하는 경우 커스텀 도메인 지정도 가능하다. 
  * ex : https://catveloper24-7.github.io/githubtestrepo/index.html
* 각 경로의 index.html은 생략 가능하다. 
  * 두 url은 동일하게 실행된다.
    1. https://catveloper24-7.github.io/githubtestrepo/test/index.html
    2. https://catveloper24-7.github.io/githubtestrepo/test/

### [CLI 방식으로 사용하기]
#### Git Bash를 이용하는 방법
Windows 탐색기 or 폴더 내에서 마우스 오른쪽 클릭하여 Git Bash here 메뉴로 실행한 후, 필요한 명령어를 입력한다.
```
$ git clone {GitHub url} .

$ git pull
$ git add .
$ git commit -m 'message contents'
$ git push
```
* `git clone {GitHub url}` : 지정한 원격 저장소의 정보를 로컬 저장소로 복제한다.
  * `$ git clone {GitHub url}` : 현재 선택된 경로(dir)에 하위 폴더를 생성하여 복제한다. 
  * `$ git clone {GitHub url} .` : 현재 선택된 경로(dir)에 바로 복제한다.
    * 압축파일 압축해제할 때 `여기에 압축풀기` 메뉴와 같은 기능이다.
  * ex : $ git clone https://github.com/catveloper24-7/TIL.git .
* `git pull` : 지정한 원격 저장소(GitHub의 repository)의 최신 데이터를 로컬 저장소로 받아온다.(갱신 update)
* `git add .` : 작업한 내용(변경사항)을 스테이지에 올린다. (커밋 준비 상태)
  * `git add .`을 하면 변경된 모든 파일이 스테이지에 올라간다.
  * `git add 특정파일명`을 하면 해당 파일만 스테이지에 올라간다.
    * ex : $ git add Git과GitHub사용법.md
* `git commit -m '커밋 메세지'` : 로컬 저장소에 작업한 내용을 저장한다. 이때 작업한 내용에 대한 설명으로 커밋메세지가 붙는다.
  * 커밋 메세지를 생략하고 `git commit`만 입력하면 vi 창이 나오며 커밋 메세지를 입력하도록 유도한다.(커밋 메세지를 입력하는 것이 권장사항) 
* `git push` : 커밋된 내용을 지정한 원격 저장소에 저장한다.

### [GUI 방식으로 사용하기]
  * GitHub 웹 사이트를 통해 repository 생성, 파일 등록/변경/삭제를 할 수 있다.

## 참고(Reference)
* [30분 요약 강좌 시즌4 : 알잘딱깔센 GitHub](https://www.inflearn.com/course/30%EB%B6%84-%EC%8B%9C%EC%A6%8C4-%EA%B9%83%ED%97%88%EB%B8%8C)
  * 전체적인 맥락은 본 강의를 통해 작성했다.
  * [학습자료(Notion)](https://paullabworkspace.notion.site/GitHub-435ec8074bcf4353afb947f601a030df)
* [Git 공식 책 - ProGit](https://git-scm.com/book/ko/v2)