## HTML File Path

HTML, javascript의 경로 표현에서  
`/` 로 시작하면 루트 디렉토리에서 시작하는 경로를,  
`../` 로 시작하면 현재 페이지의 상위 경로를 나타낸다.  

```
<img src="picture.jpg"> <!-- 현재 페이지와 같은 Directory에 있는 이미지 -->  
<img src="/images/picture.jpg"> <!-- root Directory에 있는 images 폴더 안의 이미지 -->  
<img src="../picture.jpg"> <!-- 현재 Directory의 상위 Directory에 있는 이미지 -->  
```
---
이번에 프로젝트의 모든 namespace를 정리하면서 폴더 구조가 바꼈다.  
내가 예전에 이미지 파일 경로를 폴더 구조에 영향없도록 개발해놨는데 이미지가 깨졌다.  
알고보니 C#의 `Server.MapPath("~/images")`의 `~/` 와 헷갈려서 `../` 를 사용해버린 것이다.😨  
게다가 마침 해당 폴더의 상위폴더가 Root Directory여서 별다른 문제도 없었다.😥  
다시 실수하지 않도록 정리해둔다.

### Reference
- https://www.w3schools.com/html/html_filepaths.asp