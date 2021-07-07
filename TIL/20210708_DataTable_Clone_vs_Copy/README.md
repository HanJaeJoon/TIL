## [c#] DataTable Clone vs Copy

DataTable `Clone()`으로 복사했더니 DataRow가 하나도 없었다.  
문서를 확인해보니 `Copy()`를 사용하라고 한다.  

DataTable의 구조를 복사하려면 `Clone()`을 사용하고,  
DataRow까지 복사하기 위해서는 `Copy()`를 사용하자!  

> Clone creates a new DataTable with the same structure as the original DataTable,
> but does not copy any data (the new DataTable will not contain any DataRows).
> To copy both the structure and data into a new DataTable, use Copy.

### 참고
- [DataTable Clone](https://docs.microsoft.com/en-us/dotnet/api/system.data.datatable.clone?view=net-5.0#:~:text=Clone%20creates%20a%20new%20DataTable,a%20new%20DataTable%2C%20use%20Copy.)