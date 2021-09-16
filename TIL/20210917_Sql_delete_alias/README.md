# [MSSQL] DELETE, UPDATE 문에서 Alias 사용

간단한데 늘 헷갈리는 DELETE, UPDATE 문에서 Alias 사용하는 법  

```
DELETE a FROM TableA a JOIN TableB b ON a.ID = b.ID

UPDATE a SET a.COLUMN1 = b.COLUMN2 FROM TableA a JOIN TableB b ON a.ID = b.ID
```

처음에는 오라클과 달라서 몰랐지만, 지금은 자꾸 까먹어서 모르고...  
결국 SQL 0개국어