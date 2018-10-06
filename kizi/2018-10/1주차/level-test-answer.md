# level test answer
## HTML
1. Doctype을 사용하지 않을 때는 무슨 일이 발생할까요?

DTD는 브라우저의 렌더링 모드를 지정해준다.
doctype 선언을 선언하지 않을 때는 Quirks mode(웹 브라우저 마다 코드가 다르게 렌더링됨)로 렌더링이 되어, 엉뚱한 결과의 페이지로 출력되는 문제에 직면한다.

2. 웹표준에 맞게 작업할 때 b, i 태그 대신 적합한 태그는 각각 무엇일까요?

b > strong
i > em

3. block 요소와 inline 요소에 해당하는 태그들을 각각 5개씩 적어보세요.

block 요소 - div, h1, p, ul, ol, li, dl, dt, dd, blockquote, form, ..
inline 요소 - span, a, em, img, strong, abbr, acronym, input, label, select, ..

4. blockquote 태그는 어떤 용도로 사용해야 할까요?

인용구 글을 나타내고자 할때 용한다.

5. 인라인 스타일(style=”property:value”)을 가급적 사용하지 말아야 할 이유는 무엇일까요?

+ 1.css 유지관리가 용이하지 않다.
+ 2.시멘틱 웹에 적합하지 않다.
   (웹표준의 기본 요구조건이 구조와 표현/행위 분리이다.)
+ 3.Perfomence 효율이 좋지 않다.
   (하나의 HTML안에 포함되어 있는 정보량이 많아 질 수록 효율은 저하된다.)
+ 6. myPhoto.jpg 파일을 img 태그로 작성해보세요.

```
<img src=“myPhoto.jpg” alt=“”>
```

7. HTML에서 id 속성을 사용하는 이유와 주의 할 점은 무엇일까요?

HTML 스팩에서 id 는 고유성을 가지므로 한 문서에 한번만 사용이 가능하다.
그러므로 해당 문서에서 고유성을 갖은 요소를 제어할때 사용함을 목적으로 해야한다. id 속성은 class 속성의 css우선순위보다 높기때문에 사용에 있어 신중해야한다.

8. ‘TopArea’라는 클래스명이 좋지 않은 이름이라면 그 이유는 무엇일까요?

+ 1. css는 2개 이상의 단어가 사용된 속성에도 -(hyphen)를 사용한다. 
   css의 기본 문법에 맞춰 사용함에 있어 통일감을 줄 수 있다.
+ 2. -(hyphen) syntax는 보다 더 읽기 용이하다.
+ 3. -(hyphen) syntax는 css 속성 선택자를 보다 쉽게 사용할 수 있다.

9. ‘blue-box’라는 클래스명이 좋지 않은 이름이라면 그 이유는 무엇일까요?
‘조나단 스눅'의 SMACSS에서는 css규칙을 4가지 범주로 나누도록 제안한다.

+ 1.기본(base)
+ 2.레이아웃(layout)
+ 3.모듈(modules)
+ 4.상태(state)

또한, '의미있는 클래스명을 사용하는 것’ 역시 구조와 표현의 분리라는 시맨틱 웹의 가장 기본적인 원칙이다. 클래스명도 ID와 마찬가지로 HTML의 구조를 의미하는 중요한 수단이다. 그렇다면 이 요소가 갖고있는 역할을 작명함이 더 적절하다.

[신현석님의 '의미있는 CSS 클래스 명을 써라’]

10. HTML5에 새롭게 추가된 aside 태그는 어떤 용도로 사용해야 할까요?

주요 문맥을 담은 section과 관련성을 지니고 있지만, 부연 설명 혹은 광고처럼 문맥의 주요 흐름에는 속하지 않는 section을 나타낼때 사용한다.

11. input 태그와 항상 함께 사용해야 할 태그는 무엇일까요?

form, lable

12. 모바일 웹 또는 반응형웹디자인 프로젝트에서 각 기기에 적합한 화면을 보여주기 위해 필요한 meta 태그는 무엇일까요?

<meta name=“viewport” content=“width=device-width, initial-scale=1.0, user-scalable=no”>

## CSS
1. 화면 상에는 보이지 않으나, 스크린 리더에서 읽혀야 하는 요소에 주어야 할 스타일링을 작성해보세요.

.bind {
position: absolute !important;
height: 1px; width: 1px;
overflow: hidden;
clip: rect(1px 1px 1px 1px); // for IE6, IE7
clip: rect(1px, 1px, 1px, 1px);
}
*일반적으로 사용하는 display:none; 속성은 읽히지 않으며,
visibility:hidden; 속성은 기기 별 차이가 있다.

2. float 속성을 가진 자식을 품은 부모요소는 높이 값이 0이 되는 때가 있습니다. 이 현상을 해소하는법(clearing)을 알고 있나요?

부모 element에 overflow: hidden; 혹은 clear: both; 속성을 준다.

3. border-box와 content-box의 차이점은 무엇일까요?

content-box (css 규격에 의해 default값) 는 box-model에서 border/padding 이 content의 크기값에 포함되여 렌더링 되며,
border-box는 box-model에서 border/padding 의 값에 상관없이 content의 크기값을 유지한다.

4. position: relative는 어떤 경우에 사용 하나요?

+ 1.레이아웃을 변경하지 않고 위치를 조정할때
+ 2.position: absolute;을 갖고있는 자식요소의 기준점을 설정할때
+ 3.레이아웃을 변경하지 않고 z-index 값으로 쌓임 순서를 지정할때

5. CSS Reset은 무엇이며 왜 사용할까요?

브라우저에 내장된 css를 초기화하여 보다 자유로운 스타일 제어와 원활한 크로스 브라우징을 위해서 사용한다.

6. Sass, less, Stylus와 같은 CSS 프리프로세서를 사용해본적이 있나요?

less 사용중

7. id, class, inline style, !important를 우선순위 순으로 나열해보세요.

!important > inline-style > id > class

8. CSS에서 상속이 되는 속성을 2개만 꼽아보세요.

font 속성, color .. 

9. Sprite image 기법을 사용하는 이유는 무엇일까요?

http 호출(서버로의 요청 횟수)을 줄여 페이지의 첫 로딩속도를 줄이기 위함이 목적이다. 더불어 내려받는 이미지의 크기까지 줄여줄 수 있는 효과도 있다.

10. Sprite image 기법을 사용하는데 필요한 CSS 속성들을 꼽아보세요.

background-image / background-position / width / height

11. 점진적 향상(Progressive Enhancement)의 뜻을 설명 할 수 있나요?

사용가능한 기능을 바탕으로 향상된 기능을 적용하기 전에 테스트를 통해 풍부한 사용자 경험을 하나씩 증가시킴을 의미한다.

12. 웹폰트를 적용하기 위해서는 어떤 확장자의 폰트 파일들이 필요할까요?

eot(ie legacy browder)/ ttf,otf woff(mordern browder) / svg (ios legacy browder)

13. 개발사 접두어(vendor prefix)를 꼭 사용해야 할 CSS 속성(property)를 2개만 꼽아보세요.

translate / transform

14. 반응형웹디자인의 3가지 요소를 꼽아보세요.

+ 1.grid
+ 2.plexible
+ 3.user-interaction

15. 모바일기기를 대응할 때 기준으로 삼는 해상도 사이즈는 몇이며 그 이유는 무엇인가요?

1023~ (태블릿)
767~640 (태블릿+확장형 디바이스)
639~480 (확장형+기본형 디바이스)
479~320 (기본형 휴대폰)

16. :first-child와 :last-child가 지원하는 IE의 버전명을 적어보세요.

ie 9 / ie 8은 first-child(css2.1) 지원

17. 포토샵(또는 다른 그래픽툴)에서 이미지를 자를 때 어떤 기능을 사용하나요? (메뉴명, 단축키 등)

알트 + 우클릭 > 컨트롤 + 레이어클릭 >  컨트롤 (쉬프트) + C > 컨트롤 + n + 엔터 > 컨트롤 + v
(…)

18. jpg, gif, png의 차이점을 설명해보세요.

jpg - 손실 압축 방식
원본에 손상을 가해 이미지의 용량을 줄이는 트루컬러(24비트) 색상 지원
gif - 비손실 압축 방식
포맷자체는 비손실이나, 하나의 이미지에 저장 가능한 색상이 256 색으로 제한되어 246이상의 색을 가진 이미지는 어쩔 수 없이 손실이 발생한다.
png - 비손실 압축 방식
비손실이며 트루 컬러-24비트를 지원하기 때문에 원본을 손상없이 그대로 저장할 수 있다.
또한, gif의 단색 투명층이 아닌 8비트 알파 채널을 통한 투명층을 지원하기 때문에 이미지의 정밀한 색상과 투명을 지원한다. 단순한 패턴에는 높은 압축 효율을 보여주지만, 다양한 색상과 명도를 가진 이미지에서는 압축 효율이 좋지 못하다. )

19. 가상컨텐츠(:before, :after)는 어떤 용도로 사용할까요?

문서의 구조에 영향을 미치지 않는정도의 요소일때 사용한다.

20. 블럭요소 안의 어떤 자식 요소를 정중앙에 놓는 방법을 알고 있습니까?

+ 1. 부모 element 가 높이값이 존재할 경우 position 을 사용하여
+ 2. 자식 element 와 형제 element 가 존재할 경우 display: table; 사용
