# 1. display 프로퍼티

display 프로퍼티는 layout 정의에 자주 사용되는 중요한 프로퍼티다.

block : block 특성을가지는 요소 (block 레벨 요소)로 지정
inline: inline 특성을 가지는 요소(inline 레벨 요소)로 지정
inline-block: inline-block 특성을 가지는 요소(inline-block 레벨 요소)로 지정.
none: 해당 요소를 화면에 표시하지 않는다. (공간조차 사라진다.)

모든 HTML 요소는 아무런 CSS를 적용하지 않아도 기본적으로 브라우저에 표현되는 디폴트 표시값을 가진다. HTML 요소는 block 또는 inline 특성을 갖는다.

아래는 p 요소에 대한 크롬 브라우저의 디폴트 css이다.

p{
    display:block;
    -webkit-margin-before: 1em;
    -webkit-margin-after: 1em;
    -webkit-margin-start: 0px;
    -webkit-margin-end: 0px;
}

display 프로퍼티는 상속되지 않는다.

# 1.1 block 레벨 요소

block 특성을 가지는 요소 (block 레벨 또는 block 요소)는 아래와 같은
특징을 갖는다.

- 항상 새로운 라인에서 시작한다.
- 화면 크기 전체의 가로폭을 차지한다. (width:100%)
- width, height, margin, padding 프로퍼티 지정이 가능하다.
- block 레벨 요소 내에 inline 레벨 요소를 포함할 수 있다.

-block 레벨 요소 예

 div
 h1 ~ h6
 p
 ol
 ul
 li
 hr
 table
 form



 # 1.2 inline 레벨 요소

 inline 특성을 가지는 요소(inline 레벨 요소 또는 inline 요소)는 아래와 같은 특징을 갖는다.

 - 새로운 라인에서 시작하지 않으며 문장의 중간에 들어갈 수 있다. 
 즉 줄을 바꾸지 않고 다른 요소와 함께 한 행에 위치한다.
 - content의 너비만큼 가로폭을 차지한다.
 -width, height, margin-top, margin-bottom 프로퍼티를 지정할 수 없다. 상,하 여백은 inline-height로 지정한다.
 -inline 레벨 요소 뒹에 공백(엔터, 스페이스 등)이 있는 경우, 정의하지 않은 space(4px)가 자동 지정된다.
 - inline 레벨 요소 내에 block 레벨 요소를 포함할 수 업삳.
 inline 레벨 요소는 일반적으로 block 레벨 요소에 포함되어 사용된다.
 - inline 레벨 요소 예

   span
   a
   strong
   img
   br
   input
   select
   textarea
   button


   # 1.3 inline-block 레벨 요소

   block 과 inline 레벨 요소의  특징을 모두 갖는다.
   inline 레벨 요소와 같이 한 줄에 표현되면서 width, height, margin 프로퍼티를 모두 지정할 수 있다.

   - 기본적으로 inline 레벨 요소와 흡사하게 줄을 바꾸지 않고 다른 요소와 함께 한 행에 위치시킬 수 있다.
   - block 레벨 요소처럼 width, height, , margin, padding 프로퍼티를 모두 정의할 수 있다.
   상, 하 여백을 margin과 inline-hegiht 두가지 프로퍼티 모두를 통해 제어할 수 있다.
    -content의 너비만큼 가로폭을 차지한다.
    -inline-block 레벨 요소 뒤에 공백(엔터, 스페이스 등)이 있는 경우, 정의하지 않은 space(4px)가 자동 지정된다. 이것을 회피 방법은 Fighting the Space Between Inline Block Elements를 참조. 
    https://css-tricks.com/fighting-the-space-between-inline-block-elements/

    # 2.visibility 프로퍼티
    visibility 프로퍼티는 요소를 보이게 할 것인지 보이지 않게 할 것인지를 정의한다. 즉, 요소의 렌더링 여부를 결정한다.

    visible : 해당 요소를 보이게 한다(기본값)
    hidden : 해당 요소를 보이지 않게 한다. display:none;은 해당 요소의 공간까지 사라지게 하지만 visibility:hidden;은 해당 요소의 공간은 사라지지 않고 남아있게 된다.
    collapse: table 요소에 사용하며 행이나 열을 보이지 않게 한다.
    none: table 요소의 row나 column을 보이지 않게 한다.
    IE, 파이어폭스에서만 동작하며 크롬에서는 hidden과 동일하게 동작한다.



    # 3. opacity 프로퍼티
    opacity 프로퍼티는 요소의 투명도를 정의한다.
    0.0~1.0의 값을 입력하며 0.0은 투명, 1.0은 불투명을 의미한다.

    