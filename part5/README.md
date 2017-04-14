# fr?
fr이란 유연한 크기를 갖는 단위입니다.
그리드 컨테이너 내의 공간 비율을 분수(fraction)으로 나타냅니다.

사용자가 계산해야할 부분을 fr을 통해서 쉽고 유연하게 사용할 수 있습니다.

```css
.grid {
    display: grid;
    grid-template-columns: auto 100px 1fr 2fr;
}
```

- 1번 열은 auto를 사용한다. 해당 Element 내부 콘텐츠에 맞게 사이즈가 조정된다.
- 2번 열은 100px을 할당한다. 100픽셀 크기만큼의 폭을 차지한다.
- 3번 열은 1fr 크기를 할당한다. 1fr이란 남은 자유공간의 1/3(총fr)만큼의 크기를 할당한다.
- 4번 열은 2fr 크기를 할당한다. 2fr이란 남은 자유공간의 2/3(총fr)만큼의 크기를 할당한다.

# 예제
![grid5_](/assets/grid5_.PNG)

[보기]()

위와같은 Layout을 만들어 보도록 하겠습니다.

HTML파일은 아래와 같은 element를 가지고 있습니다.
```xml
<div class="container">
    <div class="box a">A</div>
    <div class="box b">B</div>
    <div class="box c">C</div>
    <div class="box d">D</div>
    <div class="box e">E</div>
</div>
```

CSS를 아래와 같이 할당하여 여러개의 rows를 가진 layout을 만들었습니다.
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
우선 300px 30px을 할당 합니다.
이후 남은 자유공간을 총 fr만큼 분할하여 Layout의 크기를 할당 합니다.






# 참고
[2017년에 배울 새로운 CSS기능 3가지 - nhnent](https://github.com/nhnent/fe.javascript/wiki/January-16-January-19,-2017)
[holy-grail-layout-css-grid](https://bitsofco.de/holy-grail-layout-css-grid/)
[HTML5&CSS3](http://html5tech.info/html5/pdf/HTML5&CSS3_08%EC%9E%A5_v1.0.pdf)
