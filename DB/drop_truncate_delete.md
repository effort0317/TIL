1. DROP  
- 테이블 자체를 삭제한다.
- auto commit이 이루어지며, 용량도 사라져서 롤백이 불가능하다.

2. TRUNCATE
- 테이블을 create table을 한 직후인 완전 초기상태로 돌려 놓는다.
- 모든 데이터, 인덱스 등 모든 정보들이 삭제된다.
- auto coimmit이 이루어지며, 용량도 줄어들어 롤백이 불가능하다.

3. DELETE
- 데이터를 삭제하되, 테이블 용량이 줄어들지 않는다.
- where절을 통해 원하는 데이터만 삭제 가능하다.
- auto commit이 되지 않아, oracle의 경우 commit 전이라면 롤백이 가능하다.