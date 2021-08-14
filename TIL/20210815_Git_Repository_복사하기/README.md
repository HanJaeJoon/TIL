# Repository 복사하기

복사할 repository를 새로운 repository로 복제(mirroring)하려면 다음과 같다.  

```
git clone --mirror <복사할 repository>  

cd <새 repository 위치>
git remote set-url --push origin <새 repository>  

git fetch -p origin
git push --mirror  
```