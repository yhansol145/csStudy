## 자바 가상 머신(Java Virtual Machine)

### JVM의 기능
1. JAVA와 OS간 중간다리 역할을 수행하여 JAVA가 OS에 구애받지 않고 사용 가능하게 해준다.
2. 프로그램 메모리를 관리하고 최적화해준다. (Garbage Collection)

### 자바프로그램 실행과정
![자바프로그램 실행과정](../../resources/image/javaPlay.jpeg)
1. 프로그램이 실행되면 JVM은 OS로부터 이 프로그램이 필요로 하는 메모리를 할당받는다.
2. 자바 컴파일러(javac)가 자바 소스코드(.java)를 읽어 자바 바이트코드(.class)로 변환시킨다.
3. 클래스 로더 동적로딩(Dynamic Loading)을 통해 필요한 클래스들을 로딩 및 링크하여 JVM의 메모리에 올린다.
4. 실행엔진 JVM 메모리에 올라온 바이트 코드들을 명령어 단위로 하나씩 가져와서 실행한다.
5. 해석된 바이트코드는 Runtime Data Areas에 배치되어 실질적인 수행이 이루어지게 된다.