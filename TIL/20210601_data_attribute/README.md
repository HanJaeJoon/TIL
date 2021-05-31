## data-* attribute

`data-*` attribute에 저장된 데이터를 가져올때  
jquery의 `data()` 는  `-` 다음에 오는 알파벳을 `-`를 제거하고 uppercase로 바꿔도 가져올 수 있다.  
하지만, `data-` attribute 뒤에 오는 대문자도 `data()`로 가져오기 위해서는 lowercase로 가져와야 한다.  
**모든 attribute가 lower처리되고 `-`가 오면 `-`를 제거하고 바로 뒤에 오는 알파벳만 uppercase한다고 생각하면 된다.**

```
"data-productId"  => "productid"  
"data-ProDUctId"  => "productid"

"data-product-id" => "productId"  
"data-PRODUCT-ID" => "productId"  
```

반면에 getAttribute는 대소문자 구별 없이 attribute를 string으로 가져올 수 있다.

```
<input id="a" type="text" data-member-idx="1" />  
<input id="b" type="text" data-memberIdx="2" />
```

```
// a
console.log($("#a").data("member-idx")); // 1  
console.log($("#a").data("memberIdx")); // 1: '-'빼고 uppercase로 변환 가능  
// b
console.log($("#b").data("member-idx")); // undefined  
console.log($("#b").data("memberIdx")); // undefined 주의!  
console.log($("#b").data("memberidx")); // 2  

// get attribute
console.log(document.querySelector("#b").getAttribute("data-memberIdx")); // "2"  
console.log(document.querySelector("#b").getAttribute("data-memberidx")); // "2"  
console.log($("#b").attr("data-memberidx")); // "2"  
console.log($("#b").attr("data-memberIdx")); // "2"  
```

---


[jsfiddle](https://jsfiddle.net/jjhan/fy02gseh/1/) 에서 직접 해볼 수 있다.  



### Reference
https://www.w3.org/TR/html51/dom.html#element-attrdef-global-data