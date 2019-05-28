# LaTex로 수식 입력하기

tistory는 자체적으로 지원하는 수식 편집기가 없습니다. 아무래도 공학 관련 내용을 주로 올리다 보니 수학과 관련된 내용이 올라갈 수도 있고, 굳이 수학이 아니더라도 시간복잡도를 표현한다거나 간단한 공식을 예를 들어 설명할 수 있으므로 수식 입력기가 필요한 상황이었습니다.

## 옛날에 사용한 방식 : 수식입력기 to image file
#### 장점
- 어디서나 수식을 보여줄 수 있음
- 수식 입력기는 숏컷이나 아이콘이 잘되어있어 입력이 수월
#### 단점
- 이미지이기 때문에 수정이 귀찮아짐
- 용량 문제

## LaTex 스크립트
tistory는 네이버 블로그같이 조금 폐쇄적인 블로그 호스팅 서비스와 비교하면 스크립트 삽입이 비교적 자유로워서 LaTex관련 스크립트도 삽입할 수 있었습니다. [MathJax.js](https://www.mathjax.org/)를 이용했는데 스크립트를 cdn으로 제공해서 비교적 쉽게 스크립트 삽입이 가능합니다.

```html
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js">
  MathJax.Hub.Config({
    extensions: ["tex2jax.js","TeX/AMSmath.js","TeX/AMSsymbols.js"],
    jax: ["input/TeX", "output/HTML-CSS"],
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
    },
    "HTML-CSS": { availableFonts: ["TeX"] }
  });
</script> 
```
이 스크립트를 불러오고 나면 $ 기호 사이에 LaTex를 사용할 수 있게 된다.  
예를 들어 `$a_0{t^2} + a_1{t} + c = 0$`와 같이 ${내용}$에 Latex 문법에 맞추어 식을 작성하면 된다.

## LaTex 스크립트의 문제점
$표시를 기호로 사용하니 당연하게 그냥 $를 쓸 수가 없다. 방법이 있다면 $$$를 써서 수식 스타일로 사용하거나, <span> 태그로 묶어서 사용하면 사용할 수 있다.

## 참고 사이트
- MathJax : [www.mathjax.org](https://www.mathjax.org/)
- Latex 문법 : [위키백과](https://ko.wikipedia.org/wiki/%EC%9C%84%ED%82%A4%EB%B0%B1%EA%B3%BC:TeX_%EB%AC%B8%EB%B2%95)
- Atelier d`Orca : [적용된 포스팅](http://orcacode.tistory.com/entry/%EC%88%98%ED%95%99%EC%9C%BC%EB%A1%9C-%EA%B3%A1%EC%84%A0%EC%9D%84-%EA%B7%B8%EB%A0%A4%EB%B3%B4%EA%B8%B0-part1)
