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
> > Run
> > 
> > git config --global user.email "you@example.com"
> > git config --global user.name "Your Name"
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

<table> : 표 전체를 담는 컨테이너
 <caption> : 표 제목
 <thead> : 헤딩 셀 그룹
 <tfoot> : 바닥 셀 그룹
 <tbody> : 데이터 셀 그룹
 <tr> : 행. 여러 <td>, <th> 포함
 <th> : 열 제목(헤딩) 셀
 <td> : 데이터 셀


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

### 

### if... else 문

## [구문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#구문)

```
if (condition)
   statement1
[else
   statement2]
```

- `condition`

  참 또는 거짓으로 평가되는 [표현식](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Expressions_and_Operators#표현식)입니다.

- `statement1`

  조건이 참으로 평가될 경우 실행되는 문입니다. 중첩된 if구문을 포함하여 어떤 구문이든 쓸 수 있습니다. 다중구문을 사용할 경우  ({ ... })[블럭](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block) 구문 으로 그룹화 하고 실행하지 않으려면 [빈](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/Empty) 구문을 사용합니다.

- `*statement*2`

  이 구문은 조건이 거짓일경우 다른 조항이 있을 때 실행되는 구문입니다. 블록 문과 if문의 중첩을 호함한 모든문이 될 수 있습니다.

## [설명](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#설명)

다중의 if...else 문은 else if 절을 만들기 위해 중첩될 수 있다.
자바스크립트에서는 elseif (하나의 단어) 키워드가 존재하지 않는다.

```
if (조건1)
   명령문1
else if (조건2)
   명령문2
else if (조건3)
   명령문3
...
else
   명령문N
```

아래 작업한 것을 보면,  if문을 중첩 사용하면 들여쓰기된 것이 제대로 보여집니다.

```
if (조건1)
   명령문1
else
   if (조건2)
      명령문2
   else
      if (조건3)
...
```

하나의 절에서 여러개의 명령문들을 실행하려면,  그 명령문들을 그룹화하는 블록 명령문 ({ ... }) 블럭구문을 사용한다.
일반적으로, 블럭구문을 항상 사용하는 것은 좋은 연습입니다. 특히 중첩된 if 문과 관련되어
있는 코드안에서 사용하면 더욱 좋습니다.

```
if (조건) {
   명령문들1
} else {
   명령문들2
}
```

원시 불리언 값인 true (참) 과 false (거짓) 을 불리언 객체의 truthiness (참으로 보이는 것) 과 falsiness (거짓으로 보이는 것)으로 혼동하면 안된다. false, undefined, null, 0, NaN, 또는 빈 스트링 ("") 이 아닌 모든 값, 그리고 false 값인 불리언 객체를 포함하는 모든 객체는 조건으로 사용될 때 [truthy](https://developer.mozilla.org/ko/docs/Glossary/Truthy) 로 간주된다. 예:

```
var b = new Boolean(false);
if (b) // 이 조건은 참으로 보이는 것 (truthy) 이다.
```

## [예시](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#예시)

### [if...else 사용하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#if...else_사용하기)

```
if (cipher_char === from_char) {
   result = result + to_char;
   x++;
} else {
   result = result + clear_char;
}
```

### [else if 사용하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#else_if_사용하기)

자바스크립트에는 elseif 구문이 없다. 그러나, else if 를 사용할 수 있다.

```
if (x > 5) {

} else if (x > 50) {

} else {

}
```

### [조건식의 값을 지정하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else#조건식의_값을_지정하기)

조건식을 단순하게 지정하는 것은 좋지 않습니다.
왜냐하면,  코드를 흘깃 보면 값을 지정한것을 평등한것으로  혼동할 수 있기 때문입니다. 예를들어, 다음코드를 사용하지 마세요:

```
if (x = y) {
   /* do the right thing */
}
```

당신이 조건식에 값의 지정을 해야할 경우, 일반적인 관행은 그 할당된 것 주위에 추가 괄호를 넣어야 합니다. 예를들면:

```
if ((x = y)) {
   /* do the right thing */
}
```



### switch문

expression. It then looks for the first `case` clause whose expression evaluates to the same value as the result of the input expression (using the [strict comparison](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators), `===`) and transfers control to that clause, executing the associated statements. (If multiple cases match the provided value, the first case that matches is selected, even if the cases are not equal to each other.)

If no matching `case` clause is found, the program looks for the optional `default` clause, and if found, transfers control to that clause, executing the associated statements. If no `default` clause is found, the program continues execution at the statement following the end of `switch`. By convention, the `default` clause is the last clause, but it does not need to be so.

The optional `break` statement associated with each case label ensures that the program breaks out of switch once the matched statement is executed and continues execution at the statement following switch. If `break` is omitted, the program continues execution at the next statement in the `switch` statement.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#예제)

### [Using switch](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#Using_switch)

In the following example, if `expr` evaluates to "Bananas", the program matches the value with case "Bananas" and executes the associated statement. When `break` is encountered, the program breaks out of `switch` and executes the statement following `switch`. If `break` were omitted, the statement for case "Cherries" would also be executed.

```
switch (expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Apples':
    console.log('Apples are $0.32 a pound.');
    break;
  case 'Bananas':
    console.log('Bananas are $0.48 a pound.');
    break;
  case 'Cherries':
    console.log('Cherries are $3.00 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    break;
  default:
    console.log('Sorry, we are out of ' + expr + '.');
}

console.log("Is there anything else you'd like?");
```

### [break를 쓰지않으면 어떻게 되는가?](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#break를_쓰지않으면_어떻게_되는가)

If you forget a break then the script will run from the case where the criterion is met and will run the case after that regardless if criterion was met. See example here:

```
var foo = 0;
switch (foo) {
  case -1:
    console.log('negative 1');
    break;
  case 0: // foo is 0 so criteria met here so this block will run
    console.log(0);
    // NOTE: the forgotten break would have been here
  case 1: // no break statement in 'case 0:' so this case will run as well
    console.log(1);
    break; // it encounters this break so will not continue into 'case 2:'
  case 2:
    console.log(2);
    break;
  default:
    console.log('default');
}
```

### [Can I put a default between cases?](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#Can_I_put_a_default_between_cases)

Yes, you can! JavaScript will drop you back to the default if it can't find a match:

```
var foo = 5;
switch (foo) {
  case 2:
    console.log(2);
    break; // it encounters this break so will not continue into 'default:'
  default:
    console.log('default')
    // fall-through
  case 1:
    console.log('1');
}
```

It also works when you put default before all other cases.

### [Methods for multi-criteria case](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#Methods_for_multi-criteria_case)

Source for this technique is here:

[Switch statement multiple cases in JavaScript (Stack Overflow)](http://stackoverflow.com/questions/13207927/switch-statement-multiple-cases-in-javascript)

#### Multi-case - single operation

This method takes advantage of the fact that if there is no break below a case statement it will continue to execute the next case statement regardless if the case meets the criteria. See the section titled "What happens if I forgot a break?"

This is an example of a single operation sequential switch statement, where four different values perform exactly the same.

```
var Animal = 'Giraffe';
switch (Animal) {
  case 'Cow':
  case 'Giraffe':
  case 'Dog':
  case 'Pig':
    console.log('This animal will go on Noah\'s Ark.');
    break;
  case 'Dinosaur':
  default:
    console.log('This animal will not.');
}
```

#### Multi-case - chained operations

This is an example of a multiple-operation sequential switch statement, where, depending on the provided integer, you can receive different output. This shows you that it will traverse in the order that you put the case statements, and it does not have to be numerically sequential. In JavaScript, you can even mix in definitions of strings into these case statements as well.

```
var foo = 1;
var output = 'Output: ';
switch (foo) {
  case 0:
    output += 'So ';
  case 1:
    output += 'What ';
    output += 'Is ';
  case 2:
    output += 'Your ';
  case 3:
    output += 'Name';
  case 4:
    output += '?';
    console.log(output);
    break;
  case 5:
    output += '!';
    console.log(output);
    break;
  default:
    console.log('Please pick a number from 0 to 5!');
}
```

이 예제의 결과:

| Value                                | Log text                          |
| :----------------------------------- | :-------------------------------- |
| foo is NaN or not 1, 2, 3, 4, 5 or 0 | Please pick a number from 0 to 5! |
| 0                                    | Output: So What Is Your Name?     |
| 1                                    | Output: What Is Your Name?        |
| 2                                    | Output: Your Name?                |
| 3                                    | Output: Name?                     |
| 4                                    | Output: ?                         |
| 5                                    | Output: !                         |

### [Block-scope variables within switch statements](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch#Block-scope_variables_within_switch_statements)

With ECMAScript 2015 (ES6) support made available in most modern browsers, there will be cases where you would want to use [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) and [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) statements to declare block-scoped variables.

Take a look at this example:

```
const action = 'say_hello';
switch (action) {
  case 'say_hello':
    let message = 'hello';
    console.log(message);
    break;
  case 'say_hi':
    let message = 'hi';
    console.log(message);
    break;
  default:
    console.log('Empty action received.');
    break;
}
```

This example will output the error `Uncaught SyntaxError: Identifier 'message' has already been declared` which you were not probably expecting.

This is because the first `let message = 'hello';` conflicts with second let statement `let message = 'hi';` even they're within their own separate case statements `case 'say_hello':` and `case 'say_hi':`; ultimately this is due to both `let` statements being interpreted as duplicate declarations of the same variable name within the same block scope.

We can easily fix this by wrapping our case statements with brackets:

```
const action = 'say_hello';
switch (action) {
  case 'say_hello': { // added brackets
    let message = 'hello';
    console.log(message);
    break;
  } // added brackets
  case 'say_hi': { // added brackets
    let message = 'hi';
    console.log(message);
    break;
  } // added brackets
  default: { // added brackets
    console.log('Empty action received.');
    break;
  } // added brackets
}
```

This code will now output `hello` in the console as it should, without any errors at all.

### while 문 

## [문법](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/while#문법)

```
while (condition)
  statement
```

- `조건`

  반복이 시작되기 전에 조건문은 참,거짓을 판단받게 된다. 만약 조건문이 참이라면, while문 안의 문장들이 실행된다. 거짓이라면, 문장은 그냥 while 반복문 후로 넘어간다.

- `문장`

  조건문이 참일 때만 while문 속의 문장들이 실행된다. 반복문 속에 여러개의 문장을 사용하고 싶다면 중괄호 { } 를 통해 문장들을 하나로 묶어야 한다.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/while#예제)

다음의 while문은 n이 3보다 작을 때까지 반복한다.

```
var n = 0;
var x = 0;

while (n < 3) {
  n++;
  x += n;
}
```

반복을 살펴보면, n을 x에 계속 더하게 된다. 그러므로 x와 n 변수는 다음의 값을 갖는다.

- 첫번째 반복; n=1 과 x=1
- 두번째 반복; n=2 과 x=3
- 세번째 반복; n=3 과 x=6

세번째 반복후, n<3 이라는 초건은 더 이상 참이아니가 되므로 반복은 종료된다

### 

### do... while 문

## [문법](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/do...while#문법)

```
do구문
while (조건식);
```

- ### `*구문*`

  테스트 조건이 참일 때마다 한 번이상 실행되는 구문입니다. 만약 루프 내에서 여러 구문을 반복 실행 시키고 싶으시다면, 다음 명령을 사용합니다.

  [block](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/block) 구문을 활용하여 (`{ ... }`) 이런 식으로 그룹화합니다.

- `*조건식*`

  루프가 실행될 때마다 평가되는 식입니다. 만약 조건식이 참으로 평가되었다면, `구문` 이 다시 실행됩니다. 만약 조건식이 거짓으로 평가되었다면, 자바스크립트는 `do...while`. 구문 밑에 있는 구문들을 실행시킵니다.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/do...while#Examples)

### [do...while](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/do...while#do...while)

예제에서 `do...while` 문은 적어도 한번 반복되고 i 변수가 5 보다 작을 때까지 실행됩니다.

```javascript
var result = '';
var i = 0;
do {
   i += 1;
   result += i + ' ';
}
while (i > 0 && i < 5);
// Despite i == 0 this will still loop as it starts off without the test

console.log(result);
```



### for 문

for (시작식 ; 조건식 ; 증감식) {

​	statements...

}

## [구문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/for#구문)

```javascript
for ([initialization]; [condition]; [final-expression])
   statement
```

- `initialization`

  식(할당식 포함) 또는 변수 선언. 주로 카운터 변수를 초기화할 때 사용합니다. `var` 또는 `let` 키워드를 사용해 새로운 변수를 선언할 수도 있습니다. `var` 키워드로 선언한 변수는 반복문에 제한되지 않습니다. 즉 `for` 문과 같은 범위scope에 위치합니다. `let` 키워드로 선언한 변수는 반복문의 지역 변수가 됩니다.  식의 결과는 버려집니다.

- `condition`

  매 반복마다 평가할 식. 평가 결과가 참이라면 `statement`를 실행합니다. 이 식을 넣지 않았을 때 계산 결과는 언제나 참이 됩니다. 계산 결과가 거짓이라면 `for` 문의 바로 다음 식으로 건너 뜁니다.

- `final-expression`

  매 반복 후 평가할 식. 다음번 `condition` 평가 이전에 발생합니다. 주로 카운터 변수를 증감하거나 바꿀 때 사용합니다.

- `statement`

  조건의 평가 결과가 참일 때 실행하는 문. 여러 문을 반복 실행하려면 [블럭문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/block)(`{ ... }`)으로 묶어야 합니다. 아무것도 실행하지 않으려면 [공백문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/empty) (`;`)을 사용하세요.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/for#예제)

### [for 사용하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/for#for_사용하기)

다음 `for` 문은 변수 `i`를 선언하고 0으로 초기화하여 시작합니다. `i`가 9보다 작은지를 확인하고 맞으면 명령문을 수행한 후 `i`의 값을 1 높입니다.

```javascript
for (var i = 0; i < 9; i++) {
   console.log(i);
   // 기타 등등
}
```

### [선택적 식 사용](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/for#선택적_식_사용)

`for` 반복문의 3개 식은 모두 선택 사항입니다.

예를 들어, 변수를 초기화하려고 `initialization` 블럭을 사용할 필요는 없습니다.

```javascript
var i = 0;
for (; i < 9; i++) {
    console.log(i);
    // 기타 등등
}
```

`initialization` 블럭처럼 `condition` 블럭도 선택 사항입니다. 다만 이 경우, 반복문 본문에 무한 반복을 탈출할 수 있는 장치를 추가해야 합니다.

```javascript
for (var i = 0;; i++) {
   console.log(i);
   if (i > 3) break;
   // 기타 등등
}
```

세 가지 모두 생략할 수도 있습니다. 위와 같이 [`break`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/break) 문을 사용해 반복을 탈출할 수 있도록 추가하고, 변수를 수정해 탈출 조건이 언젠가 참이 되도록 해야 합니다.

```javascript
var i = 0;

for (;;) {
  if (i > 3) break;
  console.log(i);
  i++;
}
```

### [문 없이 for 사용하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/for#문_없이_for_사용하기)

다음 `for` 반복 사이클은 노드의 위치 오프셋을 `final-expression`에서 계산해 문이나 블럭문이 필요하지 않으므로 세미콜론을 사용합니다.

```javascript
function showOffsetPos(sId) {
  var nLeft = 0, nTop = 0;

  for (
    var oItNode = document.getElementById(sId); /* initialization */
    oItNode; /* condition */
    nLeft += oItNode.offsetLeft, nTop += oItNode.offsetTop, oItNode = oItNode.offsetParent /* final-expression */
  ); /* semicolon */

  console.log('Offset position of \'' + sId + '\' element:\n left: ' + nLeft + 'px;\n top: ' + nTop + 'px;');
}

/* Example call: */

showOffsetPos('content');

// Output:
// "Offset position of "content" element:
// left: 0px;
// top: 153px;"
```

**참고:** 여기서 쓰인 세미콜론은, JavaScript가 **필수로 요구하는 몇 안되는 세미콜론**입니다. 물론 세미콜론 없이는 반복 사이클 선언의 바로 다음 줄을 반복 본문으로 인식합니다.



### break;

## [구문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/break#구문)

```
break [label];
```

- `label` Optional

  문의 라벨에 연결한 [식별자](https://developer.mozilla.org/ko/docs/Glossary/식별자). 반복문이나 [`switch`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch)에서 사용하는게 아니면 필수로 제공해야 합니다.

## [설명](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/break#설명)

`break` 문은 프로그램이 label 달린 문에서 빠져나오게 하는 선택사항 label을 포함합니다. `break` 문은 참조되는 label 내에 중첩되어야 합니다. label 달린 문은 어떤 [`block`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/block) 문이든 될 수 있습니다. 꼭, loop 문을 달 필요가 없습니다.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/break#예제)

다음 함수는 `i`가 3일 때 [`while`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/while) loop를 종료하는 break 문이 있고, 그러고는 3 * `x`값을 반환합니다.

```
function testBreak(x) {
  var i = 0;

  while (i < 6) {
    if (i == 3) {
      break;
    }
    i += 1;
  }

  return i * x;
}
```

다음 코드는 label 달린 블록이 있는 `break` 문을 사용합니다. `break` 문은 자신이 참조하는 label 내에 중첩되어야 합니다. `inner_block`은 `outer_block`내에 중첩되어야 함을 주의하세요.



### contiune;

## [구문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/continue#구문)

```
continue [label];
```

- `label`

  명령문의 레이블과 연관된 식별자.

## [설명](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/continue#설명)

[`break`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements / break) 문과 달리 `continue`는 루프의 실행을 완전히 종료하지 않고 `for`, `while`문에서 다음과 같이 동작합니다.

- [`while`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements / while) 루프에서는 다시 조건으로 점프합니다.

- [`for`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements / for) 루프에서는 업데이트 표현식으로 점프합니다.

`continue` 문에는 현재 루프 대신 레이블이 지정된 루프 문의 다음 반복으로 건너 뛰도록하는 선택적 레이블이 포함될 수 있습니다. 이 경우, `continue` 문은 이 레이블 된 명령문 내에 중첩되어야합니다.

## [예제](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/continue#예제)

### [Using continue with while](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/continue#Using_continue_with_while)

다음 예제에서는 `i`의 값이 3일 때 실행되는 `continue`문을 포함하는 [`while`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/while)을 보여줍니다. 따라서 n은 1, 3, 7 및 12 값을 갖습니다.

```
var i = 0;
var n = 0;

while (i < 5) {
  i++;

  if (i === 3) {
    continue;
  }

  n += i;
}
```

### [label과 함께 continue 사용하기](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/continue#label과_함께_continue_사용하기)

다음 예제에서 `checkiandj`라는 문에는 `checkj`라는 문이 있습니다. `continue`가 발생하면 프로그램은 `checkj` 문의 맨 위에서 계속됩니다. `continue`가 발생할 때마다 `checkj`는 조건이 false를 반환 할 때까지 반복합니다. false가 리턴되면 나머지 `checkiandj` 문이 완료됩니다.

`continue`에 `checkiandj` 레이블이 있으면이 프로그램은 `checkiandj` 문 맨 위에서 계속됩니다.

See also [`label`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/label).

```
var i = 0;
var j = 8;

checkiandj: while (i < 4) {
  console.log('i: ' + i);
  i += 1;

  checkj: while (j > 4) {
    console.log('j: ' + j);
    j -= 1;

    if ((j % 2) == 0)
      continue checkj;
    console.log(j + ' is odd.');
  }
  console.log('i = ' + i);
  console.log('j = ' + j);
}
```

출력:

```
i: 0

// start checkj
j: 8
7 is odd.
j: 7
j: 6
5 is odd.
j: 5
// end checkj

i = 1
j = 4

i: 1
i = 2
j = 4

i: 2
i = 3
j = 4

i: 3
i = 4
j = 4
```

