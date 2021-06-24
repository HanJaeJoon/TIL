## Element ID

DOM element의 id는 전역변수로써 사용할 수 있다.  
아무리 생각해도 글로 설명하기 어렵다. 아래 예시가 이해하기 쉬울 것이다.

HTML
```
<span id="test"></span>
```  
JS
```
test.innerText = "this is text";
```

https://jsfiddle.net/jjhan/u2bqL4dw/1/  

---
오늘 element id와 전역함수의 이름이 공교롭게도 같아서 클라이언트단에서 에러가 발생했다.  

> Uncaught ReferenceError: something is not defined

일반적으로 DOM element의 id는 prefix(btn, select 등등)를 붙이기 때문에 충돌이 발생할 경우는 없지만 이 사실을 몰랐더라면 꽤나 헤맬 수 있었던 이슈다.  
운이 좋게 이직 전에 이 사실을 알게 되어서 쉽게 찾아서 고칠 수 있었다.