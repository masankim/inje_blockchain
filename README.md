#### 형상관리프로그램을 설치한다.

https://git-scm.com/ 사이트에 접속해서 GIT설치프로그램을 설치한다.

설치한후 CMD창을 전부 껐다가 다시 실행한다.

버전관리를 위해서는 버전관리하고자 하는 폴더로 이동후 GIT명령어중에 초기화 명려어를 이용해서 초기화시켜준다.

```powershell
git init
```

다음과 같은 결과가 나온다.

```powershell
>> Initialized empty Git repository in C:/apps/.git/
```

버전을 관리할 파일을 STATE상에 올려놓는 과정과 COMMIT 하는 과정을 거쳐야 만이 그 파일이 버전이 정해지면서 관리를 할 수 있다.

```powershell
git add .
git commit -m <원하는 메세지>
```



처음 깃을 설치하고 실행을 하게되면 다음과 같은 결과가 나온다.

> > ```powershell
> >  Run
> > 
> >   git config --global user.email "you@example.com"
> >   git config --global user.name "Your Name"
> > 
> > to set your account's default identity.
> > Omit --global to set the identity only
> > ```
> >
> >  



초기에 등록하는 명령어를 이용해서 초기 유저 등록을 마저 해준다

```powershell
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```



등록을 한후 다시한번 git commit 명령어를 실행한다.



```powershell
git commit -m <원하는 메세지>
```



깃을 원격에 등록시켜 놓고 관리한다.

github.com 에 접속하여 회원가입 및 로그인을 한다.

새로운 repository 를 생성한다.



다음과 같은 명령어를 이용하여 원격 github클라우드와 local git 폴더와 연결한다.

```powershell
git remote add origin https://github.com/masankim/inje_blockchain.git
```



branch 생성



```powershell
git branch -M main
```



push 명령어를 이용해서 원격에 올린다.

```powershell
git push -u origin main
```



# HTML

html의 기본구조(interface)는 

```html
<!DOCTYPE html>
<!--이 부분은 주석문입니다. 웹 브라우저는 주석을 화면에 출력하지 않습니다.-->
// 주석처리하는 부분이고 웹브라우저는 주석은 처리하지 않는다.
<html>
    <head>
        //문서의 속성들이나 meta속성들이나 title을 정의한다.
    </head>
    <body>
        //웹브라우저상에서 주소창 밑에 있는 부분을 body라고 이 바디에 표현되는 콘텐츠또는 기능들을 정의한다.
    </body>
</html>
```





#### html 문서는 3가지의  종류로 문서를 작성한다.

HTML , CSS , JAVASCRIPT

CSS :  **Cascading Style Sheets**(**CSS**)는 [HTML](https://developer.mozilla.org/ko/docs/HTML)이나 [XML](https://developer.mozilla.org/ko/docs/XML)([SVG](https://developer.mozilla.org/ko/docs/SVG), [XHTML](https://developer.mozilla.org/ko/docs/XHTML) 같은 XML 방언(dialect) 포함)로 작성된 문서의 표현을 기술하기 위해 쓰이는 [스타일시트](https://developer.mozilla.org/ko/docs/Web/API/StyleSheet) 언어입니다.

JS(JAVASCRIPT) : HTML page를 역동적으로 구현하기위한 기능을 만드는 언어



html_lecture/test2.html 문서를 보면

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        웹 페이지의 구성 요소</title>
    <style>
        body {background-color: linen;
            color: green;
            margin-left: 40px;
            margin-right: 40px;
        }

        h3 {
            text-align: center;
            color: darkred;
        }

        hr {
            height: 5px;
            border: solid grey;
            background-color: grey
        }

        span {
            color: blue;
            font-size: 20px;
        }
    </style>
    <script>
        function show() { // <img>에 이미지 달기
            document.getElementById("fig").src = "ElvisPresley.png"
        }

        function hide() { // <img>에 이미지 제거
            document.getElementById("fig").src = "";
        }
    </script>
</head>

<body>
    <h3 onmouseover="show()" onmouseout="hide()">
        Elvis Presley</h3>
    <hr>
    <div>
        <img id="fig" src=""></div>
    He was an American singer and actor. In November
    1956, he made his film debut in <span>Love Me
        Tender</span>. He is often referred to as
    "<span>the King of Rock and Roll</span>".
</body>

</html>
```



CSS -> <style> 내용 </style>

javascript -> <style>내용</style>

태그를 선언하고 그안에 적는 onmouseover , onmouseout 같은 것을 이벤트리스너 와 id , src와 같은 속성을 적어서 html기능을 추가한다.



#### 메타데이터

데이터의 성질등을 나타내는 데이터 

메터데이터를 정의내리는 태그는 

HTML 페이지에 대한 메타 데이터를 담기 위한 태그들
– <base>, <link>, <script>, <style>, <title>, <meta>

head 태그 안에 위의 태그를 사용한다.

단 script태그는 body태그안에도 사용할 수 있다.







<meta> 태그는 다양한 메타 데이터 표현
– 웹 페이지의 저작자, 문자 인코딩 방식, 내용 등
➢ 웹 페이지의 저작자가 “황기태”임을 표기하는 사례
▪ <meta name="author" content="황기태">
➢ 웹 페이지의 내용 설명
▪ <meta name="description" content="입학 요령에 대한 자세한 사항">
➢ 웹 페이지의 키워드(검색 엔진에 의해 검색되게 하기 위함)
▪ <meta name="keywords" content="컴퓨터, 소프트웨어, 스마트폰">
➢ charset 속성으로 웹 페이지에 사용하는 문자 코드 지정
▪ <meta charset=“UTF-8”>



#### img태그

<img> 태그의 src 속성에 이미지 파일의 주소 지정
• src에 지정할 수 있는 이미지 종류
• BMP, GIF, PNG, JPG(JPEG), animated-GIF

![image-20201211220845454](https://user-images.githubusercontent.com/75194770/101907228-98b9a500-3bfd-11eb-96ca-5fd9478e5edd.png)



##### 경로를 지정할때 " . /" 같은 계층 구조에 있는 파일이나 폴더 경로 

##### "/" 그 폴더안으로 들어가는 경로

##### "../" 경로보다 상위폴더로 이동하는 경로



#### 3 가지 종류의 리스트

– 순서 있는 리스트(ordered list) - <ol></ol>
– 순서 없는 리스트(unordered list) - <ul></ul>
– 정의 리스트(definition list) - <dl></dl>
• 리스트 아이템
– <li>…</li>
– </li> 생략 가능



![image-20201211222148331](https://user-images.githubusercontent.com/75194770/101908350-4bd6ce00-3bff-11eb-8c37-4043340a6041.png)

다음과 같은 샘플 코드를 보면서 이해 할 수 있다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <ol type="A" start="2">
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
      </ol>
      
      <ol start="50">
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
      </ol>

      <ul>
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
      </ul>
</body>
</html>
```



코드를 chrome 브라우저에서 실행시키면서 용도를 이해한다.

### 표 만드는데 사용되는 태그들

<table></table>

####  <table> : 표 전체를 담는 컨테이너

####  <caption> : 표 제목

####  <thead> : 헤딩 셀 그룹

####  <tfoot> : 바닥 셀 그룹

####  <tbody> : 데이터 셀 그룹

####  <tr> : 행. 여러 <td>, <th> 포함

####  <th> : 열 제목(헤딩) 셀

####  <td> : 데이터 셀





다음과 같은 샘플 코드를 보면서 이해 할 수 있다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table style="width:100%">
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Age</th>
        </tr>
        <tr>
          <td>Jill</td>
          <td>Smith</td>
          <td>50</td>
        </tr>
        <tr>
          <td>Eve</td>
          <td>Jackson</td>
          <td>94</td>
        </tr>
</body>
</html>
```

