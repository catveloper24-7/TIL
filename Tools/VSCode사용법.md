# VS Code 사용법
> * [VS Code(Visual Studio Code)](https://ko.wikipedia.org/wiki/%EB%B9%84%EC%A3%BC%EC%96%BC_%EC%8A%A4%ED%8A%9C%EB%94%94%EC%98%A4_%EC%BD%94%EB%93%9C)는 Microsoft에서 개발한 소스코드 편집기이며 2016년 4월 15일에 정식판이 발표되었다.
> * Electron 프레임워크를 기반으로 개발되었다.
> * MS의 개발 툴 중 최초로 크로스 플랫폼을 지원하는 에디터이며 Windows, macOS, Linux를 모두 지원한다.
> * 가장 큰 강점은 확장 기능이고, 디버깅과 Git 제어, 구문 강조, SSH 접속 등의 기능을 지원한다. 

## 설치하기
1. [VS Code 다운로드 페이지](https://code.visualstudio.com/download#, "VS Code 다운로드 페이지")에서 Windows - System Installer 64Bit 버전으로 다운로드 받기
2. 기본 설정으로 설치하기

## 사용하기

### [TIL을 위한 마크다운 파일 작성]
1. 확장자를 `.md`로 하는 파일을 생성하고 저장한다.
2. `측면에서 미리보기 열기` 기능을 사용하면, 마크다운 문법으로 작성한 내용(좌측)과 rendering된 결과(우측)를 함께 보면서 작성할 수 있다.
   * 단축키 Ctrl + K, V
     * Ctrl + K 먼저 누르고 V(키보드 입력이 영문으로 되어있어야함) 누르기
3. `소스 제어 메뉴`를 통해 해당 파일에 대한 Git 버전 관리를 GUI 방식으로 할 수 있다. (로컬저장소)
   * Git 설정이 되어있는 파일/폴더를 열면 자동으로 설정이 되어있다.
   * 단축키 Ctrl + Shift + G
4. 로컬저장소(Git)의 변경사항을 원격저장소(GitHub)에 올리기(push)
   * `소스 제어 메뉴`의 **푸시 기능** 사용하기
   * `VS Code의 터미널 기능` 사용하기
     * 터미널 - 새 터미널 메뉴(단축키 Ctrl + `)


* 그 외 단축키
  * 내어쓰기 : Shift + Tab 
    * 들여쓰기 레벨을 한 단계 이전으로 되돌릴 때 
  * 강조 : 강조할 내용을 블럭으로 지정하고 Ctrl + B


### [유용한 확장 프로그램]
* 다양한 확장 프로그램들을 market place에서 검색하여 설치 및 사용할 수 있다.
    - `Korean Language Pack for Visual Studio Code` : 한글팩
      - 설치하고 VSCode 다시 시작해야 적용됨
    - `open in browser` : 작성한 파일을 브라우저에서 실행
      -  단축키 Alt + B : 기본 브라우저로 실행
    - `Prettier - Code formatter` : 코드 포맷팅
    - `indent-rainbow` : 소스의 들여쓰기 레벨을 색으로 알아보기 쉽게 표시 (가독성 up)
    - `Auto Rename Tag` : 태그 수정 시, 수정 사항이 태그 쌍(여는 태그, 닫는 태그)에 한 번에(같이) 적용되게 해줌
    - `Auto Close Tag` : 여는 태그 입력 시, 닫는 태그(close tag)를 자동으로 추가해줌
    - `Markdown All in One` : 마크다운 관련 플러그인

## 참고(Reference)
* [VS Code 위키백과](https://ko.wikipedia.org/wiki/%EB%B9%84%EC%A3%BC%EC%96%BC_%EC%8A%A4%ED%8A%9C%EB%94%94%EC%98%A4_%EC%BD%94%EB%93%9C)
* [VS Code 다운로드 페이지](https://code.visualstudio.com/download#)
* [패스트캠퍼스 - 스프링의 정석:남궁성과 끝까지 간다 강의](https://fastcampus.co.kr/dev_academy_nks)
* [VSCode를 마크다운(Markdown) 편집기로 사용하는 방법](https://sianux1209.github.io/etc/markdown_editor_vscode/)
* [Visual Studio Code에 git 연동하기](https://earth-95.tistory.com/m/87)
