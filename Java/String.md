1. new String을 이용한 문자열 생성
- 「 String string = new String("hello world"); 」 와 같은 방식으로 문자열 생성
- 메모리의 Heap 영역에 생성이 됨
- 같은 문자열이라도 각각 Heap영역에서 다른 문자열을 바라봄.   
예를들어 「 String string1 = new String("hello world"); 」과 「 String string2 = new String("hello world"); 」  
에서 변수 string1과 string2는 같은 문자열 "hello world"을 참조하고 있지만, 두 변수는 heap메모리에서 각각 다른 주소 위에 올라 가 있는 
 문자열 "hello world"를 바라보고 있다.

2. 문자열 리터럴 생성 방식
- 「 String string = "hello world"; 」 과 같은 방식으로 문자열 생성.
- 해당 문자열 "hello world"는 상수풀(String Constant Pool, 자바 7이상 기준 메모리의 Heap영역에 존재)에 할당된다.  
- 「 String string1 = "hello world"; String string2 = "hello world"; 」 과 같이 두 개의 변수를 생성하면,  
 두 변수가 참조하는 문자열은 "hello world"로 동일하므로 상수풀에서 같은 문자열을 바라본다.