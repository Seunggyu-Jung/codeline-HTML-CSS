# 3월 8일 학습내용

## 1. flex

1. flex : diplay의 한 종류로, 보다 유동적이고 유지보수에 용이하며, 주로 1차원적 레이아웃을 다루기 위해 사용함, **반드시 부모요소와 자식요소로 나뉘어야 함**

- flex-container : flex에서 부모요소로, flex를 적용할 배경역할을 함

- flex-item : flex에서 자식요소로, flex로 작동할 요소들을 의미

- flex는 주축과 교차축으로 설정되어 있으며, 주축은 justify-content로, 교차축은 aligin-items로 변화를 준다.

<br>

2. flex-direction : flex-container에서 flex-item들이 들어갈 주축을 결정함

- row : 가로를 기준으로 왼쪽에서부터 오른쪽 방향으로 간다.

- colum : 세로를 기준으로 위에서 아래 방향으로 간다.

- row-reverse : 가로를 기준으로 오른쪽에서 왼쪽 방향으로 간다.

- colum-reverse : 세로를 기준으로 아래에서 위로 간다.

<br>

3. justify-content : 주축을 기준으로, 아이템들의 위치나 간격을 조절할때 사용하는 속성

- flex-start: 주축이 시작하는 곳으로 정렬

- flex-end: 주축이 끝나는 곳으로 정렬

- center : 가운데 정렬

- space-between : 아이템의 시작과 끝을 양끝에 고정하고, 일정 간격만큼 떨어뜨리는 정렬

- space-around : 양끝에 일정간격을 때고, 아이템을 일정간격만큼 떨어뜨리는 정렬

<br>

4. align-items, align-content : 교차축을 기준으로, 아이템의 위치나 간격을 조절할때 사용하는 속성

- align-items: 아이템이 단수일 경우 사용

- align-content: 아이템이 복수일 경우 사용

<br>

5. flex-wrap : 한 줄에 배치되게 하거나, 가능 범위내에서 여러 행으로 배치되게 하는지를 결정

6. flex-flow : flex-direction, flex-wrap 순의 단축 속성
```
    flex-flow: colum wrap;
```

<br>

8. flex-basis : flex-items의 초기 크기를 설정하는 속성으로, row일 경우 item의 width 값이 무시당하고, colum일 경우 item의 height 값이 무시당함

9. flex-grow : 아이템이 컨테이너 내부에서 늘어날 수 있는 공간의 범위를 지정, 같은 형제 요소들이 같은 값을 가지면 내부에서 일정한 공간을 나눠가짐

10. flex-shrink : 아이템의 크기를 고정하거나 축소를 하는데 사용, 반응형에 용이하게 해줌

<br>

--------------

<br>

## 2. grid

1. grid : flex와 유사하지만, 2차원으로 레이아웃을 만들기에 더욱 직관적인 디스플레이 표현방식이다.
- grid-container : grid의 부모요소를 나타냄
- grid-item : grid-container의 자식요소를 나타냄
- grid cell : grid의 한 칸을 의미
- grid track : grid의 row나 colum을 가리킴
- **grid number** : grid line의 각 번호로, 이를 조합하여 단축속성을 읽는 법 숙지할 것
- grid area : grid cell의 집합을 의미

<br>

2. grid-container가 사용하는 속성

- grid-template-colums : grid에서 열의 개수와 간격을 나타냄(열방향 트랙 사이즈)

- grid-template-rows : grid에서 행의 개수와 간격을 나타냄(행방향 트랙 사이즈)

- **fr** : 컨테이너를 분할하는 비율로, 보다 유연한 길이 단위

- repeat(a,b) : 트랙 사이즈를 나타내는 함수로, a에는 반복할 횟수, b에는 반복할 사이즈를 작성 / 사이즈가 전부 같아야 사용가능

- minmax(a,b) : 트랙 사이즈의 최솟값(a)와 최댓값(b)을 나타냄, 반응형을 보다 유용하게 처리하도록 지원하는 함수

- auto-fill : repeat() 함수의 반복 횟수로 들어가는 속성으로, 컨테이너 안에 공간이 남을 경우, 그대로 방치함

- auto-fit : auto-fill의 반대로, 컨테이너 안에 공간이 남을 경우, 그 공간을 셀들이 나누어 가짐 / 주로 이걸 많이 사용함

<br>

3. grid-item이 사용하는 속성

- grid-area : **grid track의 사이즈를 나타내는 단축속성으로, grid-row-start / grid-colum-start / grid-row-end / grid-colum-end 순으로 나타냄**
```
grid-row-start : 1;
grid-row-end : 3;
grid-colum-start: 2;
grid-colum-end: 3;

grid-area: 1/2/3/3
grid-area: 1/2/span 3/span 3  // span n: n칸만큼 공간을 차지한다는 것을 의미  
```

<br>

- grid-template-areas : grid의 영역을 직접 행렬로 나타내는 속성, 이때 grid-item들은 각자 고유한 grid-area를 가져야 함(단, 숫자는 불가능)

```
.container {
    grid-template-areas:
    "a b b"
    "a b b";
}

.itemA {
    grid-area: a; // class가 itemA인 item의 grid-area 값은 a이다.
}
```

<br>

4. grid 단축속성 : 요거 질문 할 것.

