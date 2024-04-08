1. equals()
- 객체의 조상 클래스 Object에서 equals()는 객체의 주소값 비교 메소드이다.
- String 클래스에서 equals()메소드는 문자열 값 비교로 사용 되는 데, 이는 String 클래스는 equals()메소드를 문자열 비교 로직으로 오버라이딩하였기 때문이다.

2. 해시코드(hashCode)
- 해시코드란 객체의 메모리 주소값을 이용해 만들어진 고유의 정수값이다.
- Object의 hashCode() 메소드를 통해 이 해시코드 값을 리턴 받을 수 있다.

3. equals() 메소드와 hashCode() 메소드를 오버라이딩해서 사용해야하는 이유
- Hash타입의 컬렉션(HashMap, HashSet 등등)에서 중복 에러를 방지하기 위해서이다.
- Hash타입의 컬렉션에서 객체를 비교 시 두 객체의 hashCode()의 리턴 값 비교 후, 동일할 시 equals()메소드의 리턴값을 통해 같은 객체인지 판단을 한다.
- 예를 들어, name(String 형)과 age(int 형)이라는 두 변수를 가진 Person이라는 클래스가 존재하고,
  이 클래스로 name과 age이 동일한 person1, person2 두 객체를 생성 후, 이 두 객체를 HashMap의 key값으로 사용 시 equals()와 hashCode()를
  오버라이딩 하지 않으면 두 객체의 hashCode값이 다르므로 두 객체를 다른 객체로 판단한다.
- 즉, person1과 person2 두 객체가 동일한 객체로 판단되기 위하여 hashCode()와 equals() 두 메소드를 오버라이딩해서 사용한다.
  