## [Javascript] Map object IE 10 이하 버전에서 사용하기(core-js)

javascript [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) object를 사용하는 라이브러리 때문에 IE 11 미만 버전을 지원하지 못하는 상황이 벌어졌다.  
IE 좀 쓰지마라!! 🤬🤬🤬  

자료를 조사하던 중 MDN See also 메뉴에 한 줄기 희망이 보였다.  
> A polyfill of Map is available in core-js  

[core-js](https://github.com/zloirock/core-js#map)는 생각보다 많은 곳에서 사용 중인 라이브러리였다(심지어 Babel도).  
core-js를 사용하니까 IE 11 미만에서도 Map object를 사용할 수 있었다.  
하지만 내년이면 없어질 IE를 위해(심지어 old 버전) 이렇게까지 투자를 해야 하는지 모르겠다.   

### 참고
- [core-js CDN 링크](https://unpkg.com/core-js-bundle@3.15.2/index.js)
- [core-js(minified) CDN 링크](https://unpkg.com/core-js-bundle@3.15.2/minified.js)