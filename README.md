# 20213072_kimlina

---

**1.top**
-실시간으로 시스템에서 현재 실행중인 프로세스에 대한  정보를 실시간으로 제공한다

![image](https://user-images.githubusercontent.com/86597790/171852433-b6554203-0caf-43fd-a3a6-58382775ccbf.png)


```
시스템 요약 부분 항목
첫째줄 - 현재시간, 서버가동 후 유지시간, 현재 접속 사용자, 최근 1, 5, 15분 동안 시스템 부하
둘째줄 - 프로세스의 상태(총 프로세스, 실행중, sleep, stop, 좀비프로세스)
셋째줄 - cpu 상태
넷째줄 - MEM 상태
다섯째줄 - swap메모리 상태
```


```
프로세스 CPU 사용 사용순서 부분 항목
PR - 우선순위 NI - Nice value(-20~19 사이의 숫자이며 값이 작을수록 우선순위가 높음)
VIRT - 작업에 사용된 가상 메모리 총사용량
RES - 프로세스가 사용하는 실제 메모리양
SHR - 프로세스가 사용하는 공유 메모리양 
S - 현재 프로세스의 상태를 나타냄 
TIME+ - 프로세스가 시작하여 사용한 CPU시간 
```





|옵션|의미|
|---|---|
|-n|지정한 숫자만큼 화면 출력을 갱신|
|-u|지정한 사용자의 프로세스를 모니터링|
|-b|출력결과를 파일이나 다른프로그램으로 전달|
|-d|화면갱신주기를 초 단위로 설정|
|-p|지정한 PID 프로세스를 모니터링|



*-n:지정한 숫자만큼 화면 출력을 갱신*

<img src=https://user-images.githubusercontent.com/86597790/171877953-9058aad3-23ec-4f3e-bdf7-9f7abb2cb949.png width="600" height="350">

<img src=https://user-images.githubusercontent.com/86597790/171879714-af173198-f10c-4626-bb4d-21a3b2b839b7.png width="600" height="350">






---
