# top, ps, jobs, kill 명령어
마크다운 문법을 사용하여 `top`, `ps`, `jobs`, `kill`에 대해서 README 파일로 정리하기

## top
<img width="1280" height="159" alt="img1 daumcdn" src="https://github.com/user-attachments/assets/701dc323-6e1b-4249-95d2-eda65589f8b0" />

`top` 명령어는 실시간으로 시스템의 프로세스와 자원 사용 현황을 보여주는 명령어이다.

상단에는 순서대로 다음을 나타내는 영역들이 있다.
- System time, Uptime, User: 시스템 현재 시간, OS가 살아있는 시간, 유저 세션 수
- Load Average: CPU가 수행하는 작업 양의 평균값(순서대로 1,5,15분)
- Tasks: 현재 프로세스들의 상태
- CPU: CPU의 사용률
  - us: 프로세스 유저 영역에서의 사용률
  - sy: 프로세스 커널 영역에서의 사용률
  - ni: 프로세스의 우선순위 설정에 사용하는 사용률
  - id: 사용하지 있지 않는 비율
  - wa: IO가 완료될때까지 기다리고 있는 비율
  - hi: 하드웨어 인터럽트에 사용되는 비율
  - si: 소프트웨어 인터럽트에 사용되는 비율
  - st: CPU를 VM에서 사용하여 대기하는 비율
- Memory: 메모리 사용량(Mem: 실제 메모리 양, Swap: 디스크를 메모리처럼 사용하는 양)
  - total: 총 메모리 양
  - free: 사용 가능한 메모리 양
  - used: 사용중인 메모리 양

주요 기능은 다음과 같다.
- 각 프로세스가 CPU를 얼마나 사용하는지 표시
- 메모리 사용 현황 표시
- 실행 중인 프로세스 목록 표시
- 시스템 부하 정보 표시

주요 옵션은 다음과 같다.
| 옵션 | 기능 |
| :---: | :---: |
| P | CPU 사용률 기준 정렬 |
| M | 메모리 사용량 기준 정렬 |
| N | 프로세스 아이디 기준 정렬 |
| T | 실행 시간 기준 정렬 |
| R | 오름차순, 내림차순 변경 |

## ps
<img width="560" height="153" alt="image" src="https://github.com/user-attachments/assets/31c4e373-198c-44cd-8224-3f3dadcc1e93" />

`ps` 명령어는 `Process Status`의 약자로, 현재 시스템에서 실행 중인 프로세스 정보를 출력한다.

주요 옵션은 다음과 같다.
| 옵션 | 기능 |
| :---: | :---: |
| -e 또는 -A | 모든 프로세스 출력 |
| -f | 상세 정보 출력 |
| -u <사용자> | 특정 사용자의 프로세스만 출력 |
| -p \<PID\> | 특정 PID의 프로세스만 출력 |

`ps` 명령어는 다른 명령어와 결합되어 사용되기도 하며, 활용 예시는 다음과 같다.

`ps -ef | grep ngnix `: ngnix 관련 프로세스를 검색  
`ps -u username`: 특정 사용자의 프로세스를 확인


## jobs

## kill
