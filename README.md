# 20213072_kimlina

---

**1.top**
-실시간으로 시스템에서 현재 실행중인 프로세스에 대한  정보를 실시간으로 제공한다

![image](https://user-images.githubusercontent.com/86597790/171852433-b6554203-0caf-43fd-a3a6-58382775ccbf.png)


```
[시스템 요약 부분 항목]
첫째줄 - 현재시간, 서버가동 후 유지시간, 현재 접속 사용자, 최근 1, 5, 15분 동안 시스템 부하
둘째줄 - 프로세스의 상태(총 프로세스, 실행중, sleep, stop, 좀비프로세스)
셋째줄 - cpu 상태
넷째줄 - MEM 상태
다섯째줄 - swap메모리 상태
```


```
[프로세스 CPU 사용 사용순서 부분 항목]
PR - 우선순위 NI - Nice value(-20~19 사이의 숫자이며 값이 작을수록 우선순위가 높음)
VIRT - 작업에 사용된 가상 메모리 총사용량
RES - 프로세스가 사용하는 실제 메모리양
SHR - 프로세스가 사용하는 공유 메모리양 
S - 현재 프로세스의 상태를 나타냄 
TIME+ - 프로세스가 시작하여 사용한 CPU시간 
```





|옵션|의미|
|---|---|
|-n num|지정한 숫자num만큼 프로세스를 출력함|
|-u user|지정한 user사용자의 프로세스를 모니터링|
|-U user|지정된 사용자에 의한 프로세스만 보여줌.사용자는 실제,유효한,저장된 및 파일시스템 UID를 의미|
|-b|배치모드로 정보보를 출력한다.(3초마다 갱신)|
|-d n|화면갱신주기를 초n 단위로 설정|
|-p pid|지정한 PID 프로세스만을 모니터링|
|-s|몇 개의 대화식 명령을 비활성화한다.보안모드로 시작|
|-S|누적 시간 모드로 시작.활성화 되면 각 프로세스는 cpu를 사용한 시간과 함께 출력|
|-H|모든 개별 쓰레드가 보여짐|
|-i idle| 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않는다|


top 단축기 명령어

|명령어|설명|
|---|---|
|스페이스바|정보를 화면에 갱신|
|^L|스크린 초기화|
|F or f|필드를 추가하거나 제거한다.확인하고자 하는 항목의 알파벳을 누를 때  마다 선택/취소가 반복된다|
|d or s|화면 갱신주기를 초 단위로 설정|
|h or ?|사용 가능한 명령어를 출력한다|
|r|nice 값 변경//nice 는 우선순위를 뜻함 -20~20까지 사용가능.낮을수록 우선권이 높음.기본값은 0|
|n or #|출력할 프로세스의 수를 지정한다|
|z|Z효과 on,off|
|t| top 출력 상단의 프로세스와 cpu 항목 on/off|
|m|top 출력 상단의 메모리 항목 on/off|
|k|kill 프로세스를 종료시킨다|
|B|글자 두껍게|
|I|top 출력 상단의 load avg 항목 on/off|
|O|화면 정렬(sort) 기준 지정|
|M|적재된 메모리 사용량을 기준으로 정렬한다|
|P|CPU 사용량을 기준으로 정렬한다|
|A|age 정보를 기준으로 정렬한다|
|N|pid 정보를 기준으로 정렬한다|
|Z|화면 출력 색상변경|
|T|시간/누적시간을 기준으로 정렬한다|
|S|cumulative 모드(실시간 정보를 누적 데이터로 보여 줌)를 선택/해제한다|
|q|종료|

등등..




*-n:지정한 숫자만큼 화면 출력을 갱신*

<img src=https://user-images.githubusercontent.com/86597790/171879714-af173198-f10c-4626-bb4d-21a3b2b839b7.png width="600" height="200">

*-u:지정한 사용자의 프로세스를 모니터링*

![image](https://user-images.githubusercontent.com/86597790/171880384-4a065b1b-3bf1-4d98-aa0a-c281c175c63b.png)

*-d:화면갱신주기를 초 단위로 설정*

![image](https://user-images.githubusercontent.com/86597790/171895887-03b31e2b-6c6a-466a-a3ec-00b98cf43c01.png)


---

**ps**



-proc 디렉터리 이하에 프로세스와 연관된 가상 파일시스템의 내용을 토대로 프로세스 정보를 출력한다.

![image](https://user-images.githubusercontent.com/86597790/171989080-c8ec870c-b996-41e7-9df4-d2dd814a133b.png)

|필드명|설명|
|---|---|
|ADDR|프로세스 스택의 세그먼트 번호 (-l, l 옵션)|
|BND|커널 스레드가 바인드되는 프로세스의 논리 프로세스 번호 (-o 옵션)|
|C|프로세스 사용량 (-f, l, -l 옵션)|
|CMD|사용자가 실행한 명령 이름 (-f, -l, l 옵션)|
|COMMAND|사용자가 실행한 명령 이름 (s, u, v 옵션)|
|F|프로세스 및 스레드에 관련된 항목 (-l, l 옵션)|
|LIM|메모리에 대한 소프트 한계와 관련된 항목 (v 옵션)|
|NI|프로세스의 우선순위 값. 낮을수록 CPU 시간이 높다 (-l, l 옵션)|
|PID|프로세스 ID (기본 필드)|
|PRI|프로세스 스케줄링 우선순위. 낮을수록 우선순위가 높다 (-l, l 옵션)|
|RSS|프로세스의 실제 메모리의 크기로 KB 단위 (-l, l 옵션)|
|S|프로세스나 커널 스레드의 상태 (-l, l 옵션)|
|SIZE|가상 이미지의 크기 (v 옵션)|
|SAT|실행되고 있는 프로세스의 상태 (s, u, v 옵션)－D : 디스크 입출력 대기 상태로 인터럽트를 걸 수 없는 상태－R : 실행 중일 경우－S : 짧은 슬립 상태－T : 정지 상태－Z : 좀비 상태－W : 메모리에 상주한 페이지가 없는 프로세스
－< : 높은 우선권 프로세스
－N : 낮은 우선권 프로세스
－L : 페이지가 락이 걸린 상태|
|STIME|프로세스의 시작 시간 (-f, u 옵션)|
|SZ|프로세스가 사용하는 자료와 스택의 크기 (-l, l 옵션)|
|TIME|프로세스가 소비한 총 시간 (기본 필드)|
|TRS|텍스트의 실제 메모리 크기 (v 옵션)|
|TTY|연결되어 있는 터미널 (기본 필드)|
|UID|사용자 ID (-f, -l, l 옵션)|
|USER|사용자 이름 (u 옵션)|
|WCHAN|프로세스에 거주하는 커널 함수 (-l, l 옵션)|
|VSZ|가상 메모리에 적재된 프로세스의 KB 단위 크기|
|%CPU|마지막 1분 동안 프로세스가 사용한 CPU 점유율 (u 옵션)|
|%MEM|마지막 1분 동안 프로세스가 사용한 메모리의 점유율 (u, v 옵션)|


*기본 프로세스출력*

|옵션|의미|
|---|---|
|-a|터미널과 연관된 프로세스만 출력|
|-x|터미널과 연관되지 않는 프로세스만 출력|
|-A| 모든 프로세스 출력 (-e와 동일)|
|-e|모든 프로세스 출력|
|-a| 세션 리더와 커미널과 연관되지 않은 프로세스를 제외하고 모든 프로세스를 출력

*지정한 프로세스 출력*

|옵션|의미|
|---|---|
|-p|지정한 PID 목록의 정보만 출력|
|-C|지정한 프로세스의 실행 파일 이름의 정보만 출력|
|-u|특정 사용자의 프로세스 정보를 출력|


*프로세스 형식*
|옵션|의미|
|---|---|
|u|프로세스의 소유자 정보를 함께 출력|
|l|BSD 형식의 긴 형식으로 출력|
|e|프로세스 정보와 함께 프로세스의 환경변수 정보도 출력|
|-l|긴 포맷으로 출력|
|-o|사용자 정의 형식 지정 가능|

*프로세스 장식*
|옵션|의미|
|---|---|
|f|프로세스 계층을 텍스트 형식의 트리구조를 보여줌.|
|-f|전체 포맷으로 출력|





