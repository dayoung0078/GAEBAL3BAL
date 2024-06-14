<details>
<summary>이은석</summary>
<div markdown="1">

<h1>Thymeleaf</h1>

<pre>
웹 서비스를 만들 때 서버의 데이터 정적 자원(html, css, img)을 조합한다

1 SPA (Single Page Application)
   최초 한 번 전체페이지를 다 불러오고 응답데이터만 페이지 특정부분 렌더링

2. SSR(Server Side Rendering)
   전통적인 웹 애플리케이션 방식. 요청시마다 서버엫서 처리한 후 새로고침으로 페이지에 대한 응답

자바에서 웹 개발시 JSP ( Java Server Page)를 이용하여 진행
JSP 를 사용하면 <% %>형태의 스크립트릿을 사용
html이 혼재된 상태가 되고 html태그의 반복적인 사용으로 인핸 수정하기 어려운 상황이됩니다

이러한 상태를 해결하고자 하는것이 템플릿 엔진을 사용

템플릿 엔진 (Markup)  
데이터를 결한한 결과물을 만들어주는 도구

타임리프는 그 중 하나

스프링 부트에서 JSP가 아닌 타임리프를 사용하는것을 권장

먼저 타임리프의 속성들에 대해 알아보고 실습을 진행하겠습니다.
</pre>


<pre>

<h3>표현식</h3>

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

</pre>

<h1>ViewResolver</h1>

<pre>
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fo6VcT%2FbtrQZsM5B7H%2FZs1LpORY4X9sJfjYjD9Ay1%2Fimg.png">

@Controller 어노테이션을 사용하면 반환값을 처리하는 과정에서 ViewRsolver가 사용된다

뷰 리졸버란 스프링 프레임워크에서 뷰 객체를 생성하는 방법을 결정하는 인터페이스이다.

뷰 리졸버는 컨트롤러가 반환하는 뷰 이름을 뷰 객체로 변환하는데, 
변환된 객체는 <span style=background-color:#fff5b">디스패처 서블릿이</span> 클라이언트에게 반환하는 
응답을 생성하기 위해 사용된다




</pre>
```
디스패처 서블릿?

Servlet(서블릿)이란 자바로 작성된 프로그램을 실행할 수 있는 웹 애플리케이션을 실행하기 위한 스펙이다.
즉, 동적인 웹 페이지를 생성해 주는 자바 웹 프로그래밍 기술



DispatcherServlet(디스처 서블릿)

디스패처 서블릿은 HTTP 프로토콜로 들어오는 모든 요청을 가장 먼저 받아 적합한 컨트롤러에 위임해 주는 Front Controll(프론트 컨트롤러)이다.

*****Front Controller(프론트 컨트롤러): 주로 서블릿 컨테이너의 제일 앞에서 서버로 들어오는 클라이언트의 모든 요청을 받아서 처리하는 컨트롤러

```
</div>
</details>