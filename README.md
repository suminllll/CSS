css와 HTML을 섞는 방법						
1. 같은 HTML 파일에 CSS코드를 놓는 방법						
head tag 안에 syle tag를 추가						
2. CSS와 HTML을 분리시키는 방법(추천)						
따로 새파일 CSS 파일을 만든다 ex) styles.css						
link tag를 이용해 styles.css와 연결하고 rel( relationship 관계)을 이용해 관계를 적어줌						
styles.css와 이 HTML과의 관계를 말할때, styles.css는 스타일시트라 한다						
						
body에서 사용한 tag를 사용하여 그 tag를 꾸며준다 						
ex) < style > h1 { color:blue;  font: 25px; } tag지정->원하는 속성값	
![](https://images.velog.io/images/krlatnalsl/post/75ee6d56-9a08-476f-9514-64d8a31a83fb/pasted%20image%200.png)	
						
CSS를 직접 적는것을 inline CSS, CSS 파일을 include 하는것을 external CSS라고 함	
같은 selector를 가리키는 CSS가 여러개이면, 가장 마지막 스타일이 적용된다						
CSS는 위에서 아래로 차례대로 읽힌다 / 브라우저는 위에서 아래로 코드를 읽으므로 마지막에 있는 코드가 보여지게 된다						
						
block(옆에 아무것도 올 수 없음) [ div, p, header ]의 반대말은 inline(같은줄에 위치 할 수 있다 in the same line) [image,a,span등]						
display로 block or inline으로 변경할 수 있음						
inline은 높이와 너비가 없음 즉 block tag에 inline을 적용할 때 높이와 너비를 설정하면 안됨 						
반대로 block은 높이와 너비를 설정할 수 있음						
inline에 높이와 너비를 설정하고 싶으면 display: inline-block; 사용 (단점: 모니터 크기가 다르면 달라짐)						
margin = box의 border(경계)로부터 바깥에 있는 공간/ 없애려면 margin:0; , 원하는크기가 있으면 margin-left ,top,right...:50px; 등						
margin 값을 한번에 주는법 첫번째 위 오른쪽 아래 왼쪽 시계방향순, 하나만 적으면 모두가 해당 두개적으면 상하 좌우 margin: 20px 15px ;						
collasing margin 현상 (상하에서만 발생) div margin이 body margin과 만나면 둘 중 큰 값의 margin으로 body에 적용되고, 						
body와 div margin은 하나로 취급						
						
padding= box의 경계로부터 안쪽에 있는 공간						
						
같은 태그일 경우 id를 통해 각각의 스타일을 낼 수  있음						
각 id는 #{}으로 태그해줌						
한 요소는 하나의 id만을 가질 수 있다						
각기 다른 id를 같은 요소를 줄 때 #1,2,3{} 으로 콤마로 한번에 적용시킬 수 있다 또는 class사용	
![](https://images.velog.io/images/krlatnalsl/post/4ba8a0bb-8bf0-4c1c-bb94-72013a16d31b/pasted%20image%200.png)
						
class = 여러개의 속성들이 공용으로 사용할 수 있는 스타일 형식						
.(맨앞온점)속성으로 사용한다						
여러 요소를 한번에 사용할 수 있다 ex) class=" tomato hello honey"						
#tomato=id="tomato"  =		.tomato=class="tomato"		
![](https://images.velog.io/images/krlatnalsl/post/f7fe85d7-2cc9-4bc3-a719-1e3084f6ce86/pasted%20image%200.png)
![](https://images.velog.io/images/krlatnalsl/post/0778b06a-d22e-4b93-935e-848f51559c40/pasted%20image%200.png)
border= 말 그대로 box의 경계(border)이다						
border의 스타일은 border style mdn 구글링						
border: 2px(굵기) solid(스타일) black(색깔);						
전체박스에 적용= * { 2px(굵기) solid(스타일) black(색깔); } 						
전체를 사용했을때 하나는 다른 스타일로 할 경우						
ex) span{ border-style: dotted; }						
*는 전체를 뜻한다 사용법 * { }						
						
사각면을 둥글게 만들고 싶으면 border-radius: 50px;						
						
코드를 한번에 수정하려면 = (win)ctrl+D  (mac)command+D 누르고 방향키로 옮김						
						
display는 block 이다						

div 바로 밑 자식에서 span만 효과를 주는 방법 
div span{ text-decoration: underline;} 하면 div밑에있는 모든 span들이 효과를 가진다 
div> span{text-decoration: underline;} 하면 바로 밑의 자신만 적용
![](https://images.velog.io/images/krlatnalsl/post/9189d5e7-02a0-4056-b565-a3e6183b97bc/image.png)
body-div-p-span(child) 에서 p안에있는 span(child)에만 효과를 주고싶으면 
stlye에서 p span{} 을 적용시킴
![](https://images.velog.io/images/krlatnalsl/post/dd1f48d6-b1ef-4fa2-95c0-2f64f411b963/image.png)
body-div-span-p-span(부모) 에서 p다음에 오는 span에게 효과를 주고싶으면
p+span{}사용(딱 바로뒤에 오는태그만 가능). 이때 +에 마우스를 올리면 적확히 어디에있는 span인지 미리보기가 된다
![](https://images.velog.io/images/krlatnalsl/post/b5879282-8e56-418c-8530-165ca69199b1/image.png)
p~span{} 만약span이 p의 형제인데 바로뒤에 오지않을때 사용
![](https://images.velog.io/images/krlatnalsl/post/c57394e7-a366-4c68-b26e-86a0122f94f0/image.png)

< a >링크에서 밑줄을 없애고 싶으면 text-decoration:none;을 사용


body에서 작성한 input을 head-style에서 스타일을 줄때
[ ]구간선택
![](https://images.velog.io/images/krlatnalsl/post/4dd325c2-c26d-4cd3-91a8-b170e5c9a9b0/image.png)
[placeholder~="name"] placeholder에 "name"이라는 단어를 포함한 모든 input
![](https://images.velog.io/images/krlatnalsl/post/7553b2f5-1cd6-424a-960f-86e239ca9b90/image.png)
button:active{} 마우스 버튼을 누르는 순간부터 떼는 시점
hover{} 마우스 커서가 대상 위에 있을 때
focus{} 키보드로 선택되었을 때
a:visited{} 링크에만 적용됨, 방문한 링크의 색깔을 변경
focus-within{} focus 동시적용
조건/form: hover input:focus{backgrond-color:black;}일때 hover와 focus가 동시인 상태에서만 작동함/ 조건을 나열해 여러상황을 만들수 있다
button에서 배경색을 바꾸면 border의 속성이 없어짐

placeholder을 꾸미는방법은 ::placeholder
드래그 했을때 색을 입히고 싶으면 selection{color, background-color} 적용
::first-letter 첫번째 글자에만 효과

color-zilla로 어느 사이트에서나 원하는컬러를 따올수 있음
var(Vector AutoRegression/편집) 여러개의 같은 코드 색깔이 지정되어 있을때 여러개 수정하지 않고 root를 이용해 한번에 변수를 만들어 수정한다 
:root {--main-변수이름:컬러;} / 해당코드에는 var(--main-변수이름);
변수에 공간이 있으면 안됨 /변수를 사용할 때는 var(--main-변수이름);
![](https://images.velog.io/images/krlatnalsl/post/446715c2-3e2b-4c4d-8f64-d21abd43a6aa/image.png)
![](https://images.velog.io/images/krlatnalsl/post/e1f0d70e-cfba-4cb8-9f64-f12650a32f03/image.png)
https://developer.mozilla.org/ko/docs/Web/CSS/Using_CSS_custom_properties
어떤브라우저에서 작동되는지 이 사이트에서 확인하기, 변수의 기본 사용법이 담겨있음 



어떤상태에서 다른상태로 '변화'를 애니메이션 으로 만드는것

transition: 변화시키려는것 시간 ease-in-out;
transition: all; 은 모두 변화시킬수 있다

**변화시키고 싶은게 있다면 그것이 상태 안에 꼭 입력되어 있어야 한다(캡쳐예 a:hover{color}
**transition은 꼭 원래 element에 있어야 한다(캡쳐예 a{})

![](https://images.velog.io/images/krlatnalsl/post/949c8360-752c-4900-b59c-1868145e5d86/image.png)
![](https://images.velog.io/images/krlatnalsl/post/3896bc4b-c04d-4383-9851-d57ac5948330/image.png)
![](https://images.velog.io/images/krlatnalsl/post/52530919-c2ca-4049-9c6d-05980e45480e/image.png)

https://matthewlein.com/tools/ceaser
ease-in-out 사이트

"ease-in function"은 브라우저에게 애니메이션이 어떻게 변할지 말해주는 기능이다
default로 갖고 있는 것은 linear, ease-in, ease-in-out, ease-out, ease 이다.
- cubic-bezier(0, 0, 0, 0)을 이용해서 자신만의 커브를 만들 수 있다.
- transition은 state에 따라 바뀌는 property를 갖고 있으면 사용된다.
- 다른 transtion을 더 쓰고 싶다면 "콤마(,)"를 잊어선 안된다.

transition 은 상태에 따라 바귀는 요소가 있을때 사용함
상태 ex) hover, active, focus ...
ease-in function : 브라우저에게 변화하는 방법을 알려주는 역할
ㄴlinear - 변화 그래프가 직선
ㄴease-in - 시작과 끝이 빠름
ㄴease-out - 시작과 끝이 느림
ㄴease-in-out - 시작이 빠르고 끝이 느림
all : 변화 요소를 한번에 다룬다.
ㄴ따로 다루고 싶으면 각각 써주면 됨

border-radius:50%; 둥글게 된다
transformations은 다른 box element, 이미지에 영향을 끼치지 않는다
![](https://images.velog.io/images/krlatnalsl/post/faa0df40-9520-449d-8f8c-b8a440221c7a/image.png)
![](https://images.velog.io/images/krlatnalsl/post/af5bc093-b883-4b47-a7b0-c0861762addf/image.png)

transform mdn 으로 스타일 찾아보기
transition 과 transformation 을 합친다면 아름다운 애니매이션을 만들 수 있다

애니메이션을 만들고 싶으면 stlye에서 @를적기
animation: 애니메이션 이름 재생시간 옵션;
무한으로 반복되게 하려면 뒤에 infinite를 붙여줌
![](https://images.velog.io/images/krlatnalsl/post/7557d580-ec47-4a96-8a43-a7fa58adb0ac/image.png)

from to말고도 1,2,3,4,5,...10 혹은 0% 25% 50% 75% 100% 같이 여러 단계로 나눠서 애니메이션을 만들수 있다
다른 property들도 애니메이션으로 만들 수 있다. 하지만 transform을 쓰는걸 권장한다. 일부 proterty는 애니메이션이 잘 안되기 때문.
![](https://images.velog.io/images/krlatnalsl/post/f460967d-c66f-4b8d-83de-da41c8fa02d5/image.png)

https://animista.net/play/basic/shadow-pop
transform 애니메이션 디자인 사이트

@midia screen and (min-width: 650px) and (max-width: 750px){이 조건은 오직 650px과 750px사이에 있을때만 적용됨/ '이 조건이 참이면,
div {
background-color: wheat;
}} 이 css를 실행하라는 조건을 말해준다'
(orientation:portrait) 세로모드 (orientation: landscape) 가로모드
min-width는 모두 적용되지만, min-devicde-width는 핸드폰만 적용됨
media query를 사용하면 모니터가 레티나 액정인지도 알아먹을 수 있다
media query는 and로 연결된다 
media query는 조건을 추가할 수 있는 방법이다

웹 브라우저에서 inspect의 device toolbar를 이용해 핸드폰 기종별 사이즈로 미리 볼 수 있다

CSS media query MDN 구글링



