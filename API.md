Mongodb example Rest API 문서

============================

이 문서에서는 위 예제의 Rest API에 대해서 다룹니다.

통신 방법
=======
클라이언트 -> 서버(Upstream)
-------------------------

클라이언트와 서버가 통신하는 데에는 기본적으로 http프로토콜을 사용합니다.
서버의 JS 오브젝트는 JSON.stringfy(object)함수를 이용해 JSON으로 변환해줍니다.

서버->클라이언트(Downstream)
------------------------

서버에서 클라이언트로 보내는 정보는 모두 JSON포맷으로 보내도록 합니다.
JSON.parse(string)을 사용하여 자바스크립트 오브젝트로 변환후 DB에 넣도록 합니다.

서버 관리
=======
이 서버는 Mongodb를 사용합니다.
따라서, mongod 명령을 이용하여 데이터베이스 서버를 열어준 후, node를 이용해 서버를 열수있도록 합니다.

###자세한 내용은 아래 링크 참조
[참조링크](mobicon.tistory.com/197)

API Methods
===========

GET
----
Wine의 전체 DB목록을 관리하는 메서드입니다.

###URL

/wines

또한 id로 생성된 wine의 정보도 얻어올수 있습니다.

###URL

/wines/(objectID)

POST
----
새로운 Wine을 생성합니다.

###URL

/wines

PUT
---
id로 생성된 Wine의 정보 갱신이 가능합니다.

###URL

/wines/(objectID)

DELETE
------
생성된 Wine을 삭제할 수 있습니다.

###URL

/wines/(objectID)
