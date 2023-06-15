# mission-05

## 마크업 코드

---

### 초기 컨테이너 설정

```html
<section class="popular-container">
  <h2 class="popular-header"><span class="accent-color"></span></h2>
  <ol class="popular-wrap">
    <li class="popular-site sprite sprite-rank-01">
      <a href="/" class="popular-siteLink"></a>
    </li>
    <li class="popular-site sprite sprite-rank-01">
      <a href="/" class="popular-siteLink"></a>
    </li>
    <li class="popular-site sprite sprite-rank-01">
      <a href="/" class="popular-siteLink"></a>
    </li>
    <li class="popular-site sprite sprite-rank-01">
      <a href="/" class="popular-siteLink"></a>
    </li>
  </ol>
  <a href="/" class="popular-more"></a>
</section>
```

### 스프라이트 기법

순위가 등락하는 이미지를 스프라이트 기법을 통해서 표현했습니다.

```css
/* 스프라이트 설정 */
.sprite {
  background: url(./../images/rank.png) no-repeat;
}
.sprite-rank-01 {
  background-position: 180px 3px;
}
.sprite-rank-02 {
  background-position: 180px -42px;
}
.sprite-rank-03 {
  background-position: 180px -19px;
}
.sprite-rank-04 {
  background-position: 180px 3px;
}
```

### counter 함수를 이용한 링크 넘버링 
a 태그에 가상요소 ::before선택자를 설정하고 counter함수를 사용하였습니다. <br/> 그리고 inline-block 속성과 text-align 속성으로 숫자를 가운데 정렬하였습니다.

```css
.popular-site {
  counter-increment: number;
}

.popular-siteLink::before {
  content: counter(number);
  width: 16px;
  height: 16px;
  display: inline-block;
  background: var(--border-color);
  border-radius: 3px;
  color: var(--white);
  text-align: center;
  margin-right: 5px;
}
```

### 유효성 검사 완료

---

## 완성 UI

![과제UI](./과제-05.png)
