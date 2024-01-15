1. Http Referer란  
   ① 현재 웹사이트를 불러온 웹 주소를 알려 주는 HTTP 헤더값 중 하나이다.   
   ② 자바로 짜여진 스프링 웹 프레임워크 구조에서는 아래와 같이 컨트롤러 단에서 Http Referer값을 알 수 있다.
   - String referer = request.getHeader("referer");