# 3월 7일 학습 및 복습 내용

## 1. CSS 개념 복습

1. line-height : 행간을 설정, 주로 40px~50px을 사용하는 것 같음

<br>

2. word-break : 문서가 길어 줄바꿈이 일어날때, 끊어지는 기준을 정해줌 
- break-all : 단어에 관계없이 끊어지는대로 줄바꿈을 해줌, 영어는 default, **한중일은 설정해야함**
- keep-all: 줄의 마지막 단어를 기준으로 줄바꿈이 일어남, 한중일이 default, **영어는 설정해야함**

<br>

3. text-overflow : 텍스트가 넘쳤을때, 말줄임을 통해 보다 깔끔하게 정리해줌
- 한줄정리
```
    white-space:nowrap;
    overflow:hidden;
    text-overflow:ellipsis;
```

- 멀티
```
  overflow:hidden;  
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: n;
```

<br>

4. 가상 클래스 선택자

- :first-child : 형제요소 중 가장 처음에 나오는 요소

- :last-child : 형제요소 중 가장 마지막에 나오는 요소

- :nth-child(n) : 형제요소 중 n번째 요소, n에는 변수나 even, odd도 올 수 있음

- :nth-of-type : 형제요소 중 요소의 타입을 기준으로 요소 선택

- :only-of-type : 동일한 형제요소가 없는 유일한 요소들을 선택

- :not(n) : n이 아닌 요소를 선택해주는 선택자
```
p :not(:first-child){
    font-size:20px;
}
```

<br>

- :root : html, 전역 변수를 선택할때 사용
```
:root {
  --main-color: hotpink;
  --pane-padding: 5px 42px;
}
```

<br>

5. **가상 요소: 선택자에 추가하는 가상의 요소**

- before:: : 선택자의 앞부분에 영향을 줌

- after:: : 선택자의 뒷부분에 영향을 줌


<br>

6. 선택자 우선순위

- 후자우선의 원칙 : 같은 선택자에 동일한 속성의 경우, 나중에 작성한 속성을 따름
```
p {
            color: blue;
            color: red;
        }   // p태그는 red
```
<br>

- 가중치 우선순위: 구체적일수록 우선순위가 높아짐
```
1. inline 속성
2. id(#)
3. class(.), 가상클래스, 속성선택자
4. tag, 가상 요소 선택자
5. 전체 선택자(*)
```

- !important : 모든 순서를 무시하고 제일 우선순위가 됨 -> 쓰지마라, 자연스러운 상속을 다 깨기에 좋은 습관이 아님

<br>

7. 이미지 비율 유지하기

- aspect-ratio : 기본 이미지의 가로와 세로 비율을 설정 + object-fit : cover; 를 같이 써서 비율유지

```
img {
    width: 300px;
    aspect-ratio: 288/194;
    object-fit : cover;
}
```

<br>

- paddig % : padding-top 과 padding-bottom의 %r값은 부모의 가로 너비를 기준으로 함

<br>

8. CSS Box Model : HTML요소를 감싸는 상자, 밖에서부터 margin, border, padding, 요소로 구성됨

- margin : 가장 밖의 부분으로 육안으로는 보이지 않음, 단축 속성으로 위, 오른쪽, 아래, 왼쪽 순으로 단축되어 있음

```
// 가운데 배치
p {
    width: npx;
    margin: auto;
}
```

<br>

```
// 왼쪽 배치
p {
    width: npx;
    margin: auto auto auto 0;
}
```

<br>

- 마진 병합 현상: 요소와 요소 사이에 margin-top과 margin-bottom이 겹친경우, 더 높은 값으로 합쳐지는 현상 /  부모 요소와 자식 요소가 존재할 때, 자식 요소의 마진 탑 혹은 마진 바텀 값이 부모의 높이에 영향을 미치지 않는 현상

```
// 마진 병합 현상 해결책
1. 부모요소에 overflow 속성 값을 적용(보통 overflow: hiddden을 씀)
2. 부모요소에 display: inline-block 적용
3. 부모요소에 border 값 적용
```

<br>

- border : CSS box의 테두리를 지정, 단축속성으로 테두리의 두께, 스타일, 색상 순으로 단축되어 있음

- box-sizing: border-box : width,height에 border과 padding 값 포함됨, 주로 블럭 요소의 비율을 맞출때 사용

<br>

- padding : border과 요소 사이의 안보이는 거리를 나타내는 단축 속성
```
p{
	padding: 10px; /* top, right, bottom, left 모두 10px */
	padding: 10px 20px; /* top, bottom :10px,  left, right:20px */
	padding: 10px 20px 30px; /* top:10px, left,right:20px, bottom:30px */
	padding: 10px 20px 30px 40px;
}
```


