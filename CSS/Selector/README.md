# 셀렉터

CSS(Cascading Style Sheets)는 HTML 요소(Element)의 style(design, layout etc)을 정의한다. 그리하려면 HTML이 존재하여야 하고 또한 style을 적용하고자하는 HTML 요소를 특정할 필요가 있다.

이러한 목적으로 사용되는 것이 셀렉터(Selector)이다. 즉, style을 적용하고자하는 HTML 요소를 셀렉터로 특정하고 선택된 요소에 스타일을 정의하는 것이다.


  복수개의 셀렉터를 연속하여 지정할 수 있으며 쉼표( , )로 구분한다.

  h1, p { color: red; }

# 1. 전체 셀렉터 (Universal Selector)

패턴	Description
 *별표	HTML 문서 내의 모든 요소를 선택한다. html 요소를 포함한 모든 요소가 선택된다. (head 요소도 포함된다)

   *별표 { color: red; }


 # 2. 태그 셀렉터 (Type Selector)

 패턴	Description
태그명	지정된 태그명을 가지는 요소를 선택한다.

지정된 태그명을 가지는 요소를 선택한다.


 p { color: red; }


# 3. ID 셀렉터 (ID Selector)


패턴	Description
#id 어트리뷰트 값	id 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. id 어트리뷰트 값은 중복될 수 없는 유일한 값이다.

/* id 어트리뷰트 값이 p1인 요소를 선택 */
    #p1 { color: red; }

# 4. 클래스 셀렉터 (Class Selector)


패턴	Description
.class 어트리뷰트 값	class 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. class 어트리뷰트 값은 중복될 수 있다.

/* class 어트리뷰트 값이 container인 모든 요소를 선택 */
    /* color 어트리뷰트는 자식 요소에 상속된다. */
    .container { color: red; }
    /* not supported in IE */
    #p2 { color: initial; }

HTML 요소에 class 어트리뷰트 값은 공백으로 구분하여 여러 개 지정할 수 있다. 아래와 같이 클래스 셀렉터를 사용하여 미리 스타일을 정의해 두고, HTML 요소는 이미 정의되어 있는 클래스를 지정하는 것으로 필요한 스타일을 지정할 수 있다. 이것은 재사용의 측면에서 유용하다.

   /* class 어트리뷰트 값이 text-center인 모든 요소를 선택 */
    .text-center { text-align: center; }
    /* class 어트리뷰트 값이 text-large인 모든 요소를 선택 */
    .text-large  { font-size: 200%; }
    /* class 어트리뷰트 값이 text-red인 모든 요소를 선택 */
    .text-red    { color: red; }
    /* class 어트리뷰트 값이 text-blue인 모든 요소를 선택 */
    .text-blue   { color: blue; }


# 5. 어트리뷰트 셀렉터 (Atrribute Selector)

패턴	            Description
셀렉터[어트리뷰트]	지정된 어트리뷰트를 갖는 모든 요소를 선택한다.

  /* a 요소 중에 href 어트리뷰트를 갖는 모든 요소 */
    a[href] { color: red; }

패턴	Description
셀렉터[어트리뷰트=”값”]	지정된 어트리뷰트를 가지며 지정된 값과 어트리뷰트의 값이 일치하는 모든 요소를 선택한다.
/* a 요소 중에 target 어트리뷰트의 값이 "_blank"인 모든 요소 */
    a[target="_blank"] { color: red; }

패턴	Description
셀렉터[어트리뷰트~=”값”]	지정된 어트리뷰트의 값이 지정된 값을 (공백으로 분리된) 단어로 포함하는 요소를 선택한다.

/* h1 요소 중에 title 어트리뷰트 값에 "first"를 단어로 포함하는 요소 */
    h1[title~="first"] { color: red; }


패턴	Description
셀렉터[어트리뷰트|=”값”]	지정된 어트리뷰트의 값과 일치하거나 지정 어트리뷰트 값 뒤 연이은 하이픈(“값-“)으로 시작하는 요소를 선택한다.

  /* p 요소 중에 lang 어트리뷰트 값이 "en"과 일치하거나 "en-"로 시작하는 요소 */
    p[lang|="en"] { color: red; }

    

패턴	Description
셀렉터[어트리뷰트^=”값”]	지정된 어트리뷰트 값으로 시작하는 요소를 선택한다.

/* a 요소 중에 href 어트리뷰트 값이 "https://"로 시작하는 요소 */
    a[href^="https://"] { color: red; }

패턴	Description
셀렉터[어트리뷰트$=”값”]	지정된 어트리뷰트 값으로 끝나는 요소를 선택한다.

/* a 요소 중에 href 어트리뷰트 값이 ".html"로 끝나는 요소 */
    a[href$=".html"] { color: red; }

패턴	Description
셀렉터[어트리뷰트*=”값”]	지정된 어트리뷰트 값을 포함하는 요소를 선택한다.

 /* div 요소 중에서 class 어트리뷰트 값에 "test"를 포함하는 요소 */
    div[class*="test"] { color: red; }
    /* div 요소 중에서 class 어트리뷰트 값에 "test"를 공백으로 단어로 포함하는 요소 */
    div[class~="test"] { background-color: yellow; } 

# 6. 복합 셀렉터 (Combinator)

# 6.1 후손 셀렉터 (Descendant Combinator)

자신의 1 level 상위에 속하는 요소를 부모 요소, 1 level 하위에 속하는 요소를 자손 요소(자식 요소)라한다.

자신보다 n level 하위에 속하는 요소는 후손 요소(하위 요소)라 한다.

후손 셀렉터는 셀렉터A의 모든 후손(하위) 요소 중 셀렉터B와 일치하는 요소를 선택한다.


셀렉터A 셀렉터B

 /* div 요소의 후손요소 중 p 요소 */
    div p { color: red; }

# 6.2 자식 셀렉터 (Child Combinator)
자손 셀렉터는 셀렉터A의 모든 자식 요소 중 셀렉터B와 일치하는 요소를 선택한다.

셀렉터A > 셀렉터B

 /* div 요소의 자식요소 중 p 요소 */
    div > p { color: red; }

# 6.3 형제(동위) 셀렉터 (Sibling Combinator)
형제(동위) 셀렉터는 형제 관계(동위 관계)에서 뒤에 위치하는 요소를 선택할 때 사용한다.






