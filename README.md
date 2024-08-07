# DynamicTable

자바스크립트로 만든 동적 테이블 생성 프로그램.

## 개요
개인적인 프로젝트를 위해 만들었습니다.

## 주의사항
버그가 꽤 있을 수 있습니다.

## 알려진 문?제점
테이블 헤더에서 부모 뎁스가 자식을 1개 가지는 경우, json의 data 항목에서 최하단 뎁스가 아닌 상위 뎁스를 키 값으로 입력한 경우, 값이 들어가지는 않습니다.(예시로 작성된 json의 경우 5-1-4-1에 해당함. 대신 5-1-4-1-1로 입력해야 정상적으로 값이 들어갑니다.)

row 타입이 object(JSON)인 경우에 헤더 값이 키로 매핑이 되므로, colspan 또는 rowspan 사용 시 해당 키에 매핑을 못하는 상황이 발생할 수 있습니다.

colspan을 사용하려는 컬럼이 서로 겹친 경우, 먼저 실행된 colspan 기준으로 실행됩니다.
(예시로 작성된 json에서 10번째와 12번째 컬럼 부분 참고)

현재 구조 상 Header나 Body에 값이 아닌 태그를 사용할 수 없기 때문에, 한계가 있습니다. 또한 Header와 Body를 name으로 매핑하는데, 태그를 허용하면 이 방식은 맞지 않아 수정이 필요합니다.

## TODO List
header값 name대신 key값이 필요함(실제 보여지는 부분은 value나 text 같은 다른 값으로 사용)

태그를 사용할 수 있도록 개선 예정