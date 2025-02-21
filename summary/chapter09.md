질문 리스트 

#### 9. 센티널

- 센티널이란? 
- 센티널의 필요성? 
- 센티널 기능 3가지

##### 분산 시스템으로 동작하는 센티널

- SFOF 란?
- 센티널은 기본 몇대로 동작하는가? 
- 센티널은 왜 그렇게 여러대로 동작해야하는가?
- 쿼럼(quorum)이란? 
- 홀수로 센티널을 구성하는 이유? 

##### 센티널 인스턴스 배치방법

그림9-3

- 센티널 인스턴스는 어떻게 배치해야하는가?

그림 9-6

- 위와같은 구조로 센티널을 구성해도 동작하는가? 
- 이렇게 구성하면 장점은 무엇인가?

##### 센티널 인스턴스 실행하기

아래 명령어는 무슨 명령어 인가? 
- replicaof redis-ip redis-port:
- sentinel monitor master-test <master-ip> <master-port> 쿼럼수:
- sentienl master:

##### 페일오버 테스트

아래는 2가지로 페일오버를 테스트하는 방법이다. 
1. SENDTINEL FAILOVER <master-name>는 무슨 명령어인가? 어떻게 동작하는가? 
2. 마스터를 동작을 중지시켜 페일오버는 어떻게 테스트할 수 있는가? (shut down, ping)

##### 센티널 운영하기

- 센티널을 이용한 구성을 할 경우 한 그룹의 모든 노드는 같은 비밀번호를 설정해야한다. 이유는 무엇인가?
- replica-priority 파라미터는 무엇인가?
- replica-priority 값은 마스터로 선출되지 않는가?

##### 운영 중 센티널 구성 정보 변경

- SENTINEL MONITOR <master name> <ip> <port> <quorum> : 무슨 명령어인가?
- SENTINEL REMOVE <master name> : 무슨 명령어인가?
- SENTINEL SET <name> : 무슨 명령어인가?
- SENTINEL RESET <master name> : 무슨 명령어인가?

- 센티널 노드를 새로 추가하려면 모든 센티널 노드에 추가되는 센티널 ip를 추가해야하는가? 

##### 센티널의 자동 페일오버 과정

- down-after-milliseconds : 무슨 파라미터인가? 
- PING의 답은 +Pong, -Loading, -Masterdown인데 다른 응답을 받거나 응답을 아예 받지 않는 경우 무효하다고 판단하는가?
- sdown, odown은 무엇인가?
- sdown, odown 상태 전환 과정을 설명하여라
- 에포크(epoch)값이 무엇인가?

##### 스플릿 브레인 현상

그림 9-15

- 스플릿 브레인 현상이 무엇인가?
- 어떻게 이런 현상이 나타나는가?

그림 9-16

- 네트워크가 다시 복구되면 그동안 입력했던 데이터는 어떻게 되는가?
