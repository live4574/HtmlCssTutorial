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


# input

input 태그는 form 태그 중에서 가장 중요한 태그로 사용자로부터 데이터를 입력받기 위해 사용된다.

input 태그는 다양한 종류가 있는데 type 어트리뷰트에 의해 구분된다. form 태그 내에 존재하여야 입력 데이터를 전송할 수 있으나 ajax를 사용할 시에는 form 태그 내에 존재하지 않아도 된다.

서버에 전송되는 데이터는 name 어트리뷰트를 키로, value 어트리뷰트를 값으로하여 key=value의 형태로 전송된다.


브라우저에 따라 지원여부 다를 수 있음.

button : 버튼생성
checkbox: 체크박스 생성
color: 컬러 생성
date : date control(년월일) 생성
datetime: date & time control (년월일시분초) 생성. HTML spec에서 drop되었다.
datetime-local:	지역 date & time control (년월일시분초) 생성
email:	이메일 입력 form 생성. subumit 시 자동 검증한다.
file:	파일 선택 form 생성
hidden:	감추어진 입력 form 생성
image:	이미지로 된 submit button 생성
month:	월 선택 form 생성
number:	숫자 입력 form 생성
password:	password 입력 form 생성	
radio : radio button 생성
range:	범위 선택 form 생성
reset:	초기화 button 생성
search:	검색어 입력 form 생성
submit:	제출 button 생성
tel:	전화번호 입력 form 생성
text:	텍스트 입력 form 생성
time:	시간 선택 form 생성
url:	url 입력 form 생성
week:	주 선택 입력 form 생성