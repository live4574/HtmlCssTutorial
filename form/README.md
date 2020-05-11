# form

attribute / value / description
action      URL     입력데이터(form data)가 전송될 URL 지정
method      get / post  입력데이터(form data) 전달 방식 지정

## GET

GET 방식은 전송 URL에 입력 데이터를 쿼리스트링으로 보내는 방식이다.
예) http://jsonplaceholder.typicode.com/posts?userId=1&id=1
전송 URL 바로 뒤에 ‘?’를 통해 데이터의 시작을 알려주고, key-value형태의 데이터를 추가한다. 1개 이상의 전송 데이터는 ‘&’로 구분한다.

REST API에서 GET 메소드는 모든 또는 특정 리소스의 조회를 요청한다.

## POST

POST 방식은 Request Body에 담아 보내는 방식이다.
예) http://jsonplaceholder.typicode.com/posts
URL에 전송 데이터가 모두 노출되지 않지만 GET에 비해 속도가 느리다.

REST API에서 POST 메소드는 특정 리소스의 생성을 요청한다.