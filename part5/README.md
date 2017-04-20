# 들어가기 전
링크를 타고 오거나 중간부터 보셨다면 [시작하기](http://sonim1.tistory.com/193)를 먼저 보시길 추천해 드립니다.

# fr?
fr이란 유연한 크기를 갖는 단위입니다.
그리드 컨테이너 내의 공간 비율을 분수(fraction)로 나타냅니다.

사용자가 계산해야 할 부분을 fr을 통해서 쉽고 유연하게 사용할 수 있습니다.

```css
.grid {
    display: grid;
    grid-template-columns: auto 100px 1fr 2fr;
}
```

- 1번 열은 auto를 사용한다. 해당 Element 내부 콘텐츠에 맞게 사이즈가 조정된다.
- 2번 열은 100px을 할당한다. 100픽셀 크기만큼의 폭을 차지한다.
- 3번 열은 1fr 크기를 할당한다. 1fr이란 남은 자유 공간의 1/3(총fr)만큼의 크기를 할당한다.
- 4번 열은 2fr 크기를 할당한다. 2fr이란 남은 자유 공간의 2/3(총fr)만큼의 크기를 할당한다.

# 예제
![grid5_](https://raw.githubusercontent.com/sonim1/css_grid_example/master/assets/grid5_.PNG)

[보기](https://github.com/sonim1/css_grid_example/blob/master/assets/grid5_.PNG)

위와 같은 Layout을 만들어 보도록 하겠습니다.

HTML 파일은 아래와 같은 element를 가지고 있습니다.
```xml
<div class="container">
    <div class="box a">A</div>
    <div class="box b">B</div>
    <div class="box c">C</div>
    <div class="box d">D</div>
    <div class="box e">E</div>
</div>
```

CSS를 아래와 같이 할당하여 여러 개의 rows를 가진 layout을 만들었습니다.
```css
.container{
    display: grid;
    height: 100vh;
    grid-gap: 10px;
    grid-template-rows: 2fr 300px 30px 1fr 1fr;
}

.box {
    background-color: rgb(201, 108, 108);
}
```
fr값을 제외하면 300px과 30px이 남습니다. 그렇다면 우선 rows 사이즈 중 300px 30px을 할당 합니다.
이후 남은 자유 공간을 총 fr만큼 분할하여 Layout의 크기를 할당 합니다.



# 마치며
fr 단위 사용으로 계산해야 할 부분들이 대폭 줄어들었습니다.
가독성도 좋고 하지만 [지원하는 브라우저](http://caniuse.com/#search=grid)가 한정적이기 때문에 너무 아쉽습니다.

파트6으로 다시 돌아오겠습니다.


# 참고
[2017년에 배울 새로운 CSS기능 3가지 - nhnent](https://github.com/nhnent/fe.javascript/wiki/January-16-January-19,-2017)
[holy-grail-layout-css-grid](https://bitsofco.de/holy-grail-layout-css-grid/)
[HTML5&CSS3](http://html5tech.info/html5/pdf/HTML5&CSS3_08%EC%9E%A5_v1.0.pdf)
