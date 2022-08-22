## REST(Representational State Transfer) 기본

### REST의 요소

#### Method
| Method | 의미 | Idempotent |
|------|------|------|
| POST | Create   | No |
| GET  | Select   | Yes |
| PUT  | Update   | Yes |
| DELETE | Delete   | Yes |
- Idempotent : 한번 혹은 여러번 수행해도 결과값 동일 여부



#### Resource
```
- http://web/user 와 같은 URI
- 모든것을 Resource(명사)로 표현하고 세부 Resource에는 id값을 지정
```

#### Message
```json
- 메세지 포맷이 존재(JSON, XML)

{
  "person" : 
  {
    "name" : "hansol",
    "age" : 30
  }   
}
```

### REST 특징
#### Uniform Interface
