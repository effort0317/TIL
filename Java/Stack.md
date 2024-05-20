1. Stack이란
- java.util패키지에서 제공하는 LIFO(Last In First Out)형태의 자료구조.
- Stack<E>와 같이 제네릭 클래스이다.

2. 메서드
- push(E item) : 맨 위에 item추가
- pop() : 맨 위의 요소 제거하고, 제거 된 요소 return
- peek() : 맨 위의 요소 제거하지 않고 return
- size() : 스택에 존재하는 요소 갯수 반환
- clear() : 스택에 존재하는 모든 요소 제거
- empty() : 스택에 요소가 하나도 없는 지 boolean값 return(true : 요소가 하나도 없음, false : 요소가 하나 이상 존재)
- get(index) : 해당 index에 해당하는 item return(여기서 index는 맨 아래부터 0,1,2... 순으로 시작)