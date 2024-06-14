<details>
<summary>이은석</summary>
<div markdown="1">
1. Thymeleaf

웹 서비스를 만들 때 서버의 데이터 정적 자원(html, css, img)을 조합한다

1 SPA (Single Page Application)
   최초 한 번 전체페이지를 다 불러오고 응답데이터만 페이지 특정부분 렌더링

2. SSR(Server Side Rendering)
   전통적인 웹 애플리케이션 방식. 요청시마다 서버엫서 처리한 후 새로고침으로 페이지에 대한 응답

자바에서 웹 개발시 JSP ( Java Server Page)를 이용하여 진행
JSP 를 사용하면 <% %>형태의 스크립트릿을 사용
html이 혼재된 상태가 되고 html태그의 반복적인 사용으로 인핸 수정하기 어려운 상황이됩니다

이러한 상태를 해결하고자 하는것이 템플릿 엔진을 사용

템플릿 엔진 (Markup) ? 
데이터를 결한한 결과물을 만들어주는 도구

타임리프는 그 중 하나

스프링 부트에서 JSP가 아닌 타임리프를 사용하는것을 권장

먼저 타임리프의 속성들에 대해 알아보고 실습을 진행하겠습니다.

표현식
변수 : ${…}
선택 변수 : *{…}
메시지 : #{…}
Link URL : @{…}
리터럴
텍스트 : ‘one text’, ‘Another one’,…
숫자 : 0, 34, 1.0, …
boolean : true, false
Null : null
token : one, sometext, main, …
text opeation
문자열 연결 : +
문자 대체 : |The name is ${name}|
연산
Binary : +, -, *, /, %
마이너스 : -
boolean 연산
Binary : and, or
부정 : !, not
비교 연산
비교연산자 : >, <, >=, <= (gt, lt, ge, le)
균등연산자 : ==, != (eq, ne)
조건 연산
if-then : (if) ? (then)
if-then-else : (if) ? (then) : (else)
Default : (value) ?: (defaultValue)

리졸브

</div>
</details>