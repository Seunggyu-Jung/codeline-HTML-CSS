# 3월 3일 학습내용 

## 1. CSS 정의 : Cascading Style Sheets, HTML 스타일이나 레이아웃을 꾸밀때 사용

<br>


## 2. CSS 선택자 
- `Selecter {}` : CSS 스타일을 적용할 요소를 대괄호로 앞에 작성  

- `* {}` : 전체 선택자, 문서안의 모든 요소를 가르킴
```
* {
            color: aqua;
         }
```

<br>

- `h1 {}` : 타입 선택자(태그 선택자, 요소 선택자), 특정 태그를 선택해줌

```
h1 {
            background: red;
         }
```
<br>

- `#id {}` : 아이디 선택자, **id는 HTML문서상 유일함**

```
#id {
    color: red;
}
```

<br>

- `.class {}` : 클래스 선택자, 한 페이지에 여러 선택자들이 올 수 있음

```
.class {
    padding : 10px
}
```

<br>

- `[] {}` : 특성 선택자, 문서내 해당 특성(type, class)을 지닌 요소들을 선택함

```
[type="button"] {
    padding : 10em;
}

[class^="hole"] {  /* ^= a : a 로 시작하는 모든 것 */
    color: salmon;
}
```
<br>

- `, {}` : 그룹 선택자, 여러 그룹들을 선택함

```
h1, h2, h3 {
    font-size: 1em;
}
```

<br>

- 복합 선택자 : 요소의 족보를 이용하여 선택함

```
div p {     /*자손 선택자(공백)*/
    font-weight: 20px;
}
```
<br>

```
div > p {       /*자식 선택자(>)*/
    font-size: 20px;
}
```

<br>

```
h1~p{  /*일반 형제 선택자(~)*/
    text-decoration: underline;
}
```

<br>

```
h1 + p {    /*인접 형제 선택자(+)*/
    background : red
}
```

<br>

## 3. CSS 상속 : 부모 요소의 CSS를 자식 요소가 상속 받는 것을 의미

- **상속이 되는 속성이 있고 안되는 요소도 있으니 주의!!** : `width`, `height` , `margin`, `padding`, `border`

- **상속 할 수 없는 태그 또한 존재** : `button`, `input`

<br>

- `inherit` : 상속을 받는 자식요소가 CSS의 속성에 상속이라 작성하면 상속받음

```
section {
    color: salmon;
}

p {
    color: inherit;
}
```

<br>


## 4. 단위

- px : 디바이스 화면에 표시되는 가장 작은 단위, 디바이스별 단위가 상이하기에 안쓰는 것을 권장

- % : 부모 요소를 기준으로 하느 ㄴ







