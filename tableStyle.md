# tistory-github-style-table
table tag generator &amp; converter for tistory

#### [2018.06.21]  
지금은 티스토리에서 기본으로 제공하는 반응형 #1 스킨을 사용하고 있습니다.  
굉장히 잘 만들어진 반응형 스킨이지만 테이블을 만들 었을 때는 정말 투박한 모양으로 출력되게 됩니다.  
티스토리 로드맵도 발표되었기 때문에 곧 개선이 되겠지만, 지금 당장은 깃허브에서 제공하는 table style을 사용하고 싶었습니다.  
  
일단, 깃허브 마크다운 스타일을 사용하기 위해 [이곳](https://github.com/sindresorhus/github-markdown-css)에 있는 `github-mrkdown.css`를 참고합니다.  
일단, Table관련 테마만 가져오고 싶기 때문에 table 키워드가 섞여있는 스타일만 복사해옵니다. 대략 아래와 같습니다.

```css
.markdown-body table {
  border-spacing: 0;
  border-collapse: collapse;
}

.markdown-body table {
  margin-top: 0;
  margin-bottom: 16px;
}

.markdown-body table {
  display: block;
  width: 100%;
  overflow: auto;
}

.markdown-body table th {
  font-weight: 600;
}

.markdown-body table th,
.markdown-body table td {
  padding: 6px 13px;
  border: 1px solid #dfe2e5;
}

.markdown-body table tr {
  background-color: #fff;
  border-top: 1px solid #c6cbd1;
}

.markdown-body table tr:nth-child(2n) {
  background-color: #f6f8fa;
}
```

일단 블로그 본문을 전부 Markdown 스타일을 사용하는 것이 아니기 때문에 살짝 변경해줍니다.
`.markdown-body table`을 원하는 클래스 이름으로 바꾸어 줍시다. 저는 `.github-table-style`로 바꾸었습니다.  

하지만, 이렇게 적용하고 table을 살펴보면 적용이 잘 안 되어있을겁니다. 티스토리에서 기본으로 사용하는 table 스타일을 제거하고 github-table-style로 대체하거나 모든 속성에 `!important`키워드를 사용하면 됩니다. 최종본은 다음과 같습니다.

```css
.github-table-style {
  border-spacing: 0 !important;
  border-collapse: collapse !important;
}

.github-table-style {
  margin-top: 0 !important;
  margin-bottom: 16px !important;
}

.github-table-style {
  display: block !important;
  width: 100% !important;
  overflow: auto !important;
}

.github-table-style th {
  font-weight: 600 !important;
}

.github-table-style th,
.github-table-style td {
  padding: 6px 13px !important;
  border: 1px solid #dfe2e5 !important;
}

.github-table-style tr {
  background-color: #fff !important;
  border-top: 1px solid #c6cbd1 !important;
}

.github-table-style tr:nth-child(2n) {
  background-color: #f6f8fa !important;
}
```
