# 1. font-size 프로퍼티
텍스트의 크기를 정의한다.

 .font-sizse-40{
     font-size: 40px;
 }
 .font-size-2x{
     font-size:2.0em;
 }
 }.font-size-150ps{
     font-size:150%;
 }
 .font-size-large{
     font-size:large;
 }

# 2. font-family 프로퍼티

폰트를 지정한다.컴퓨터에 해당 폰트가 설치되어 있지 않으면 적용되지 않는다.

폰트는 여러개를 동시에 지정 가능하다. 첫번째 지정한 폰트가 클라이언트 컴퓨터에 설치되어 있지 않으면, 다음에 지정된 폰트를 적용한다.

따라서 마지막에 지정하는 폰트는 대부분의 OS에 기본적으로 설치되어 있는 generic-family 폰트(Serif, Sans-serif, Mono space )를 지정하는 것이 일반적이다.


폰트 명은 따옴표로 감싸주며 폰트명이 한단어 인 경우는 따옴표로 감싸주지 않아도 괜찮다.

.serif{
    font-family:"Times New Roman", Times, serif;
}

.sans-serif{
    font-family:Arial, Helvetica, sans-serif;
}

.monospace{
    font-family:"Courier New", Courirer, monospace;
}


# 3. font-style / font-weight 프로퍼티

font-style 프로퍼티는 이탤릭체의 지정,
font-weight 프로퍼티는 폰트 굵기 지정에 사용된다.

font-style, font-weight

.itatlic{
    font-style:italic,
}

.light{
    font-weight:lighter;
}

.thick{
    font-weight:bold;
}

.thicker{
    font-weight:900;
}

# 4. font Shorthand

Shorthand Syntax

font : font-style(optional) font-variant(optional) font-weight(optional) font-size(madatory) line-height(optional) font-famliy(mandatory)


font: 2em "Open Sans", serif;

font: italic 2em "Open Sans", serif;

font: italic small-caps bolder 16px/1.2 monospace;

font: italic small-caps bolder 16px/3 cursive;



