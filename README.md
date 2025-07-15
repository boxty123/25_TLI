# 25_TLI
## 07-15
### HTTP
  * 무상태(Stateless): 클라이언트와 서버 사이에 상태를 유지하지 않는다.
  * Connetionlenss: 서버와 클라이언트의 Connection 연결을 지속하지 않는다.
* LoadBalancer
  * RRLB
  * LeastConnectionsLB
* Truncate vs Delete
  *  Truncate는 롤백이 불가하며 로그를 남기지 않는다. 테이블의 구조는 유지하고 모든 데이터를 삭제한다. ref) Drop은 테이블 자체를 삭제한다
  *  Delete는 특정 행 또는 모든 행을 삭제한다. 로그를 남기며 롤백이 가능하다.
### Process & Thread
  * Process는 fork()시 부모 프로세스의 메모리 공간을 복제해 Child를 만든다. Child프로세스의 Pid는 0을 배정한다. (Stack, Heap, Data, Code) 반면 Thread는 Process의 자원을 공유하며 각자 Stack과 Register공간이 존재한다.
  * PCB: 프로세스의 모든 상태를 저장하는 테이블
    * 프로세스 중지시: Registers값들이 PCB에 저장된다.
    * 프로세스 시작시: 저장된 값들이 하드웨어 Registers에 로딩된다. 
