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


3. HTML의 핵심 태그(텍스트 태그)

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





