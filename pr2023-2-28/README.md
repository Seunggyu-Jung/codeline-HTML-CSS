# 2월 28일 학습내용



## 1. URL, IP, PORT 개념 

### 1. IP : 웹브라우저가 지닌 주소를 의미  


```
클라이언트 -> 공유기 -> 라우터 - > DNS(도메인 네임 서버) -> 라우터 -> 공유기 -> 클라이언트 
-> 공유기 -> 각종 보안 및 네트워크 장비 -> 서버 -> DB -> 웹브라우저에 표시
```


```
택시 승객이 택시 기사에게 목적지의 도로명 주소를 알려줌 -> 택시기사가 내비게이션에 주소입력 ->
-> 내비게이션이 택시기사 안내 -> 택시 승객이 해당 목적지에 도착
```

- 택시 승객 = 클라이언트

- 택시 기사 = 라우터

- 내비게이션 = DNS, 서버

- 목적지 = URL

- 도로명 주소 = IP


### 2. PORT : 문(Door) 

- 클라이언트가 들어갈 여러 URL중 들어갈 최종 목적지를 표시

```
http://paullab.synology.me:5000/ 에서 5000이 port(문)
```


- 대표적인 port 종류 

#### 1. 80번 : http

#### 2. 443번 : https

----------


## 2. GitHub


### 1. GitHub를 쓰는 이유:

- 저장용량: 저장용량이 상당하기에 프로젝트를 작업하는데 용이함

- 협업에 용이: 접근성이 탁월하며, 보다 간편한 공유환경을 제공

- 효율적인 관리: 변경내용이나 피드백을 바로바로 작성하고 확인할 수 있어 효율적임



### 2. GitHub에서 주로 쓰이는 Git Bash 문법


- git pull : GitHub에 최신 업로드 된 사항을 내 컴퓨터내 파일로 받아오는 역할을 함


- git add . : 내 컴퓨터로 수정한 사항을 GitHub에 올릴 준비를 함


- git commit -m '메세지' : GitHub에 수정본을 올리면서 올릴 메세지를 작성함


- git push : GitHub에 수정본을 올리는 역할을 함


- shift + insert : Git Bash에 붙여넣기를 하는 단축키


- clear : Git Bash에 작성된 내용을 지워줌 (단, 초기화는 아님)


---------------


## 3. 핵심적인 HTML 문법 요약집

-    ! + Tab : 기본적인 HTML 틀을 작성해줌

-   h1 + Tab : h1 태그 자동완성

-   h1{hello world} + Tab : hello world가 들어간 h1태그 자동완성 

-   h1+p + Tab : h1태그와 p태그를 동시에 자동완성

-   h$*6 + Tab : h1 ~ h6태그 자동완성

-   p#hello + Tab : id가 hello인 p태그 자동완성

-   p.hello + Tab : class가 hello인 p태그 자동완성

-   p#hello1.hello2 + Tab : id가 hello1이고, class가 hello2인 p태그 자동완성

-   p.one.two.three + Tab : class가 one two three 인 p태그 자동완성

-   table>(tr>td*6)*4 + Tab : 테이블 자동생성

-   ul>li*5 + Tab : ul리스트 생성

-   ul>li.item$*5 + Tab : class가 item인 list 5개가 담긴 ul태그 자동완성
    
-   lorem : 막말 생성기(치기만 하면 나옴)

-   lorem5 : 단어 5개 생성
    
-   lorem*3: 문장 3줄 생성

----------------------

## 4. 자주 사용하는 VSC 단축키


- 모든 단축키 : `Ctrl + K + S`

- Settings : `Ctrl + ,` (오른쪽 상단에 Settings.json file open으로 좀 더 다양한 커스터마이징 가능)

- Sidebar : `Ctrl + B`

- Terminal : `Ctrl + Shift + `` (백틱, 틸트, 템플릿리터럴)

- Command palette : `Ctrl + Shift + P, F1`

- 동시 선택 : `Ctrl + D` (2번 입력, `Ctrl + Shift + D`와 같은 역할)

- 동시 수정 : `Ctrl` + `Alt` + `방향키(상, 하)`, `Alt + Click`, `Alt + Shift + Drag`, `Alt + Shift + i`

- Quick Open : `Ctrl + P`

- 문장의 양 끝 : `Home` / `End`

- 코드의 양 끝 : `Ctrl + Home` / `Ctrl + End`

- 복사 / 붙여넣기 : `Ctrl + C` / `Ctrl + V` / `Alt + 방향키(위, 아래)`

- 단어 복사 : `Ctrl + Shift + 방향키(위, 아래)`

- 주석 : `Ctrl + /`

- 들여쓰기 / 내어쓰기 : `Ctrl + [` / `Ctrl + ]`, `tab`, `shift + tab`

- 한 줄 삭제 : Shift + Del

- 파일 생성 : Ctrl + N

