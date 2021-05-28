## MS-SQL NULL Row를 아래로 보내기

MS SQL Server에서 Order by NULL을 마지막으로 정렬하려면 아래와 같이 사용하면 된다.
```
ORDER BY -Column DESC
```

---

최근 통계 화면을 개발하고 있다.  
ROLLUP을 사용 중인데 소계, 총계가 NULL로 표시되어 자꾸 상단에 표시됐다.  
전에 사용하던 Oracle과 달리 NULL이 가장 상단으로 와서 당황스러웠다.  
ROLLUP을 거는 Column이 INT형이라 `ISNULL(Column, Number.MAX_VALUE)` 로 하단으로 보내려고 했었는데, `Number.MAX_VALUE`도 MS SQL에는 없나보다.  
(있었어도 별로인 방법이라 사용은 안 했을 듯)

아래 방법도 MS SQL Server에서 사용할 수 없었다.  
```
ORDER BY Column DESC NULLS LAST
```

결국 아래 방법으로 간단하게 NULL을 가장 하단으로 보낼 수 있었다. 
```
ORDER BY -Column DESC
```

한국인의 감성에 집계는 아래로 와야 제맛이지~  