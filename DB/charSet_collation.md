1. charSet
- 데이터베이스에서 텍스트 데이터가 저장될 때, 어떻게 인코딩 되어 저장될 것인지 규칙의 집합
- 대표적으로 EUC-KR, UTF8 등이 있다.
- charSet별로 한 문자당 byte수가 다를 수 있다. 예를 들어 EUC-KR은 한글로 한 글자 당 2byte, UTF8은 3byte이다.

2. collation
- 문자 정렬기준이다.
- 예를 들어 알파벳 소문자 'a'와 알파벳 대문자 'A'가 있고 정렬을 할 시 어느 것이 더 먼저오는 지 기준이 되는 것이다.
- 대표적으로 utf8_general_ci, utf8_unicode_ci 등이 있다.