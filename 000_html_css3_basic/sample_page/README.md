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
<br><br>

### `position` - 태그 요소의 위치를 설정하는 속성
`position`속성을 다루기 전에 `offset`속성에 대해 먼저 다뤄보도록 하겠다.<br>

- ### `offset`속성
  `offset`속성은 기준이 되는 곳으로부터 얼마나 떨어지게 할 것인지를 정할 때 사용하는 속성이다. <br>
  `top`, `right`, `bottom`, `left` 가 있다.<br>

  이 `offset`속성의 사용을 예시로 들면 다음과 같다.<br>

  > **`top: 10px` - 기준이 되는 `top(상단)`에서 아래로 `10px`만큼 떨어져 있는 위치**<br>

- ### `position`속성
  이 `position`속성이 가질 수 있는 속성값으로는 `static`, `relative`, 'absolute`, `fixed` 이렇게 4가지 종류가 있다.<br>
  
  #### `static`
  `position`속성을 부여하지 않았을 때, 기본적으로 가지는 디폴트 값이다. 아래 코드의 경우, 3개의 `div`요소의 `position`값은<br>
  `static`이다. (`position` 속성을 부여하지 않았기 때문)<br>
  
  



