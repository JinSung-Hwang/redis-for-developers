질문리스트

### 3. 레디스 기본 개념

1. 레디스는 어떤 타입의 DB인가?
2. 가장 간단하게 저장할 수 있는 자료구조인가?
   3. String타입의 자료구조는 이미지, 숫자도 저장이 가능한가?

#### String 자료구조
- 데이터를 저장하는 명령어는?
- 데이터를 조회하는 명령어는?
- NX 옵션은 무엇인가?
- XX 옵션은 무엇인가?
- INCR 명령어는 무엇인가?
- INCRBY 명령어는 무엇인가?
- DECR 명령어는 무엇인가?
- DECRBY 명령어는 무엇인가?
- 레디스는 명령어는 원자적으로 실행된다. 그렇기에 어떤 문제가 생기지 않는가? 
- MSET 명령어는 무엇인가? 
- MGET 명령어는 무엇인가?
- MSET, MGET의 명령어는 어떤점이 장점인가?

#### List 자료구조
- 레디스에서 List는 무엇인가? 
- List에는 최대 몇개까지 저장가능한가?
- List는 데이터를 어떻게 접근 가능한가? 어떻게 활용 가능한가?
- LPUSH, RPUSH, LRANGE 명령어는 무엇인가? (그림)
- LPOP과 LTRIM은 무엇인가? (그림)
- LPOP, LTRIM을 활용하면 무엇을 만들 수 있는가?
- LINSERT와 BEFORE, AFTER명령어는 무엇인가?
- LSET, LINDEX 명령어는 무엇인가?

#### Hash 자료구조
- 레디스에서 Hash는 무엇인가?
- 필드는 무엇이고 필드가 유일해야하는가?
- 필드는 무엇을 표현하기에 적합한가? 데이터베이스 테이블도 표현하기에 적합한가?
- HSET 명령어는 무엇인가? 한번에 여러 필드-값을 저장할 수 있는가?
- HGET 명령어는 무엇인가? 어떻게 명령어를 작성해야하는가?
- HGETALL 명령어는 무엇인가? 

#### SET 자료구조
- 레디스에서 SET은 무엇인가?
- SADD 명령어는 무엇인가?
- SMEMBERS 명령어는 무엇인가?
- SREM 명령어는 무엇인가? 
- SPOP 명령어는 무엇인가?
- SUNION, SINTER, SDIFF 명령어는 무엇인가?

#### SORTED SET 자료구조
- 레디스에서 SORTED SET 은 무엇인가?
- 정렬은 어떻게 되는가? 같은 스코어의 아이템은 어떤 순으로 저장되는가?
- 인덱스로 접근이 가능한가?
- ZADD 명렁어는 무엇인가?
- 데이터가 이미 있는데 추가되면 어떤일이 발생하는가?
- ZADD 커맨드의 XX, NX, LT, GT 옵션은 무엇인가?
- ZRANGE 명령어는 무엇인가?
- ZRANGE key startIdx stopIdx [withscores] 중 withscores 명령어는 무엇인가?
- ZRANGE BYLEX 옵션은 무엇인가?

#### 비트맵
- 비트맵 자료구조는 무엇인가? 
- SETBIT, GETBIT 명령어는 무엇인가?
- BITFIELD 명령어는 무엇인가?

#### Hyperloglog 자료구조
- Hyperloglog 자료 구조는 무엇인가?
- 어떨때 사용하는 자료구조인가?
- PFADD, PFCOUNT 명령어는 무엇인가? 
- 약 1844경까지 저장 가능하다.

#### Geospatial 자료구조
- Geospatial는 무슨 자료 구조인가?
- Geospatial는 내무적으로 어떤 자료 구조로 저장되는가?
- `GEOADD <key> 위도 경도 member` 순서로 저장되는가?
- XX, NX 옵션은 무엇인가?
- GEOPOS 명령어는 무엇인가?
- GEODIST 명령어는 무엇인가?

#### STREAM 자료구조
- STREAM은 어떤 자료 구조인가?
- 언제 사용할 수 있는 자료 구조인가?

#### 레디스에서 키를 관리하는 법
키의 자동 생성과 삭제

Stream, Set, Sorted Set, Hash, List와 같은 하나의 키에 여러 아이템을 포함하는 자료구조는 
- 명시적으로 키를 생성하지 않아도 아이템을 추가하면 생성되는가? 
- 명시적으로 키를 삭제하지 않고 아이템을 모두 제거하면 자료구조가 삭제되는가?
- 키가 없는 상태에서 키 삭제, 아이템 조회, 자료 구조 크기 조회 명령어를 사용하면 에러 대신 아이템이 없는것 처럼 작동하는가?

#### 키와 관련된 커맨드

자료구조에 상관없이 모든 키에 공통적으로 사용할 수 있는 커맨드
- EXIST KEY [key ....] : </br>
- KEYS pattern : </br>
  - KEYS는 위험한 명령어인 이유는?
- SCAN cursor [MATCH pattern] [COUNT count] [TYPE type] :
- SORT key [By pattern] [Limit offset count] [GET pattern [GET pattern ...]] [ASC | DESC] [ALPHA] [STORE destination] :
- RENAME key newkey :
- RENAMENX key newkey :
- COPY source destination [DB destination-db] [REPLACE]
- TYPE key : 
- OBJECT <subcommand> [<arg> [value] [opt]] :
- FLUSHALL [ASYNC | SYNC] :