# [C#] Convert List<T> to ArrayList

이것도 알고나면 간단한데 ArrayList를 잘 사용하지 않다보니 잘 모르고 있었다.  
[Constructor](https://docs.microsoft.com/en-us/dotnet/api/system.collections.arraylist.-ctor?redirectedfrom=MSDN&view=net-5.0#System_Collections_ArrayList__ctor_System_Collections_ICollection_)를 활용하면 간단하다.

```
ArrayList arrayList = new ArrayList(list);
```