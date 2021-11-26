# WSL(Window Subsystem Linux) Root Directory

WSL 환경 내에서 `/mnt/c` 경로는 Window의 `C:` 즉, C드라이브다.  

WSL의 root directory는 다음과 같다.  

```
C:\Users\[USERNAME]\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_[CODE]\LocalState\rootfs\
```

nginx 폴더 경로를 예를 들면,  

**WSL**
```
/etc/nginx
```

**Window**
```
C:\Users\[USERNAME]\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_[CODE]\LocalState\rootfs\etc\nginx
```