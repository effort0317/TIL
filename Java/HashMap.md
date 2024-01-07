1. HashMap이란  
    ① {key, value}형태로 데이터를 저장  
      - index가 없기 때문에 List와 같이 순서의 영향을 받지 않는다.
      - 특정 값을 찾을 때 key값만 알면 바로 찾을 수 있다.
   
    ② Map인터페이스를 상속받음
      - 선언 예 : Map<String, String> map = new HashMap<>();
2. 메소드
   - 데이터 저장 : map.put(key, value);
   - 데이터 삭제 : map.remove(key);, map.clear();-> clear()는 모든 값 제거.
   - 데이터 조회 : map.get(key);  
     , map.getOrDefault(key, defaultKey);->map에 key에 해당하는 value가 존재하면 value를 반환하고, 해당하는 key값이 없으면 defaultKey를 반환한다.
3. entrySet() VS keySet()  
   - key값만 필요하면 keySet(), value값까지 모두 필요하면 entrySet()을 사용한다.
   - keySet() 예시 :  
     for (String key : map.keySet()) {  
         String value = map.get(key);  
         System.out.println("[key]:" + key + ", [value]:" + value);  
     }  
   - entrySet() 예시 :  
     for (Map.Entry<String, String> entry : map.entrySet()){  
     System.out.println("[key]:" + entry.getKey() + ", [value]:" + entry.getValue());  
     }