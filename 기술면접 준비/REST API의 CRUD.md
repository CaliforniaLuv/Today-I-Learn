```

 URL 주소를 통해 HTTP 메소드를 활용하여 CRUD 작업으로 클라이언트와 서버간의 응답, 요청이 상호작용하게 하는 방안이다.
 
 Create: POST
 Read: GET
 Update: PUT(해당 데이터 테이블의 모든 리소스를 변경), PATCH(해당 데이터 테이블의 부분적 리소스를 변경)
         만일 일부분의 데이터만 변경을 PUT 메서드로 처리하면 해당 데이터를 제외한 나머지 데이터들은 NULL로 대체되며 손실될 수 있다.
 Delete: Delete

```
