![Redis](../../resources/image/redis.png)

## Redis ?

- Key, Value 구조의 비정형 데이터를 저장하고 관리하기 위한 오픈소스 기반의 비관계형 데이터베이스 관리 시스템이다.
- 데이터베이스, 캐시, 메세지 브로커로 사용되며 인메모리 데이터 구조를 가진 저장소이다.
- [db-engines.com](http://db-engines.com) 에서 key, value 저장소 중 가장 순위가 높다.

인메모리 데이터 구조
[In-Memory DB](InMemoryDB.md)


캐시서버
[Cache Server](CacheServer.md)

### Redis 의 특징

1. Key, Value 구조이기 때문에 쿼리를 사용할 필요가 없다.
2. 데이터를 디스크에 쓰는 구조가 아닌 메모리에서 데이터를 처리하기 때문에 속도가 빠르다.
3. String, Lists, Sets, Sorted Sets, Hashes 자료 구조를 지원한다.
    - String : 가장 일반적인 key-value 구조의 형태
    - Sets : String의 집합. 여러개의 값을 하나의 value 에 넣을 수 있다.
    - Sorted Sets : 중복된 데이터를 담지 않는 Set 구조에 정렬 Sort를 적용한 구조
    - Lists : Array 형식의 데이터 구조. List를 사용하면 처음과 끝에 데이터를 넣고 빼는건 빠르지만 중간에 데이터를 삽입하거나 삭제하는것은 어렵다.
4. Single Threaded로 한번에 하나의 명령만 처리할 수 있다. 중간에 처리시간이 긴 명령어가 들어오면 그 뒤 명령어들은 모두 앞에 있는 명령어가 처리될때까지 대기한다.

### Redis 사용시 주의점

1. 서버에 장애가 발생했을 경우에 대한 대비책이 필요하다.
    - 인메모리 데이터 저장소 특성상 서버에 장애가 발생했을 경우 데이터 유실이 발생할 수 있기 때문
2. 메모리 관리가 중요하다.
3. 싱글 쓰레드의 특성상 한번에 하나의 명령만 처리할 수 있다. 처리하는데 시간이 오래 걸리는 요청, 명령은 피하는 것이 좋다.