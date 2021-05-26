## Web.Config Timeout

### Web.Config의 ExecutionTimeout의 Default는 110초다.

처음 이직하고 Web.config 파일을 보고 경악을 금치 못했다.  
배포가 debug 모드로 되고 있었던 것이다.  
그래서 Web.config의 debug attribute를 false로 바꾸고 배포해야 한다고 말했고 변경이 되었다.  
하지만 그것은 앞으로 다가올 재앙의 시작이었다.

debug 모드일때 ExecutionTimeout이 적용되지 않는다.  
하지만, release 모드로 바꿔서 timeout 110초가 생겼더니  
몇년 동안이나 timeout이 없는 채 사용되었던 제품에서 110초가 넘어가는 모든 operation에서 에러가 발생하기 시작했다.  

그 다음날부터 CS는 빗발쳤고 허겁지겁 성능개선을 하거나 Timeout을 늘려주는 작업이 진행됐다.  
6개월 후에는 DB 업그레이드와 쿼리 튜닝을 하기 시작했다.  
1년 후인 요즘 문자열 like 검색에서 가끔 남는 Timeout 로그가 전부다.  

안정화된 지금은 기획팀에게 말할 수 있다. 
> 1년 전부터 발생한 Timeout 에러 저 때문에 발생한거에요😅  

### Reference  
https://docs.microsoft.com/en-us/dotnet/api/system.web.configuration.httpruntimesection.executiontimeout?view=netframework-4.8#remarks