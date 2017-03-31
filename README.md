# CSS Grid Example

by [Kendrick B. Jung](http://sonim1.tistory.com)

# CSS Grid?
우리는 지금까지 일반적으로 그리드를 구현할 때 라이브러리를 사용하곤 했습니다. Ex) Bootstrap 등

하지만 여기 css에 공식적인 기능이 하나 있습니다.

문제는 사용하려면 Firefox 52, Chrome 57이상 버전의 브라우저를 사용하거나 크롬의 flag 기능을 이용해야 합니다.

그러니 실제 Grid 기능 사용은 기존과 같이 Bootstrap 등을 사용하시고, css에 Grid를 지원하긴 하는구만~ 하시면 더 좋을 듯 합니다.

# 시작하기
간단하게 그리드를 구현해보겠습니다.

**index.js**
```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="../reset.css">
    <link rel="stylesheet" href="./grid.css">
    <title>Document</title>
</head>
<body>
    <div class="container">
        <header>Header</header>
        <nav>Nav</nav>
        <section>Section</section>
        <aside>Aside-right</aside>
        <footer>Footer</footer>
    </div>
</body>
</html>
```
간단한 구조로 되어있습니다.

`div.container` 안에는 `header, nav, section, aside, footer` 다섯가지 레이아웃을 위한 시맨틱요소가 위치해 있습니다.

`head`에는 두가지 css파일을 가져오고 있는데 에릭마이어님의 css초기화를 위한 reset.css 파일 그리고 grid 관련 스타일 시트를 불러오고 있습니다.

reset.css에 대해서는 [이 링크](http://meyerweb.com/eric/tools/css/reset/)를 참고하시고 우리는 바로 `gird.css`를 확인해봅시다.
