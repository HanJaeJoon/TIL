# NCrontab Online Tester

Azure Functions에서 Timer Trigger의 실행 시점을 표현하기 위해 
[NCrontab](https://github.com/atifaziz/NCrontab)을 이용한다.

```
{second} {minute} {hour} {day} {month} {day-of-week}
```

[MS Docs](https://docs.microsoft.com/en-us/azure/azure-functions/functions-bindings-timer?tabs=csharp#ncrontab-expressions)에서 예시를 참고하며 배울 수 있지만, 개발을 하다보면 맞는건지 의문이 든다.  
그럴때는 아래 온라인 테스터로 확인할 수 있다.  

https://ncrontab.swimburger.net/