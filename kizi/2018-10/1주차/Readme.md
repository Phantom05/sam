## HTML, 태그

* a태그
```
  <a href=""></a>
  <a href="" download></a>
  <a href="document.html" rel="alternate">외부 link</a><br>
  <a href="" rel="bookmark">bookmark</a><br>
  <a href="" target="_blank">bookmark</a><br>
  <a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">Send Mail</a><br>
  <a href="tel:+4733378901">+47 333 78 901</a><br>
  <a href="javascript:alert('Hello World!');"></a><br>
```

* abbr 태그
```
<abbr> 태그는 "Mr.", "Dec", "ASAP", "ATM"과 같은 약어 또는 머리 글자를 정의합니다.
```

* address 태그
```
<address> 요소의 텍스트는 대개 이탤릭체로 표시 됩니다. 대부분의 브라우저는 주소 요소 앞뒤에 줄 바꿈을 추가합니다.
```

* article
```
<article> 태그는 독립적 인 독립 컨텐츠를 지정합니다.

기사는 독자적으로 이해해야하며 나머지 사이트와 독립적으로 기사를 배포 할 수 있어야합니다.

<article> 요소에 대한 잠재적 인 출처 :

포럼 게시물
블로그 게시물
뉴스 기사
논평
```

* aside
```
<aside> 태그는 배치 된 내용을 제외하고 일부 내용을 정의합니다.

별도의 콘텐츠는 주변 콘텐츠와 관련되어야합니다.
보통 사이드바 메뉴로 많이 사용합니다.
```

* audio
되도록 mp3만 사용하는게 좋음. wav나 ogg는 익스플로우나 사파리를 지원하지 않음.

* b
```
b태그는 html5부터 css와 html을 완전히 분리하는 업데이트가 진행됨으로 스타일 이 들어간 태그는 사용하지 않는게 좋음. 최후의 수단으로만 사용 할 것! html5에서 간간히 사용되고 있으나 매우 좋지 않음! 또한 스크린 리더기에 시각 효과만큼 읽히지가 않음. strong은 강조라고 읽히나 b는 그냥 일반 텍스트로 읽힘
```
* base
```
<base> 태그는 문서의 모든 상대 URL에 대한 기본 URL / 대상을 지정합니다.

문서에는 최대 하나의 <base> 요소가있을 수 있으며 <head> 요소 내에 있어야합니다.

target속성도 선택할 수 있음.
```

* blockquote
```
<blockquote> 태그는 다른 소스에서 인용 된 섹션을 지정합니다.

브라우저는 일반적으로 <blockquote> 요소를 들여 쓰기합니다.
```




html은 하이퍼 텍스트 마크업 랭귀지죠. CSS는 그 HTML이 어떻게 '나타나는가'에 대한 문서구요.

예를 들어 누군가가 html에 어떤 행사의 '식순'을 적어주면 CSS를 통해서 그 식순에 꽃무늬 테두리를 두르거나, 순서에 '번호'를 먹이거나 아니면 그냥 '점'만 찍거나 등의 '표현'을 제어할 수 있는 거죠.

그러면 '분리'를 통해서 얻을 수 있는 이득이란?

예를 들어 html에서 서론, 본론, 결론이 있는 글을 썼다고 해요. 그런데 각각 '서론', '본론', '결론'에 해당하는 것의 글자 크기를 동일하고 같은 글꼴을 쓰려고 html의 '형식'을 같게 해둔다면. CSS에서 한 번 고치는 것으로 '서론', '본론', '결론' 세 가지를 바꿀 수 있게 되는 거죠.

만약에 '태터툴즈'의 스킨이 아니라 웹페이지라면, 그리고 그 페이지가 '여러 문서'이고, 형식이 '같은 것'으로 이루어져 있다면.

CSS 파일 하나 손 보는 것으로 모든 페이지의 '모습'이 바뀌는 겁니다.



## !DOCTYPE html


<! DOCTYPE> 선언은 HTML 문서에서 <html> 태그보다 먼저 있어야함

<! DOCTYPE> 선언은 HTML 태그가 아닙니다. 페이지가 쓰여지는 HTML의 버전에 대한 웹 브라우저의 지시

독타입 설정은 해당 독타입으로 랜더링 하겠다는 브라우저와의 약속임.

HTML5는 SGML을 기반으로하지 않으므로 DTD에 대한 참조가 필요하지 않음 DTD는 아래 버전들에 w3c 사이트에 종속되어 표기됨.

: HTML 문서에 항상 <! DOCTYPE> 선언을 추가하면 브라우저가 예상 할 문서 유형을 알 수 있음
//표기 하지 않아도 되는데 브라우저의 접속, 위치, 상대적으로 종속됨.

* HTML 5
```js
<!DOCTYPE html>
```
* HTML 4.01 엄격
```js
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```
* HTML 4.01 과도기
```js
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

* HTML 4.01 프레임 세트
```js
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
```

* XHTML 1.0 Transitional
```js
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

* XHTML 1.1
```js
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```

# data- 속성

>HTML data- * 속성
```
<ul>
  <li data-animal-type="bird">Owl</li>
  <li data-animal-type="fish">Salmon</li> 
  <li data-animal-type="spider">Tarantula</li> 
</ul>
```

data- * 속성을 사용하면 모든 HTML 요소에 맞춤 데이터 속성을 포함 할 수 있습니다.

저장된 (사용자 정의) 데이터는 페이지 JavaScript에서 사용되어 Ajax 호출이나 서버 측 데이터베이스 쿼리없이보다 매력적인 사용자 환경을 만들 수 있습니다.

>data- * 속성은 두 부분으로 구성됩니다.

속성 이름은 대문자를 포함해서는 안되며 "data-"접두어 다음에 적어도 하나 이상의 문자가 있어야합니다.
속성 값은 임의의 문자열이 될 수 있습니다.
주 : 접두사가 "data-"인 사용자 정의 속성은 사용자 에이전트가 완전히 무시합니다.

>contenteditable 속성은 브라우저에서 클라이언트가 직접 글을 수정할 수 있게 해줍니다.

```
  <p contenteditable="true">안녕하세요.</p>
```

>dir 속성은 글자의 방향을 선택할 수 있다. text-ailgn의 효과
```
<element dir="ltr|rtl|auto">
```
HTML5에서 dir 속성은 모든 HTML 요소 에서 사용할 수 있습니다 (HTML 요소에서 유효성을 검사하지만 반드시 유용하지는 않습니다).
```
HTML 4.01에서는 <base>, <br>, <frame>, <frameset>, <hr>, <iframe>, <param> 및 <script>에 dir 속성을 사용할 수 없습니다.
```
> hidden 속성


>tabindex
탭을 이용하여 이동할 수 있게 해준다


# html 이벤트 속성
> onafterprint
```
<body onafterprint="myFunction()">
```
페이지 인쇄가 시작되거나 인쇄 대화 상자가 닫힌 경우 JavaScript를 실행합니다.

> onbeforeprint
```
<body onbeforeprint="myFunction()">
```

> onbeforeunload 

```
<body onbeforeunload="return myFunction()">
```
확인 상자에 나타나는 기본 메시지는 브라우저마다 다릅니다. 그러나 표준 메시지는 "이 페이지를 종료 하시겠습니까?"와 같은 메시지입니다. 이 메시지는 제거 할 수 없습니다.

> onerror
```
<img src="image.gif" onerror="myFunction()">
```
미지를로드 할 때 오류가 발생하면 JavaScript를 실행합니다.

> onload
onload 속성은 객체가로드 될 때 발생합니다.

onload는 웹 페이지가 이미지, 스크립트 파일, CSS 파일 등 모든 내용을 완전히로드 한 후에 스크립트를 실행하기 위해 <body> 요소에서 가장 자주 사용됩니다. 그러나 다른 요소에서도 사용할 수 있습니다 (아래의 "지원되는 HTML 태그"참조).


>onresize
브라우저 창 크기를 조정하면 onresize 속성이 실행됩니다.



# 반응형, 적응형
>반응형

하나의 틀에서 물흐르듯이 미디어 쿼리를 이용
창을 줄일떄 애니메이션 효과
유동적

> 적응형

역시나 미디어 쿼리를 이용하여 만들지만,
미리 값을 정해놓고 그안에다가 모두 집어넣어 만듬
-고정폭, 위치 디자인들이 기준이 되는 넓이값을 만났을때 적용됨.
-뷰를 정해둔 상태에서 작업
