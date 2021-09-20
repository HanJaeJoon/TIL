# [MS-SQL] 모든 테이블 조회

MS SQL Server에서 모든 테이블을 조회하는 쿼리는 다음과 같다.

```
SELECT c.name AS 'ColumnName'
    , t.name AS 'TableName'
FROM sys.columns c
JOIN sys.tables t ON c.object_id = t.object_id
WHERE c.name LIKE '%{something}%'
ORDER BY TableName, ColumnName;
```