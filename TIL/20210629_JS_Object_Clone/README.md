## [Javascript] Object Clone하기

- shallow copy: `{...obj}`, `Object.assign({}, obj)`
- deep copy: `JSON.parse(JSON.stringify(obj))`

```
let obj = { a: 1, b: 2, c: { level: 1 } };

// Spread Operator를 사용하는 방법
let newObject1 = { ...obj };  

// Object.assign을 사용하는 방법
let newObject2 = Object.assign({}, obj);

// JSON.stringify 후 JSON.parse하는 방법(조잡하다...)
let newObject3 = JSON.parse(JSON.stringify(obj));

// 모두 같다
console.log(newObject1.c.level);  // 1
console.log(newObject2.c.level);  // 1
console.log(newObject3.c.level);  // 1

// level up! 😎
obj.c.level++;

// JSON 방법을 제외하고 모두 shallow copy
console.log(newObject1.c.level);  // 2, shallow copy
console.log(newObject2.c.level);  // 2, shallow copy
console.log(newObject3.c.level);  // 1, deep copy!
```