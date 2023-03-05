# 3월 2일 학습내용

## 1. README.md 파일 만드는 코드(Git Bash)

```
$ touch README.md
$ git status # Untracked 확인
$ git add README.md
$ git commit -m "메시지"
```
---------
<br>

## 2. 수업 중 필기한 개발자 팁

- 폴더나 파일의 이름을 정할때: 공백없이 **영문 소문자**로 작성하고  언더바 대신 **하이픈(-)** 사용

- 어지간하면 속성값에 ""을 붙이는 습관을 들일 것

- 주석 다는 에티켓
```
// 태그의 시작과 끝을 적어놓기
<!-- header -->
<header>
	...생략...
</header>
<!-- //header -->
```
<br>

```
// 협업할 때
<!-- 메뉴 토글 class="active" 유/무로 제어 -->
<nav class="active">
	...생략...
</nav>

<!-- #2022.02.20 업데이트 -->
```

<br>

- 마크업 오류를 예방하기 위한 사이트 숙지 할 것: [Validation](https://validator.w3.org/)

-------------------------------

<br>


## 3. HTML(HyperText Markup Language)

1. HTML의 정의 : 텍스트를 매우 효율적이게 나타낼 수 있는 *마크업 언어(태그를 이용하여 사용하는 문법, 프로그램 언어는 아님)*

                웹 콘텐츠의 의미와 구조를 정의

2. HTML의 기본 구조 :

```
<!DOCTYPE html> <!--"이 문서는 html Living Standard 문서!"라는 의미-->
<html lang="en">  <!--HTML 문서의 루트, 최상단 요소-->
<head>  <!--검색엔진을 위한 다양한 정보들이 담김, 사용자에게 title,파비콘이 보임-->
    <meta charset="UTF-8">  <!--UTF-8: 세계 어떤 언어도 다 사용가능하게 함 -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge">  <!--최신 표준 모드를 보여주겠다는 의미-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  <!--name:문서 레벨 데이터, 데이터 이름 알려줌 / content: 데이터 내용 설명-->
    <title>Document</title> <!--title: 간결하게 텍스트만 포함, 적당한 제목으로 설정, 60자를 넘지 않아야 함-->
    <link rel="stylesheet" href="001.css"> <!--rel: relations 관계. 대상 파일의 속성을 나타냄, href :  hyper-references 경로. 연결 시 참조할 파일의 위치를 나타냄  --> 
    <style> 
        html {                  
            font-size: 1rem;
        }
    </style> <!--HTML내에서 스타일에 영향을 줌-->
</head>
<body>   <!--HTML의 내용을 담당(각종 정보나 동작을 담고 있음)-->
    <div>
        <p>hello</p>
    </div>
</body>
</html>
```

<br>


## 4. Tags related to Texts(HTML)

- `<h1>` : Heading 태그, 제목 태그 -> 목차이기에, 사용자가 정보를 수월하게 가져갈 수 있게 함으로 중요함, *h1 ~ h6 순서대로 작성할 것*

- `<a>` : href로 속성을 나타내고, target으로 속성값을 나타냄

```
// 연락처를 링크 걸때 : tel을 사용
<a href="tel: 010-0000-0000">연락처</a> 

// 이메일 주소를 링크 걸때 : mailto를 사용
<a href="mailto: wswm2008@naver.com">이메일 주소</a>

// 다른 웹브라우저를 링크 걸때 : target="_blank"를 사용
<a href="002.html" target="_blank">002.HTML</a>

// 다른 웹브라우저를 다운 받을 때: download를 사용
<a href="002.html" download>다운로드</a>
```

<br>

- `<p>` : 문단을 의미, 아주 빈번하게 사용된다.


- `<br>` : 줄 바꿈 태그이지만, 여러번 쓰는 것을 지양하고, 어지간하면 CSS 사용을 권장

- `<wbr>` : `<span>`으로 감싼 태그를 기준으로 줄 바꿈이 적용

```
//CSS 기준
.ex1 span{
    display:inline-block;  // span 태그를 기준으로 줄 바꿈이 생김
  }
  .ex2 span{
    display:block;          // 기준이 사라짐
  }
  
  @media (max-width:1000px){
    .ex2 span{
      display:inline;
    }
  }
  p{
    font-size:60px;
  
  }
  
  .ko{
   word-break:keep-all;     // 한글은 해당 속성과 함께 작성해야 작동함
  }
```

<br>


- `<code>` : 코드 한 조각을 나타낼때 사용
```
<code>push()</code>
```

<br>

- `<pre>` : HTML에 작성한 내용을 그대로 가져옴(공백, 고정폭 그대로 유지) 
```
<figure role="img" aria-labelledby="caption">  // <figure>을 이용하여 아래 설명란 작성(참고)
  <pre>
  ⊂_ヽ
    ＼＼  Λ＿Λ
     ＼( ‘ㅅ’ ) 두둠칫
      >　⌒ヽ
     / 　 へ＼
     /　　/　＼＼
     ﾚ　ノ　　 ヽ_つ
    /　/두둠칫
    /　/|
   (　(ヽ
   |　|、＼
   | 丿 ＼ ⌒)
   | |　　) /
  `ノ )　　Lﾉ
  </pre>
  <figcaption id="caption">
    토끼 인간이 두둠칫 두둠칫 동작을 하고 있습니다.
  </figcaption>
</figure>
```

<br> 

- `<strong>` : 기본적으로 굵은 글씨, 스크린 리더를 사용할때 강조된 어조로 말하게 만듦, 적극 권장
```
<strong>아! 화장실!!</strong>
```

<br>

- `<q>` : 출처 + 짧은 인용문을 나타냄
```
<q cite="https://www.imdb.com/title/tt0062622/quotes/qt0396921">
		I'm sorry, Dave. I'm afraid I can't do that.
	</q>
```

<br>


- `<blockquote>` : 긴 인용문을 나타냄
```
        <blockquote>
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam nam laborum dolorum nostrum delectus cum natus consectetur ipsa, provident porro! Perferendis praesentium inventore modi ipsum rem quam enim voluptate soluta.
            </p>
        </blockquote>
        <cite>--Me--</cite>
```

<br>

- `<cite>` : 저작물의 출처를 표기, 제목이 반드시 들어가야 함

```
<cite>— 어린왕자 여우의 말 중</cite>
```

<br>

- `<address>` : 연락처 정보를 작성하는 태그 / 물리적 주소나 URL, 이메일 주소, 전화번호 등등/  **이름을 반드시 포함 해야함**
```
  <p>My-tel: <address>010-****-****</address></p>  // 한 줄로 나오게 하는법 배워둘 것
```
<br>

- `<mark>` : 하이라이트를 해주는 태그/ 색상은 CSS에서 background로 주면 됨.
```

```

<br>

- `<abbr>` : 약어(줄임말)를 나타내는 태그 / title: defintion
```
<abbr title="메소 획득량">메획</abbr>
```

<br>

- `<dfn>` : 맥락에서 정의하는 용어를 감싸는 태그/ 보통은 a 태그와 함께 써서 용어에 대한 자세한 설명으로 링크시킴
```
<p>
    <dfn id="maso">
        <abbr title="메소 획득량">메획 : </abbr>
    </dfn>
    메소를 얻을 수 있는 양을 의미합니다.
</p>
```

<br>

- `<sup>` : 위에 표시되는 지수나 서수와 같은 첨자 표현하는 태그 / 위에 표시 되는 것

```
<p>Hunting <sup>3hr</sup></p> 
```

<br>

- `<sub>` : text which goes under the main text / Lower one

```
<p>Lanking <sub>4th</sub> </p>
```

<br>

- `<kbd>` : text describing KeyBoard's keys

```
<p><kbd>cntl</kbd> + <kbd>v</kbd> = Copy Things </p>
```

<br>

------------


## 5. Tags related to List(HTML)

1. ol(ordered list ) : List which is ordered in Numbers, The order is important!

- start : fix the strarting Number

- reversed : reverse the ordered Numbers

```
<ol>
        <p>How to make Soup</p>
        <li>Boil 50ml water for 5min</li> 
        <li>Put ingrediants in the pot</li>
        <li>Boil for 30min</li>
        <li>Add papper or other stuff for free</li>
    </ol>

    <ol start="4">  // starts with 4
        <li>one</li>
        <li>two</li>
        <li>three</li>
        <li>four</li>
        <li>five</li>
    </ol>


    <ol reversed>  // reversed
        <li>one</li>
        <li>two</li>
        <li>three</li>
        <li>four</li>
        <li>five</li>
    </ol>
```

<br>

- **BreadCrumbs : List which helping for find ordered Web Sites**

<br>

2. `<ul>` : Unordered List, Ordering with dots which are *Not* Numbers, Use it when the order isn't important

```
    <ul>  // ordered with dots
        <li>one</li>
        <li>two</li>
        <li>three</li>
        <li>four</li>
    </ul>
```

<br>

```
    <ol type="I"> <!--Large Roman Numbering--> 
        <li type="1">item</li>  <!--Default Number-->
        <li type="i">item</li> <!--Small Roman Numbering-->
        <li value="3">item</li>  <!--Tell the order in this line-->
    </ol>
```

3. `<li>` : **Use for ol and ul's child Only**

```
<ol>
	<div>item</div> // Can't Use
	<li>item</li>
	<li>item</li>
</ol>
```

<br>

4. `<dl>` : Definition list, Usally use in Dictionary

```
    <dl>
        <dt>Slime</dt>  <!--Definition title-->
        <dd>The Monsters which are sticky designed  <!--Defintion Detail--></dd>
    </dl>
```
















