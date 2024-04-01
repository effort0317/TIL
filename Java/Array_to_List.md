1. 배열 -> List 변경
- 'Arrays.asList()'을 사용.
- 예제 :   
   String array = {"a", "b", "c"};  
   List<String> list = Arrays.asList(array);
- 주의점 : 배열을 리스트화 한 후 리스트 값 변경(add, remove 등) 시 'java.lang.UnsupportedOperationException'
에러가 뜸. 
- 해결법 : 위 예제와 같은 경우 List<String> list = new ArrayList<>(Arrays.asList(array)); 와 같이 
'new ArrayList<>()'를 이용하여 초기화 해야함.

2. List->배열 변경
- 'toArray()'메소드를 이용하여 배열로 변경
- 예제 : 
  List<String> list = new ArrayList<>();  
  list.add("a");  
  list.add("b");  
  list.add("c");  
  String[] array = list.toArray(new String[list.size()]);
- 비고 : 위 예제와 같이 'toArray()'메소드 사용 시 파라미터로 List의 데이터 타입 배열 객체가 사용 되는 데  
        , 이 때 배열의 크기를 리스트 크기보다 같거나 작게하면 리스트와 동일한 크기의 배열이 만들어지고,   
         배열의 크기를 리스트보다 크게 하면 그 값 그대로 배열의 크기가 된다.  
         위 예제와 같은 경우 배열의 크기를 리스트 크기로 했으므로 리스트 크기의 배열이 만들어진다.
