## [MS-SQL] Column명 변경하는법

은근히 헷갈리는 Column명 변경하는법.  

매번 무의식 중에 쿼리를 짜다가  
ALTER TABLE `XXX` ALTER COLUMN `A` ...? 🤔  
늘 여기서 잘못된 부분을 느끼고 검색을 하게 된다.  

```
-- Sales 스키마 SalesTerritory 테이블의 TerritoryID Column을 TerrID로 변경
EXEC sp_rename 'Sales.SalesTerritory.TerritoryID', 'TerrID', 'COLUMN';
```

### 참고
- [Rename Columns](https://docs.microsoft.com/en-us/sql/relational-databases/tables/rename-columns-database-engine?view=sql-server-ver15)