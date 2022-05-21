---
layout: post
title: Gomindeul
date: 2022-05-22
categories: ["Web_Project"]
---

# 첫번째 프론트엔드 : 고민들

프로젝트 기획부터 많이 힘들었던 작업이었다.
애초에 웹개발 지식이 전무하기도 하였고 맨날 파이썬, C만 만져댔으니 
잘할 수 있을리가 없었다.

그래서 HTML, CSS부터 공부하였고
전문적이진 않지만 대충 외관은 잡을만한 지식을 쌓았다고 한껏 자만한 뒤
작업을 시작하였다.



## 힘들어할 모두에게 : 기획 의도

우선 프로젝트 결과를 먼저 공개하자면,
통계상 스팸과 중복 제외 이용자 수 450명 정도를 기록하였다.

결국 난 모두의 고민에 답변드리지 못했고 아직까지도 답변을 받지 못한채
기다리시는 분들에게 기대에 부응하지 못한 것에 대한 사과의 말씀을 드리고 싶다.

이 웹사이트는 물론 내가 프론트엔드 개발이라는 분야를 공부함으로써 흥미를 느끼고
더 성장하고자 하여 시작한 것이지만, 바쁜 현생을 살아가는 사람들이
부족한 필력을 가진 내가 써내려가는 위로의 말 한마디 한마디를 보고 들으며 
잠깐의, 아주 잠깐의 행복을 느끼게 해주고 싶었기 때문이기도 하다.

<img src="http://mbook.newstool.co.kr/daumeditor/images/2020/06/26/14/33/02_img1.jpg" width="300" height="200">

그런 의미에서 수박을 활용한 시원하게 고민을 해결해준다는 첫 컨셉에서
보라색과 노란색을 적절히 섞어 모르는 사람에게 돌아오는 답변에 대한 설레임과 신비로움, 
기다리는 동안의 행복감을 나타내는 지금의 컨셉으로 변경하였다.

<img src="/assets/gomindeul_L.png" width="300" height="80">



## 디자인

<img src="/assets/mainpage.png" width="700" height="400">

구성은 단순하다.
상단에는 바가 존재하고, 그 위에 노란색으로 제목이 위치한다.
그 밑에는 부제와 자세한 설명들을 우겨넣되, 글씨체와 색에 변화를 줘서 지루하지 않게끔 하였다.

또 최대한 쉽고 빠르게 고민을 보낼 수 있도록
가장 크게 메인에 놓았다.

여기서도 욕심이 더 생기는 바람에
잘하지도 못하는 애니메이션 재주 껏 넣어보았다.

<img src="/assets/animation.gif" width="700" height="400">

여기서 "전송하기" 버튼은 인터넷에서 따온 것인데, 이 녀석이 자꾸 말썽이었다.
엄청난 삽질 끝에 form 안에 div로 두르는 것으로 합의봤다.

```html
<form class="input_Main" action="https://formsubmit.co/xxxxxxxxxxxx" method="POST">
            
    <div class="Gomin_Text_P">
        <input class="Gomin_Text"id="message" name="message" required placeholder="고민이 뭔지 이야기해 줘!" />
    </div>
    <input type="hidden" name="_captcha" value="false">
    <input type="hidden" name="_next" value="http://www.gomindeul.com/thankyou.html">
            
    <input class="square_Email" id="email" name="email" type="email" value="" required placeholder="답변 받을 이메일을 입력해 줘!" />

    <div class="container">
        <button class="btn-1">전송하기</button>
    </div>
</form>
```

이것이 사이트의 주요 기능인 form 태그 속 친구들이다.
메일 전송을 직접 구현해보았으나 보안 취약점이 많은 관계로
관련 서비스로 대체하였다.
https://formsubmit.co/

생각보다 커스텀이 많이 가능하고 간편해서
유용하게 잘 사용하였다.

어찌되었든 이게 그 고생한 "전송하기" 버튼이다.

<img src="/assets/send.gif" >

hover로 마우스를 올리면 색깔이 바뀌는 형태로 제작하였다.



## 반응형 웹 디자인

뭐니뭐니해도 이게 제일 어려웠다.
창 크기가 변할 때, 그에 맞추어 변화하는 UI.
완전히 구현하기에는 지식이 짧아 우선 모바일 버전을 개발해보았다.



```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require("./lang/" + l);
  return true;
};
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

- This is an unordered list following a header.
- This is an unordered list following a header.
- This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
| :----------- | :---------------- | :---- |
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

---

### Here is an unordered list:

- Item foo
- Item bar
- Item baz
- Item zip

### And an ordered list:

1.  Item one
    1.  Item one
    1.  Item two
        1.  Item one
        1.  Item two
        1.  Item three
    1.  Item three
1.  Item four
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long.
```

```
The final element.
```
