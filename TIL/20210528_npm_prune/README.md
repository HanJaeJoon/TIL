## npm prune

`node_modules` 폴더에서 `package.json` 과 관련없는 패키지를 제거해주는 명령어
```
npm prune
```

---

github에서 VAA Repository의 패키지 중 하나에 대한 보안 경고가 왔다.  
사용하지 않는 패키지여서 `package.json`에서 지웠는데 그래도 `node_modules` 폴더에 남아있었다.  
이 참에 사용하지 않는 패키지들을 지울 수 없을까? 하는 생각이 들어서 검색해봤다.  
가지를 친다는 prune이라는 네이밍이 찰떡이다.

### Reference
https://docs.npmjs.com/cli/v7/commands/npm-prune