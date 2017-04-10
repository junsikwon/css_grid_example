# Grid name을 이용한 Grid 나누기
![grid4](/assets/grid4.PNG)

[보기](https://rawgit.com/sonim1/css_grid_example/master/part4/index.html)

이번 예제에서는 grid css 중 `grid-template-columns`와 `grid-template-rows`를 사용합니다.

여기에 Grid Name을 할당하여 레이아웃을 나눠보도록 하겠습니다.

## html element 설정
아래와 같이 class를 가진 element를 생성해 줍시다.
```xml
<body>
    <div class="container">
        <div class="left-navbar">Menu</div>
        <div class="content">Content</div>
        <div class="right-sidebar">Sidebar</div>
        <div class="footer">Footer</div>
    </div>
</body>
```

## Grid Name 설정
```css
.container {
    display: grid;
    height: 100vh;
    grid-template-columns:
        [left-navbar-start] 20%
        [left-navbar-end content-start] 60%
        [content-end right-sidebar-start] 20%
        [right-sidebar-end];
    grid-template-rows:
        [body-start] 80%
        [body-end footer-start] 20%
        [footer-end];
}
```

현재 **Element 순서로** Grid Name을 할당해 줍니다.
즉 첫번째 Element인 `<div class="left-navbar">`는 시작과 끝을 각각 `left-navbar-start`와 `left-navbar-end`
두번째 Element인 `<div class="content">`는 시작과 끝을 각각 `content-start`와 `content-end`로 이름을 지었습니다.

행도 마찬가지로 순서대로입니다. 때문에 `grid-template-rows`를 보시면 첫번째 줄은 `body-`로 할당해주고 두번째 줄은 `footer-`로 할당해서 사용하고 있습니다.

현재는 편의를 위해서 class명과 동일하게 만들었지만 사용자에 따라서 커스텀하게 이름을 설정 해 줄 수 있습니다.

## Grid Name을 이용한 레이아웃 변경
할당 한 Grid Name을 이용하여 Part 2에서 했던 것과 같이 변경이 가능합니다.

```css
.footer {
    grid-column: content-start / right-sidebar-end;
}

.left-navbar {
    grid-row: body-start / footer-end;
}
```

Part2에서 `grid-column`과 `grid-row`를 숫자로 넣어주던게 기억나시나요? 위와같이 name을 이용할 수도 있습니다.
