## undo commit

시간은 되돌릴 수 없지만 커밋은 되돌릴 수 있다.  
단, `revert`는 이력이 남는다.  
```
git revert <해당 revision>
```  

이력을 남기지 않고 되돌리기 위해서 `reset`을 사용한다.  
soft option은 워킹 디렉토리의 파일은 보존한다.  
```
git reset --soft HEAD~1
```
hard option은 워킹 디렉토리의 변동사항도 제거한다.  
해당 커밋 이후의 모든 변동사항이 사라진다(상남자식 reset).  
```
git reset --hard HEAD~1
```

### Reference
- https://git-scm.com/docs/git-revert
- https://git-scm.com/docs/git-reset
- https://www.git-tower.com/learn/git/faq/undo-last-commit/