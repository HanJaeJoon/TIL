## [MS-SQL] 임시 테이블(#, ##)

MS SQL Server에서 임시 테이블을 만들기 위해서는 `#`과 `##`을 이용하면 된다.

- `#`을 붙이면 현재 세션에서만 사용 가능하다.
- `##`을 붙이면 다른 connection에서도 사용 가능하다(global temporary table).

SQL Server는 자동으로 임시 생성했던 테이블을 Connection이 close될 때 제거해준다.  
하지만 개인적으로 `DROP TABLE`로 꼭 지워준다.😄

```
CREATE TABLE #TEMP (
    Memo VARCHAR(MAX)
);
```

```
CREATE TABLE #GLOBAL_TEMP (
    Memo VARCHAR(MAX)
);
```