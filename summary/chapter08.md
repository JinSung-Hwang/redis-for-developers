질문 리스트

#### 8. 복제

- 가용성이란? 
- 고가용성이란?
- 가용성 계산식은?
- 레디스에서 가용성을 확보하기 위한 2가지 방법은 무엇인가? 

- 복제란? (master-replica | slave)
- 자동 페일 오버(센티널)
-> 복제 또는 자동페일오버 중 1개만 동작해도 고가용성이 보장되는가?

##### 레디스에서의 복제 구조

- 복제 구조를 사용하는 3가지 이유?
- redis에서는 master-master구조를 지원하는가? 
- replicaof master-ip master-port 명령어란? 
- 한개의 복제 그룹에서 마스터는 1개만 있을 수 있는가?

##### 패스워드 설정

- requirepass 명령어란?
- masterauth 명령어란? 

##### 복제 메커니즘

- repl-diskless-sync: no 방식은 무슨 방식인가? 그림을 그려 설명하시오
- repl-diskless-sync: yes 방식은 무슨 방식인가? 그림을 그려 설명하시오

- repl-diskless-sync-delay 옵션은? 

##### 비동기 방식으로 동작하는 복제 연결

그림8-7

무슨 방식인가? 

##### 복제 ID

- replicationID란? 
- replicationID 무엇과 무엇으로 이루어져있는가?
- slave가 master에 연결되어 복제가 시작된다면 slave도 master와 같은 replicationID를 같는가? 
- master와 slave offset이 차이가 난다면 완전히 동기화를 못한것인가?

##### 부분재동기화

- 부분재동기화란?
- 왜있는가?
- 어떻게 이루어지는가?
- 언제 전체 재동기화를 하는가? 
- psync 명령어란? 

##### secondary 복제ID

- 한 그룹내의 모든 레디스 node는 같은 replicationId를 같는가?
- 같은 replicationId를 갖는다는건 어떤 의미인가?
- 마스터 노드가 바뀌면 replicationId가 변경되는가?

##### 읽기전용 모드로 동작하는 복제본 노드

- replication node는 에 데이터를 쓸 수 있는가?
- replica-load-only 옵션은 무엇인가?
- 마스터 전체 노드에 전체 데이터를 동기화하면 replica에 쓴 데이터는 유실될 수 있는가?
- 슬레이브에 넣은 데이터는 다른 슬레이브에 전달되는가? 

##### 유효하지 않는 복제본 데이터

- 유효하지 않는 복제본 데이터는 무엇인가?

##### 백업을 사용하지 않는 경우에서의 데이터 복제

- redis replica 구조를 사용하면 master와 slave모두 백업 기능을 사용하는것이 좋은가?
- 만약 이 옵션은 사용하지 않는다면 레디스가 자동으로 재시작하지 않도록 하는것이 좋은가? 왜그런가?
