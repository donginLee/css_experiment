# width : 100px 의미

width : 100px
padding : 10px
border : 5px
margin :10px 일 때

### box-sizing : content-box일 때,

width = content 자체 (padding, border 제외)
content 자체만 100px,
padding 10px,
margin 제외 전체 너비 = conent(100px)+ 2*padding(10px)+2*border(5px) = 130px
margin 포함 전체 너비 = 130px + 2\*margin(10px) = 150px

### box-sizing : border-box일 때,

width = content 자체 (padding, borde 포함)
content + padding + border 포함 100px,
padding 10px, border 5px이므로
content 너비 = width(100px) - 2*border(5px) - 2*padding(10px) = 70px
margin 제외 전체 너비 = content(70px) + 2*padding(10px) + 2*border(5px) = 100px
margin 포함 전체 너비 = 100px + 2\*margin(10px) = 120px

# 결론 도출

box-sizing은 어디 범위까지 box로 잡을 것인가? 를 정할 수 있는 속성으로, padding과 margin 은 웬만하면 줄지 않는다.

# 의문

### box-sizing : border-box로 했는데, 2*border + 2*padding > width 라면?

- 실험 조건
  width : 100px
  border : 20px
  padding : 40px

- 결과
  width : 120px
  border : 20px
  padding : 40px

- 논리 도출
  width 라고 주는 것보다 border-box라는 속성이 더 강력한 것으로 추정된다.
  실제 너비는 2*border+2*padding로 지정된다.
