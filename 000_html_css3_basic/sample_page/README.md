## HTML CSS3 Basic

### Reset CSS
브라우저마다 `default padding`값과 `default margin`값이 존재하며, 해당 값들은 각 브라우저마다 상이하다.<br>
때문에, 아래 사진처럼, 아무런 값을 지정해주지 않았는데도, 기본적으로 요소에 여백이 생기는 현상이 발생한다.<br>
```html
<head>
  <style>
    #main_header {
      width: 960px;
      height: 160px;
      position: relative;
      background-color: blue;
    }
  </style>
</head>

<body>
  <header id= "main_header">
</body>
```
<br>

![스크린샷(4)](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/8990828b-7e6f-4253-b847-15cbb01137c5)<br>
`header`요소에 여백에 관한 값은 아무것도 지정해주지 않았는데도 웹에서 결과를 확인해 보면, 위 사진과 같이 <br>
자동적으로 여백이 생긴다.<br>

이런 현상을 없애기 위해서는 기본적으로, 직접 여백과 관련된 `padding`값과 `margin`값을 0으로 초기화 해주어야 한다.<br>
그런 다음, 실질적으로 적용하고 싶은 `padding`값과 `margin`값을 원하는 값으로 초기화 해주면, 어느 브라우저에서<br>
보더라도 동일하게 보일 수 있다.<br>

이런식으로 CSS기본값을 초기화 해주는 작업을 `CSS Reset`이라고 한다.<br>
모든 요소의 기본적인 `padding`값과 `margin`값을 0으로 초기화 해주는 코드는 다음과 같다.<br>
```css
* {
    margin: 0;
    padding: 0;
}
```
<br>

해당 코드를 적용하고 나면 다음과 같은 결과를 확인 할 수 있다.<br>

![스크린샷(6)](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/3bb308ba-3392-4d37-b553-9f245f5260fc)
<br>
요소의 여백과 관련된 위 `CSS Reset` 코드를 적용하기 전에는, `header`요소의 왼쪽과 상단에 약간의 여백이 생기는<br>
현상이 발생하였는데, 모든 요소의 `padding`값과 `margin`값을 0으로 초기화 해주니, 해당 현상을 없앨 수 있었다.<br>
<br>

> 정리해보면, 브라우저마다 기본적인 `padding`값과 `margin`값이 존재하기 때문에, 요소에 여백과 관련된 값을<br>
> 지정해주지 않았는데도 불구하고, 기본적으로 원하지 않는 여백이 생기게 됨.<br><br>
> 이러한 문제를 해결하기 위해 모든 요소의 기본적인 `padding`값과 `margin`값을 0으로 초기화 해 준 다음에,<br>
> `padding`값과 `margin`값을 실질적으로 적용하고 싶은 원하는 값으로 초기화 한다.<br><br>
> 이러한 절차를 거치면, 원하지 않는 여백이 적용되는 현상도 없앨 수 있으며,  어느 브라우저에서 보더라도, <br>
> 화면에 나타나는 결과가 동일하게 나타나도록 할 수 있다.<br>

<br>

### Class와 Id의 차이 
`Id`는 한 요소에만 사용하기 위해, `Class`는 여러 요소에 중복사용하기 위해 사용하는 스타일 정의법이다.<br>
아래 그림을 보면 이해하기 더욱 쉬울 것이다.<br>
<br>

![Slide1](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/4c7e5f19-b579-4914-8d6f-83f8ae2a1c55)<br>
<br>

각 요소들을 `header`, `content`, `footer`, `side-bar`라는 id로 구분하여 고유하게 사용한다.<br>
특정 컨텐츠를 반복하는 경우, class를 이용하여, 같은 CSS를 적용시킨다.<br>
<br><br>

### `margin: 0 auto;` - 위 아래 여백없이, 좌우 여백을 균등하게 배분하여 가로 중앙에 배치하라!
`margin:_`에서 `_`는 좌우,위아래 여백을 의미하는 숫자이다. 이때, 0을 지정하였다는 것은 좌우,위아래 여백을<br>
지정하지 않는다는 뜻이다.<br>
그리고, `auto`는 가로 중앙에 좌우 여백을 자동으로 균등하게 배분하여 배치한다는 뜻이다.<br>

때문에, 이 둘을 조합한 `margin: 0 auto;`는 **위 아래 여백 없이, 좌우 여백을 균등하게 배분하여 가로 중앙에 배치하라!**<br>
라는 뜻이 된다.<br>

그럼, `margin: 100px auto;`는 무슨 의미일까?<br>
위 아래 여백은 `100px`로 지정하고, 좌우 여백을 균등하게 배분하여 가로 중앙에 배치하라! 라는 뜻이 된다.<br>

다음은 `header`요소에 `margin: 0 auto;`를 적용하여 배치한 모습이다. 
```html
<head>
  <style>
    #main_header {
      width: 960px;
      height: 160px;
      margin: 0 auto;
      position: relative;
      background-color: blue;
    }
  </style>
</head>

<body>
  <header id= "main_header">
</body>
```
<br>

![7906B9B0-61F8-4D89-81D0-9764E8742675](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/ef34619f-9063-45f6-abeb-e7d97a5861a7)<br>

추가적으로, `margin`속성을 이용한 스타일을 한줄로 설정할 수 있게 해주는 **마진 축약 표현(margin shorthand)** 을<br>
설명해 보도록 하겠다.<br>

기존에는 `margin`속성을 이용하여 스타일을 지정할 때 다음과 같은 방법을 사용하였다.<br>
```java
<style>
#example {
    border: px solid orange;
    margin-top: 25px;
    margin-right: 10px;
    margin-bottom: 30px;
    margin-left: 100px;
}
</style>
```
<br>

`margin-top : 25`, 이런식으로 하나하나 지정하여 설정해주는 방법은 오타가 날 가능성도 높아지고, 비효율적이다.<br>
그래서, 이를 해결하기 위해 사용하는 방법이 마진 축약 표현이다.<br>

이 마진 축약 표현은 `margin`속성을 이용한 스타일을 한줄에 설정할 수 있게 해준다.<br>

- ##### 4개의 `margin`속성값을 가질 경우 - `top`, `right`, `bottom`, `left` 순으로 적용
  ```html
  ex) margin: 10px, 20px, 30px, 40px;
  ```
  `margin-top: 10px;`<br>
  `margin-right: 20px;`<br>
  `margin-bottom: 30px;`<br>
  `margin-left: 40px;`<br>

- ##### 3개의 `margin` 속성값을 가질 경우 - `top`, `right` 와 `left`, `bottom` 순으로 적용
  ```html
  ex) margin : 10px, 20px, 30px;
  ```
  `margin-top: 10px;`<br>
  `margin-right: 20px;`<br>
  `margin-bottom: 30px;`<br>
  `margin-left: 20px;`<br>
  
- ##### 2개의 `margin` 속성값을 가질 경우 - `top`, `bottom`과 `right`, `left` 순으로 적용
  ```html
  ex) margin: 10px, 20px;
  ```
  `margin-top: 10px;`<br>
  `margin-right: 20px;`<br>
  `margin-bottom: 10px;`<br>
  `margin-left: 20px;`<br>
  
- ##### 1개의 `margin`속성값을 가질 경우 - 모든 마진값을 해당 값으로 같게 적용
  ```html
  ex) margin: 10px
  ```
  `margin-top: 10px;`<br>
  `margin-right: 10px;`<br>
  `margin-bottom: 10px;`<br>
  `margin-left: 10px;`<br>
  
<br><br>



### `position` - 태그 요소의 위치를 설정하는 속성
`position`속성을 다루기 전에 `offset`속성에 대해 먼저 다뤄보도록 하겠다.<br>

### `offset`속성
  `offset`속성은 기준이 되는 곳으로부터 얼마나 떨어지게 할 것인지를 정할 때 사용하는 속성이다.<br>
  `top`, `right`, `bottom`, `left` 가 있다.<br>

  이 `offset`속성의 사용을 예시로 들면 다음과 같다.<br>

  > **`top: 10px` - 기준이 되는 `top(상단)`에서 아래로 `10px`만큼 떨어져 있는 위치**<br>

<br>

### `position`속성
이 `position`속성이 가질 수 있는 속성값으로는 `static`, `relative`, `absolute`, `fixed` 이렇게 4가지 종류가 있다.<br>
  
### `static`
`position`속성을 부여하지 않았을 때, 기본적으로 가지는 디폴트 값이다. 아래 코드의 경우, 3개의 `div`요소의 `position`값은<br>
`static`이다. (`position` 속성을 부여하지 않았기 때문)<br>
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
            }
            #second {
                border: 1px solid blue;
            }
            #third {
                  border: 1px solid green;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
  </html>
  ```
  <br>
  
 ![사진1](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/5afb92a0-df14-4aea-a83b-0c0924bf98dd)<br>

  ### `relative`
  `position`속성의 속성값 중 하나인 `relative`는 **현재 위치에서 상대적인 `offset`속성을 줄 수 있다.**<br>
  위 코드 상에서 두 번째 태그 요소인 `second`에 아래로`10px (top: 10px;)`, 오른쪽으로`10px(left: 10px;)`의<br>
  `offset`을 적용해 보도록 하겠다.<br>

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
            }
            #second {
                border: 1px solid blue;
                position: relative;
                top: 10px;
                left: 10px;
            }
            #third {
                border: 1px solid green;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
  </html>
  ```
  <br>
  
  ![사진2](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/c4d47adf-bd35-4b68-998f-d6324fab38d3)<br>  
  위 코드와 같이 두 번째 태그 요소 `second`에 `relative`속성값을 적용하고, `offset`을 `top: 10px`, `left: 10px`로<br>
  적용하니, `second`가 원래(현재) 위치를 기준으로, 아래로 `10px`, 오른쪽으로 `10px`만큼 이동한 것을 알 수 있었다.<br>
  
  해당 이동은 `relative`의 성질에 따라, `relative`를 적용하기 전 현재 위치(아무런 `position` 속성값을 적용하지 않은 <br>
  디폴트로 적용되는 위치)로부터 상대적으로 아래로 `10px`, 오른쪽으로 `10px` 만큼 지정한 `offset`속성 값을 따라<br>
  이루어진 것이다.<br>
  
  당연히 첫 번째 태그 요소 `first`와 세 번째 태그 요소 `third`에는 해당 속성값(`position: relative;`)을 적용하지 않았기<br> 
  때문에, 디폴트로 적용되는 `position` 속성값, `static`이 그대로 적용되어 있다.<br>
  <br>
  
  ### `absolute`
  `position`속성의 속성값 중 하나인 `absolute`는 부모중에 `static`이 아닌 요소의 위치를 기준으로 상대적인 `offset`속성을<br>
  줄 수 있다.(`static`이 아닌 부모 요소의 위치를 기준으로 상대적인 `offset`속성 적용)<br>
  
  `relative`와 `absolute` 둘 다 `offset`속성을 적용할 수 있지만, `absolute`의 경우, `offset`속성의 기준이 되는 위치가<br>
  조건에 따라 달라질 수 있다.<br>
  
  먼저, 두 번째 태그요소 `second`의 `position`속성값을 `absolute`로 지정해주고, 아무런 `offset`속성값도 적용하지 않으면<br>
  어떤 결과가 나타나는지 보도록 하겠다.<br>
  
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
            }
            #second {
                border: 1px solid blue;
                positon: absolute;
            }
            #third {
                border: 1px solid green;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
  </html>
  ```
  <br>
  
  ![사진4](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/eb5e1e17-b285-4da5-8cb0-f6fa70e5a5b2)<br>
  이건 뭔가 ... 상상도 못한 결과가 나왔다. 태그 요소 `second`에 `absolute`속성값을 적용한 순간, 해당 요소는 다른 태그요소들과는<br>
  다른 층으로 이동한 것이라고 한다. 설명을 추가하면, 3차원 좌표계라면 `second`의 z축이 변경되었고, `second`가 다른 층으로<br>
  붕 떠버리자, 그다음 태그요소인 `third`가 z축 속성이 변경되어, 떠있는 `second`바로 아래로 그 빈자리를 채운것 이라고 한다.<br>
  이때, `second`의 x, y 위치는 변하지 않았다는 것을 명심해야 한다. (다른 층으로 이동한 것일 뿐... 현재 기존 위치는 변화x)<br>
  
  그럼, 이번엔 `offset`속성 값을 적용해 보도록 하겠다.<br>
  
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
            }
            #second {
                border: 1px solid blue;
                positon: absolute;
                top: 0px;
                left: 0px;
            }
            #third {
                border: 1px solid green;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
  </html>
  ```
  <br>
  
  ![사진3](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/f06782da-d4eb-4fc1-94d5-c1f5a1b1d803)<br>
   태그요소 `second`의 원점이 브라우저에 맞춰진 것을 확인해 볼 수 있다.<br>
   
   현재 태그요소 `second`의 부모태그는 존재하지 않는다. 이러한 경우, 브라우저의 좌 상단의 좌표가 (0, 0)이 된다.<br>
   최종적으로 정리해보면, 아래와 같은 `absolute`속성값의 성질을 이해할 수 있다. <br>
   
   - ##### 1) 부모의 `position`속성값이 모두 `static`일 경우, 브라우저의 좌 상단의 좌표가 (0, 0)이 된다.<br>
     ![사진3](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/0178ad87-dbfe-464b-b4bb-aadf891f305f)<br>
     
   - ##### 2) 부모의 `position`속성값 중에 `static`이 아닌 값이 있는 경우, 해당 부모의 좌 상단의 좌표가 (0, 0)이 된다.<br>
     ```html
     <!DOCTYPE html>
     <html lang="en">
       <head>
          <meta charset="UTF-8" />
          <meta http-equiv="X-UA-Compatible" content="IE=edge" />
          <meta name="viewport" content="width=device-width, initial-scale=1.0" />
          <title>test position</title>
          <style>
              #first {
                  border: 1px solid red;
                  position: relative;
              }
              #first > #second {
                  border: 1px solid blue;
                  position: absolute;
                  top: 0px;
                  left: 0px;
              }
              #third {
                  border: 1px solid green;
              }
          </style>
       </head>
    
       <body>
          <div id="first">first
              <div id="second">second</div>
          </div>
          <div id="third">third</div>
       </body>
     </html>
     ```
     <br>
     
     ![사진5](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/53babeda-c682-41a8-8cce-dea70f55b6ca)<br>

  쉽게 정리하자면, 태그요소의 `position`속성 값이 `absolute`인 경우, 해당 태그요소의 부모 요소가 존재하고, <br>
  이 부모요소의 속성값이 `position: static`이 아닌 경우를 제외하면, 모두 브라우저의 좌 상단이 (0, 0)이 된다.<br>
  <br>
  
  ### `fixed`
  `position`속성의 속성값 중 하나인 `fixed`는 브라우저에 대해서 위치를 잡는다. 또, 스크롤에 영향을 받지 않고,<br>
  고정된 위치를 가진다. <br>
  
  `fixed`역시, `absolute`처럼 z축 속성이 변한다. 태그요소 `first`, `second`, `third`의 `position`속성값이<br>
  `static`일 때에는 각 태그 요소들은 서로 맞물려 있지만,<br>
  이 상태에서 태그요소 `second`에 `absolute` 속성값을 부여하면, `second`의 z축 속성이 변경되어, `second`가 공중으로 띄어지고,<br>
  `second`가 공중으로 띄어지며 생긴, 빈 공간으로 태그요소 `third`가 자동으로 올라가져, 해당 빈 공간을 채우게 된다.<br>
  
  이처럼 태그요소가 자동으로 올라가지며 빈 공간을 채우는 성질을 쉽게 "브라우저 내의 중력"이라고 표현하겠다.<br>
  이 브라우저 내의 중력은 위 케이스를 보면 알 수 있듯이, 위쪽으로 작용한다.<br>
  앞서 설명하였듯이, `fixed`역시 `absolute`와 마찬가지로 적용 시, z축 속성을 변화시키는 특성을 가진 `position`<br>
  속성의 속성값이다.<br>
  
  그렇다면, `position`속성의 속성값, `fixed`와 `absolute`의 차이는 어떻게 될까?<br>
  
  `fixed`는 `absolute`와는 달리, 무조건 브라우저의 좌표를 따른다. 게다가, 스크롤도 무시하기 때문에, 화면상에서<br>
  보았을 시, 고정된 것처럼 보인다는 특성이 있다.<br>
  실제 코드를 통해서 해당 특성을 확인해 보도록 하겠다.<br>
  
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
                margin: 150px 100px;
            }
            #second {
                border: 1px solid blue;
                /* position: fixed; */
            }
            #third {
                border: 1px solid green;
                margin: 150px 100px;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
</html>
```
<br>

![스크린샷1](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/28676d1f-df31-4130-b6f6-c24287b0783c)<br>

태크요소 `second`에 `position`속성의 `fixed`속성값을 적용해주기 이전에는 위 사진과 같이, `first`와 `third`는<br>
위 아래로 150px, 좌 우로는 100px 만큼의 `margin`을 가지고 있는 형태로 간격을 유지하며 배치되어 있고,<br>

`second`는 위 아래는 자동적으로 `first`, `third`사이에 끼어있는 형태로, 각 요소들과 150px의 간격을 둔 채로<br>
배치되어 있으며, CSS초기화를 해주지 않있기 때문에 좌 우로는 브라우저의 기본적인 디폴트 값이 적용되어 약간의 <br>
여백이 생겨있는 상태이다.<br>

그렇다면, 태그요소 `second`에 `fixed`속성값을 적용하면 어떤 결과가 나타날까? 아래 결과를 보도록 하자.<br>

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
                margin: 150px 100px;
            }
            #second {
                border: 1px solid blue;
                position: fixed;
            }
            #third {
                border: 1px solid green;
                margin: 150px 100px;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
</html>
```
<br>

![스크린샷2](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/a2e52547-5998-4464-bf7c-7d388bb5ad8c)<br>

`second`에 `fixed`속성값을 적용하자, `second`의 z축 속성이 변경되어, z축 방향을 공중에 뜨게되며, 그렇게 해서 생긴<br>
빈공간을 브라우저 내의 중력에 의해 자동으로 `third`가 채우게 된다.<br>

그리고, `second`는 `fixed` 속성값이 적용되어, 스크롤에 영향받지 않고, 해당 위치에 고정된다.<br>

여기서 캐치해야할 점은 위의 내용 말고도 더 있다. 먼저, `fixed` 속성값을 적용하자, `second`요소의 `border` 테두리가<br>
내용(second)에 맞게 변경되었다. 이는 `absolute` 속성값을 적용해도 동일하게 나타나는 현상이다.<br>

그리고, 분명히, `first`와 `third`의 위, 아래 `margin`값을 150px로 설정해 주었는데, `second`가 `fixed`에 의해 <br>
공중에 뜨고, 그 빈 공간을 채우기 위해 올라온 `third`와 원래 있던 `first`의 간격이 그대로 150px이다.<br>

설정해준 대로면, `first`의 `margin-bottom: 150px`와 `third`의 `margin-top: 150px`에 의해 총 300px 만큼의 간격이<br>
나타나야 하는데, 마치 설정해둔 두 `margin`값이 겹쳐진것과 같은 현상이 발생하였다.<br>
이러한 결과는 정상적인 현상으로, **마진(margin) 겹침 현상**이라 한다. 아래 설명에서 더욱 자세히 다뤄보도록 하겠다.<br>
<br><br>

### 마진(margin) 겹침 현상과 `position`속성의 `absolute`, `fixed`
`absolute`나 `fixed`속성을 가지는 태그 요소에 마진(margin)값을 적용할 때에는 주의가 필요하다.<br>
다음 예시를 보도록 하자.<br>

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
                margin: 10px;
            }
            #second {
                border: 1px solid blue;
                margin: 10px;
            }
            #third {
                border: 1px solid green;
                margin: 10px;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
</html>
```
<br>

![스크린샷1](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/ed453640-c3ab-4e0e-99d0-e2cd6fef77e6)<br>
위 예시를 보면 알 수 있듯이, 코드 상으로는 태그요소 `first`, `second`, `third` 모두 `margin: 10px;`를 통해 상하좌우에<br>
10px만큼의 margin이 적용되어있다.<br>

하지만, 해당 코드를 실행한 결과를 보면, 각 요소들의 위 아래 간격은`margin-bottom: 10px` + `margin-top: 10px` = 20px가<br>
아닌 10px로, 서로의 `margin-bottom: 10px`와 `margin-top: 10px`가 겹쳐져 있는 듯한 형태를 띄는 것을 알 수 있다.<br>

이러한 현상을 **마진(margin) 겹침 현상** 이라고 한다.<br>

그럼, 이 상태에서 태그 요소 `second`에 `absolute(또는 fixed)`속성값을 적용한 코드와 해당 코드의 결과를 보도록 하자.<br>

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>test position</title>
        <style>
            #first {
                border: 1px solid red;
                margin: 10px;
            }
            #second {
                border: 1px solid blue;
                position: absolute;
                margin: 10px;
            }
            #third {
                border: 1px solid green;
                margin: 10px;
            }
        </style>
    </head>
    
    <body>
        <div id="first">first</div>
        <div id="second">second</div>
        <div id="third">third</div>
    </body>
</html>
```
<br>

![스크린샷2](https://github.com/Yoonsik-2002/html-css-javascript-study/assets/83572199/a02f77db-3076-437f-85ef-2c8d5cc5536f)<br>
태그요소 `second`에 `position: absolute`속성값을 적용하니, 위 사진과 같은 결과가 나타났다.<br>
계속 이해했다 시피, `absolute`속성값에 의해, 해당 속성값이 적용된 태그요소 `second`의 z축 속성이 변형되어, 공중으로 뜨고<br>
`second`가 공중으로 뜨면서 생긴 빈 공간으로 브라우저 내의 중력에 의해 태그요소 `third`가 위로 올라가 빈 공간을 채우게 된다.<br>
`absolute`속성값이 적용되지 않은 태그요소 `first`와 `third`는 정상적으로 마진 겹침 현상이 발생해, 서로 10px의 간격을 두고<br>
떨어져 있다! 여기까지는 오늘 공부한 내용을 토대로 자연스럽게 그려지는 내용이다.<br>

문제는 `absolute`속성값이 적용되어 있는 `second`요소이다. `absolute`속성값이 적용되니, 태그요소 `first`와의 간격에 있어,<br>
마진 겹침 현상이 일어나지 않았다!<br>
`first`의 `margin-bottom: 10px;`와 `second`의 `margin-top: 10px;`의 마진 겹침 현상이 일어나지 않아, 두 태그 요소의<br>
간격이 20px가 된 것이다! 이러한 현상은 `fixed`속성값에도 똑같이 적용된다.<br>

그럼 어떻게 해야 할까? 아니 왜 헷갈리게 `absolute`랑 `fixed`속성값에만 이런일이 일어나지?<br>

그래서 `positon`의 4개의 속성값들 중, `absolute`와 `fixed`에게만 공통으로 주어지는 속성이 있다. 바로 `offset`속성이다!<br>
사실은 `absolute`나 `fixed`속성값을 사용할 때, `offset`속성을 함께 사용하기 때문에 이러한 `absolute`나 `fixed` 속성값을<br>
적용한 태그요소에 마진 겹침 현상이 일어나지 않는 이슈는 크게 신경쓰지 않아도 된다.<br>
<br><br>

### `display`속성
`display`속성은 웹 페이지의 레이아웃(layout)을 결정해주는 CSS의 중요한 속성 중 하나이다.<br>
이 속성은 해당 HTML요소가 웹 브라우저에 언제 어떻게 보이는가를 결정해 준다.<br>

**대부분의 HTML요소는 이 `display`속성의 기본 값으로, 블록(`block`)/인라인(`inline`) 중 하나의 값을 가진다.**<br>

- #### 기본적인 `display`속성 값이 `block`인 HTML 요소들(`display: block;`)
  **`<div>`** **`<h1>`** **`<p>`** **`<ul>`** **`<ol>`** **`<form>`** <br> 
  
  `display`속성값이 `block`인 요소는 언제나 새로운 줄(line)에서 시작하며, 해당 라인의 모든 너비를 차지한다.<br>
  
- #### 기본적인 `display`속성 값이 `inline`인 HTML 요소들(`display: inline;`)
  **`<span>`** **`a`** **`img`**<br>
  
  `display`속성값이 `inline`인 요소는 새로운 줄(line)에서 시작하지 않으며, 요소의 너비 또한 해당 라인 전체가 아닌,<br>
  해당 HTML 요소의 내용(content)만큼만 차지한다.<br>
  
이때, 기본 `display`속성값이 `block`인 요소일지라도, 해당 요소의 `display`속성값을 `inline`으로 변경이 가능하고,<br>
그 반대인 경우인 `display`속성값이 `inline`인 요소 또한 해당 요소의 `display`속성값을 `block`으로 변경이 가능하다.<br>










  
  

