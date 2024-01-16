1. DATE_FORMAT이란  
   ① mysql이 제공하는 날짜를 지정한 형식으로 출력하는 함수이다.  
   ② DATE_FORMAT('컬럼명 혹은 날짜', '원하는 형식') 과 같은 형태로 사용한다.  
2. 원하는 날짜 형식의 기호규칙  
   ① 년도 : %Y -> YYYY, %y -> yy  
   ② 월 : %M -> January ~ December, %m -> 00 ~ 12   
   ③ 일 : %d -> 00 ~ 31  
   ④ 시간 : %H -> 00 ~ 23, %l -> 00 ~ 12  
   ⑤ 분 : %i -> 00 ~ 59  
   ⑥ 초 : %S -> 00 ~ 59  
   ⑦ 요일 : %W -> Monday ~ Sunday
3. 예시
   ① SELECT DATE_FORMAT('20240115', '%Y.%m.%d') -> 2024.01.15  
   ② SELECT DATE_FORMAT('20240115220000', '%Y.%m.%d %H:%i:%S %W') -> 2024.01.15 22:00:00 Monday
