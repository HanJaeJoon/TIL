## [js] 빈 Object 확인하기

javascript에서 빈 object(`{}`)인지 확인하려면 아래와 같이 확인하면 된다(ES5 이상).
```
var isEmptyObject = obj && Object.keys(obj).length === 0 && obj.constructor === Object
```

**주의할 점**  
만약 빈 object가 아닌 경우를 조건으로 할때 `isEmptyObject === false` 조건을 이용해야 한다.  
`!isEmptyObject` 의 경우 obj가 null일때 문제가 된다.  
`null && true`, `null && false` 모두 null이고 `!null`은 true이기 때문이다.
```
if (isEmptyObject === false) // 이렇게 사용
if (!isEmptyObject) // 사용 x, obj가 null인 경우 문제
```