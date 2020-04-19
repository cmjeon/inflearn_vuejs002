# markdown 사용법
- https://gist.github.com/ihoneymon/652be052a0727ad59601
# learn-vue-js
인프런 Vue.js 시작하기 - Age of Vue.js 강좌 학습자료
https://www.inflearn.com/course/Age-of-Vuejs/lecture/21333

# 프로그램 설치
- ㅇㅇㅇ

# 수업 소스 코드 안내
- ㅇㅇㅇ

# VSCode에서 수업 코드 보는 방법
- ㅇㅇㅇ

# VSCode 플러그인 설치 및 설정
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

# 뷰 개발자 도구 소개 및 실행 방법
- ㅇㅇㅇ

# MVVM 모델에서의 Vue
- ㅇㅇㅇ

# 기존 웹 개발 방식(HTML, Javascript)
- 기존에 HTML, javascript를 사용하여 개발하는 방법
- Playgound-complete > web-dev.html 참조
- 에디터에서 
  shift + ! #html 폼 자동생성
  div@app 으로 <div id='app'></div> 생성
- HTML은 문서의 구조(DOM)를 나타내고, Javascript는 DOM을 조작하는 역할임
- Javascript에서는 변수의 내용이 변경되면 변수를 DOM에 반드시 대입해줘야 함

# Reactivity 구현
- Reactivity가 적용된 최신 기술?
- Playgound-complete > vue-way.html 참조
- Object.defineProperty란 > Object.defineProperty MDN 검색
- MDN은 표준 웹브라우저 기술을 설명해놓은 사이트로 주로 참조 할 것
- Object.defineProperty(대상 객체, 객체의 속성) { ... }의 구조
- Object.defineProperty(viewModel, 'str') { get() } Function 은 해당 값에 접근할 때
- Object.defineProperty(viewModel, 'str') { set() } Function 은 해당 값에 할당할 때

# Reactivity 코드 라이브러리화 하기
- 즉시 실행 함수 표현(IIFE, Immediately Invoked Function Expression)
- https://webcoding.tistory.com/154 참고
- 즉시 실행 함수 표현이란 함수를 선언함과 동시에 즉시 실행되는 함수를 나타냄. 즉시 실행 함수는 코드가 실행될 때 딱 한 번만 실행되며 그 후에는 다시 호출할 수 없음. 그렇기 때문에 초기화 기능으로 사용함
즉시 실행 함수의 사용 이유
- 자바스크립트에서 전역 공간에 수많은 변수를 선언하다 보면 변수명이 겹쳐서 프로그램에 문제가 생기거나 혼란을 야기할 수 있는데, 이러한 문제점을 즉시 실행 함수를 이용하여 방지가능

# Hello Vue.js와 뷰 개발자 도구
- 크롬 개발자 도구에서 Vue 탭으로 가면 Vue의 디버깅이 가능
- data를 수정하면 화면에서 즉시 변경되는 것 확인가능

# 인스턴스 소개
- new Vue()를 이용해 인스턴스 생성가능
- vue script 도입
- el 속성으로 id를 선언하면 해당 id를 가진 태그를 찾아서 인스턴스를 부착함
- el로 부착한 인스턴스를 통해서만 인스턴스 사용가능

# 인스턴스와 생성자 함수
- 뷰 인스턴스를 생성자 함수로 만드는 이유? : Vue 인스턴스에 대해 미리 다 정의해놓고 재사용만 할 수 있음

# 인스턴스 옵션 속성
- new Vue ({el:, template:, data:, methods:, created:, watch:, ...})로 객체 리터럴로 표현

# 컴포넌트 소개
- 화면을 영역별로 구분해서 개발할 수 있는 뷰의 기능이 컴포넌트
- 컴포넌트를 사용하며 코드 재사용성이 올라가고 빠르게 화면을 제작할 수 있음

# [실습 안내] 컴포넌트 등록 및 실습
- Vue.component('컴포넌트 이름', 컴포넌트 내용); 을 통해 컴포넌트 생성가능
- 생성된 컴포넌트 이름과 동일한 이름의 태그를 Vue 인스턴스 태그 내에 선언하여 표현가능

# [실습 풀이] 전역 컴포넌트 등록
- 

# 지역 컴포넌트 등록
- 지역컴포넌트는 Vue 객체안에 components 속성을 통해 생성
- components : {'컴포넌트 이름','컴포넌트 내용'}

# 전역 컴포넌트와 지역 컴포넌트의 차이점
- 지역컴포넌트는 싱글페이지앱을 만들 때 주로 활용
- 전역컴포넌트는 전역에서 사용해야하는 라이브러리를 제작할 때 활용

# 컴포넌트와 인스턴스와의 관계
- 전역컴포넌트는 인스턴스에 선언되지 않으므로 어디에서나 전역 컴포넌트를 쓸 수 있음
- 지역컴포넌트는 인스턴스 내부에서 선언하지 않으면 사용불가

# 컴포넌트 통신
- 데이터 전달 방법
- 상위 > 하위 : props 전달
- 하위 > 상위 : event 발생

# 컴포넌트 통신 규칙이 필요한 이유
- 컴포넌트 간의 규칙이 없이 통신하는 경우 데이터의 변화에 따른 원인을 찾기 어려움
- 따라서 데이터는 상위에서 하위로 props를 전달하고, 하위에서 상위는 이벤트를 발생시킴

# props 속성
- playground/props.html 참조
- app에 data 속성에 message 선언
- app-header의 props 속성에 propsdata1 선언
- app-header 에 v-bind:props 속성 이름="상위 컴포넌트의 데이터이름 추가
- ex) v-bind:propsdata1="message"

# props 속성의 특징
- 하위 컴포넌트의 props 속성은 reactivity가 적용됨
- 상위 컴포넌트의 data를 바꾸면 하위 컴포넌트에도 적용됨

# [실습 안내] props 속성 실습
- playgound/props.html

# [실습 풀이] props 속성 실습 풀이

# event emit

# [실습 안내] event emit 실습 안내

# [실습 풀이] event emit 실습 풀이

# 뷰 인스턴스에서의 this
- https://www.w3schools.com/js/js_this.asp
- https://medium.com/better-programming/understanding-the-this-keyword-in-javascript-cb76d4c7c5e8

# 같은 컴포넌트 레벨 간의 통신 방법
- 상하위 관계가 아닌 같은 레벨의 컴포넌트간의 통신방법
- Root
|- AppHeader
`- AppContent

# 같은 컴포넌트 레벨 간의 통신 방법 구현1
- AppContent >(event)> Root >(props)> AppHeader

# 같은 컴포넌트 레벨 간의 통신 방법 구현2

# 뷰 라우터 소개와 설치
- Vue Router : 싱글 페이지 애플리케이션 구현에 사용하는 라이브러리
- vue.js의 공식 라이브러리

# 뷰 라우터 인스턴스 연결 및 초기 상태 안내
- playgound/router.html
- Router 생성 후 Vue에 router를 주입
```
new Vue({
  el:'#app',
  router: myRouter
});
```

# 라우터가 표시되는 영역 및 router-view 태그 설명
```
<router-view></router-view>
```

# 링크를 이용한 페이지 이동 및 router-link 태그 설명
```
<router-link to="/login">Login</router-link>
```

# 라우터 정리 및 학습 방향 안내
- https://joshua1988.github.io/web-development/vuejs/vue-router-navigation-guards/


