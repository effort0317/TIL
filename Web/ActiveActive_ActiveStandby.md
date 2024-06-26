1. 서버이중화란  
   ① 서비스 운영의 안정성을 높이기 위해 서버를 이중 이상으로 구성하는 것  
   ② 흔히 Active-Active 또는 Active-Stand by 로 구성한다.
  
2. VIP 서버  
   ① Virtual IP의 줄임말로, L4서버라고도 하며 2대 이상의 서버가 존재할 시 클라이언트로 부터 온 요청 패킷을 특정 서버로 보내주는 역할을   
      한다.  
   ② VIP서버가 존재하므로써 실서버의 존재를 감출 수 있을 뿐만 아니라, VIP서버-실서버 간 내부망 연결을 통해 보안을 강화시킬 수 있다.  
   ③ SSL인증서를 적용해야하는 경우 흔히 VIP서버에만 적용을 한다. '클라이언트-VIP서버'는 외부망 연결일 경우가 많고, 'VIP-실서버'는 내부망   
      연결 일 경우가 많기 때문이다.
3. Active-Active  
   ① 2대 이상의 실서버를 모두 서비스에 사용하는 경우.  
   ② 주로 부하분산의 목적으로 쓰이며, VIP서버는 각 실서버에게 적절히 패킷을 전달한다(로드밸런싱).  
4. Active-Standby  
   ① 일부 실서버만 운영, 나머지 실서버들은 대기하다가 운영 중인 실서버에 문제가 생겼을 경우, VIP 서버는 패킷 전달의 대상을 대기 중인 
      실서버로 변경한다.  
   ② 장애 상황 등에 즉각적인 대처를 위해 구성하는 방식이다.
