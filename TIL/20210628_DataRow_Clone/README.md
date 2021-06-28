## [C#] DataRow Clone하기

DataTable을 사용하다 보면 DataRow를 해야 할 때가 있다.  

```
var firstRow = dataTable.Rows[0];
Table.Rows.Add(firstRow);
```

이렇게 사용하면 아래 에러가 발생한다. 

> This row already belongs to this table.

dataTable의 ImportRow() Method를 이용하면 된다.

```
var firstRow = dataTable.Rows[0];
dataTable.ImportRow(firstRow);
```

.Net fiddle에서 확인 가능하다.  
https://dotnetfiddle.net/W9h7bj