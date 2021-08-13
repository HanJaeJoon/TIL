## [javascript] delay 실행 반복문

1초를 기다리면서 10번 반복하려면 아래와 같이 recursive 함수를 이용하면 된다.

```
var idx = 1;

function loop(n) {
  setTimeout(function() {
    console.log(idx);
    idx++;

    if (idx <= n) {
      loop(n);
    }
  }, 1000);
}

loop(10);
```