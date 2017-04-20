# fr 단위를 이용하여 grid 나누기

![grid3](https://raw.githubusercontent.com/sonim1/css_grid_example/master/assets/grid3.PNG)

이번 코드에서 중요 포인트는 fr단위입니다.

[보기](https://rawgit.com/sonim1/css_grid_example/master/part3/index.html)

아래 css를 보시죠

```css
.container {
    display: grid;
    height: 100vh;
    grid-template-columns: 1fr 4fr 1fr;
    grid-gap: 10px 100px;
    margin: 10px;
}

.grid-item {
    background-color: rgb(74, 173, 228);
}
```
`grid-template-columns`를 보시면 1fr + 4fr + 1fr => 총 6개의 fragment로 나눕니다.

데모를 보시면 바로 이해가 가실겁니다.

하지만 특이한 점이 있는데 `grid-gap`이 위에서 나눈 fragment별로 적용이 된다는 점입니다.



# 마치며
이번 포스트는 간단하네요.
단순히 사용만 하는 예제이고 fr단위에 대한 자세한 설명은 **Part 5** 에서 설명하고 있습니다.

좋은 하루 되세요.
