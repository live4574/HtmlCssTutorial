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

# select
복수개의 리스트에서 복수개의 아이템을 선택할 때 사용한다. 함께 사용할 수 있는 태그는 다음과 같다.

서버에 전송되는 데이터는 select 요소의 name 어트리뷰트를 키로, option 요소의 value 어트리뷰트를 값으로하여 key=value의 형태로 전송된다.

# textarea


textarea 태그는 여러 줄의 글자를 입력할 때 사용한다.

# button

button 태그는 클릭할 수 있는 버튼을 생성한다. <input type="button">과 유사하지만 input 태그는 빈 태그인 반면 button 태그는 그렇지 않다. 따라서 button 요소에는 텍스트나 이미지 같은 콘텐츠를 사용할 수 있다.

type 어트리뷰트는 반드시 지정하는 것이 바람직하며 어트리뷰트값으로 button, reset, submit를 지정할 수 있다.


button 태그는 어트리뷰트만을 받아들이는 input 태그와 달리 콘텐츠로 문자열은 물론 HTML 요소를 받을 수도 있다는 장점이 있다. 주의할 것은 IE의 경우, submit되는 값이 다를 수 있는 것이다.

<button type="submit" name="myButton" value="foo">Click me</button>
위 예제의 경우, IE6, IE7에는 ‘foo’ 대신 ‘Click me’를 서버로 전송한다. 따라서 오래된 IE를 지원해야 한다면 input 태그를 사용하는 것이 바람직하다.


# filedset / legend

fieldset 태그는 관련된 입력 양식들을 그룹화할 때 사용한다. legend 태그는 fieldset 태그 내에서 사용되야 하며 그룹화된 fieldset의 제목을 정의한다.

