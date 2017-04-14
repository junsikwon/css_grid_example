# grid-column, grid-row를 이용하여 grid 나누기

![grid2](https://raw.githubusercontent.com/sonim1/css_grid_example/master/assets/grid2.PNG)

grid-column과 grid-row를 이용하여 레이아웃을 나누는 법을 알아보겠습니다.

우선 기본적인 grid css를 적용해 줍시다.

[보기](https://rawgit.com/sonim1/css_grid_example/master/part2/index.html)

```css
.container {
    display: grid;
    grid-gap: 20px;
    height: 100vh;
    grid-template-columns: 100px 200px auto auto;
}

.grid-item {
    background-color: rgb(74, 173, 228);
}
```


여기까지는 이전 예제와 별 차이가 없어 보이는군요
우선 현재 grid 설정을 봅시다

`grid-template-columns: 100px 200px auto auto;`

4개의 열로 이루어진 Grid CSS가 적용됩니다.

앞 두 열은 `고정 크기`이며 뒤에 두 열은 창 크기에 따른 `auto` 사이즈로 적용됩니다.

## grid-column, grid-row
```css
.grid-item:nth-of-type(2) {
  grid-row: span 2;
}

.grid-item:nth-of-type(6) {
  grid-column: 3 / span 2;
}
```

2번째 element는 현재 row에 span 2를
6번째 element는 현재 column에 3번째 열이 시작이고 span 2를 넣어줍니다.

6번째 element에 사용된 CSS를 보면 / 로 구분을 해주고 있는데요
grid-column을 start와 end로 나누면 아래와 같습니다.
```css
.grid-item:nth-of-type(6) {
  grid-column-start : 3;
  grid-column-end : span 2;
}
```
span을 사용하고 싶지 않다면 아래와 같이 사용할 수 있습니다.
```css
.grid-item:nth-of-type(6) {
  grid-column-start : 3;
  grid-column-end : 5;
}
```

### span?
html의 table을 다뤄보셨다면 `colspan`, `rowspan`이 익숙하실 겁니다.
아래와 같이 사용하죠
```xml
<table>
    <tr>
        <td colspan="2">2칸</td>
    </tr>
    <tr>
        <td>1칸</td>
        <td>1칸</td>
    </tr>
</table>
```

마찬가지로 CSS Grid를 span 2라고 적용하면, 2칸을 하나의 범위로 사용합니다.

# 마치며
이 포스트 내용처럼 Element를 죽 늘어놓고 특정 Element에 span을 할당하여 사용하는 방식은 개인적으로 직관성이 떨어진다는 생각이 듭니다.
어쨋든 여러가지 방식을 지원하니 이런게 있구나 하고 다음 포스트로 넘어가보도록 합시다.
