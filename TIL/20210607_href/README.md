## href의 #과 javascript:void(0)의 차이

`href="#"` 는 클릭 시 해당 페이지의 가장 상단으로 이동하게 된다.  
`href="javascript:void(0);` 는 아무일도 벌어지지 않는다.

아래 codepen에서 확인해보자  
https://codepen.io/jaejoon/pen/VwpxNoW  
아래에 있는 #을 누르면 가장 위로 이동하는 것을 알 수 있다.
반면 javascript:void(0);은 아무일도 일어나지 않는다.

### Reference
- https://codesource.io/vs-javascriptvoid0-which-one-is-the-best-attribute-for-empty-links/