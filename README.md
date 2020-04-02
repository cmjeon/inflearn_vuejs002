# learn-vue-js
인프런 Vue.js 시작하기 - Age of Vue.js 강좌 학습자료
https://www.inflearn.com/course/Age-of-Vuejs/lecture/21333

=프로그램 설치=
- ㅇㅇㅇ

=수업 소스 코드 안내=
- ㅇㅇㅇ

=VSCode에서 수업 코드 보는 방법=
- ㅇㅇㅇ

=VSCode 플러그인 설치 및 설정=
- 왼쪽 박스모양 > 검색 > Install
  vetur
  material icon theme
  night owl
  live server
  Auto Close Tag

- File - preferences - File Icon theme - material icon theme 선택
- File - preferences - Color theme - night owl 선택

- live server 실행방법
  파일 선택 - 우클릭 - Open with Live Server

=뷰 개발자 도구 소개 및 실행 방법=
- ㅇㅇㅇ

=MVVM 모델에서의 Vue=
- ㅇㅇㅇ

=기존 웹 개발 방식(HTML, Javascript)=
- 기존에 HTML, javascript를 사용하여 개발하는 방법
- Playgound-complete > web-dev.html 참조
- 에디터에서 
  shift + ! #html 폼 자동생성
  div@app #<div id='app'></div> 생성
- HTML은 문서의 구조(DOM)를 나타내고, Javascript는 DOM을 조작하는 역할임
- Javascript에서는 변수의 내용이 변경되면 변수를 DOM에 반드시 대입해줘야 함

=Reactivity 구현=
- Reactivity가 적용된 최신 기술?
- Playgound-complete > vue-way.html 참조
- Object.defineProperty란 > Object.defineProperty MDN 검색
- MDN은 표준 웹브라우저 기술을 설명해놓은 사이트로 주로 참조 할 것
- Object.defineProperty(대상 객체, 객체의 속성) { ... }의 구조
- Object.defineProperty(viewModel, 'str') { get() } Function 은 해당 값에 접근할 때
- Object.defineProperty(viewModel, 'str') { set() } Function 은 해당 값에 할당할 때

=Reactivity 코드 라이브러리화 하기=