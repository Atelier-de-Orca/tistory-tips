# Responsive Youtube Video
블로그를 운영하다 보면 동영상을 첨부해야 할 때가 있습니다. 

실험 결과나 결과물이 작동하는 모습 혹은, Vlog를 포스팅한다든지 말이죠. 그럴 때 자체적인 DB를 가지고 영상을 스트리밍 해줄 수도 있겠지만, 유튜브나 Vimeo같은 동영상 전문 사이트에 업로드하고 embed 하여 사용하는 것이 효율적일 것입니다.

하지만, youtube만 보더라도 embed 할 때 iframe을 사용하기 때문에 반응형 스킨을 사용하시는 분이라면 특히 모바일에서 조금 곤란하실 수도 있습니다. 간단한 css 코드만 이용해서 이런 문제를 해결해볼 수 있습니다.

```css
.youtubeWrap {
  position : relative;
  width : 100%;
  padding-bottom : 56.25%
}

.youtubeWrap iframe {
  position : absolute;
  width : 100%;
  height : 100%
}
```
이 스타일을 tistory css에 추가해주고, Youtube 영상을 embed 할 때 iframe 안에 설정되어있는 크기를 지우고 `<div class="youtubeWrap"></div>`를 이용해 묶어주면 짠! 가로길이에 맞추어 유튭 영상의 크기가 바뀌게 됩니다!
