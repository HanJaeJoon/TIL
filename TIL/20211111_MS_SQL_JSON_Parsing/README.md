## [MS-SQL] JSON Parsing하기  

DB에 저장된 JSON string을 다루는 밥법에 대한 [Documentation](https://docs.microsoft.com/en-us/sql/relational-databases/json/json-data-sql-server?view=sql-server-ver15)

```
-- JSON_VALUE를 사용하면 원하는 value를 가져올 수 있다.  
SELECT JSON_VALUE('{"columns": [{ "name": "1" },{ "name": "2" }]}', '$.columns[1].name');

-- JSON_MODIFY로 수정을 할 수 있다.  
-- append를 사용하면 원하는 value를 추가할 수도 있다!🤗  
SELECT JSON_MODIFY('{"columns": [{ "name": "1" },{ "name": "2" }]}', 'append $.columns', JSON_QUERY('{"name": "3" }'));
```

다음과 같이 결과를 확인할 수 있다.  

![](./images/1.png)

---

[PostgreSQL 14에서 json 내부 데이터 접근을 지원한다는 소식](https://www.postgresql.org/about/news/postgresql-14-released-2318/)을 들었다.  

아니 그럼 우리의 시총 1위 MS는?🤑  
이런 생각으로 검색을 했더니 역시나 있었다.  