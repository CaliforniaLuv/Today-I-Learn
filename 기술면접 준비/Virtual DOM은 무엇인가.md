```

  우선 Dom부터 설명하자면, 
  HTML의 head, body 같은 태그들을 js로 조작할 수 있는 객체를 의미한다.
  이 객체 모델은 브라우저에서 트리 구조 형태로 구축되어 있으며 즉, Dom은 HTML과 js를 이어주는 역할을 해준다. 
  virtiual Dom은 실제 DOM에 접근하여 조작하는 대신, 이것을 비슷하게 추상화시킨 자바스크립트 객체를 이용해 사용한다. 
  실제 돔의 가벼운 사본과 비슷한 개념이다.

  쓰는 이유: VIrtual Dom은 실제 Dom보다 가볍고, 빠른 렌더링이 가능하기 때문에 압도적으로 Dom의 부담을 덜어준다. 
           몇가지 특수 키워드는 조금씩 다르지만 실제 Dom과 virtual Dom의 구조상 큰 차이가 없어 이해하기 편한 장점이 있다.

  리액트가 가상돔을 반영하는 절차
  ex) 특정 페이지에서 데이터가 변했다고 가정했을 경우, 리액트를 이용해 돔을 업데이트 

  1. 변화가 일어났으므로 변화된 가상돔으로 바꾼다.
  2. 변화 전의 가상돔과 변화 후의 가상돔을 비교한다.
  3. 바뀐 부분만 실제 돔에 적용하여 렌더링 계산은 한 번만 이행된다. 

```
