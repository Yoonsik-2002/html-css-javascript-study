## HTML CSS3 Basic

### Reset CSS
브라우저마다 `default padding`값과 `default margin`값이 존재하며, 해당 값들은 각 브라우저마다 상이하다.<br>
때문에, 아래 사진처럼, 아무런 값을 지정해주지 않았는데도, 기본적으로 요소에 여백이 생기는 현상이 발생한다.<br>
```html
...
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
    ...
</body>
```
