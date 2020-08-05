# Message queue
MOM(Message Oriented Middleware)을 구현한 시스템을 메시지 큐(MQ)라고 한다. 메시지 큐는 별도의 공정 작업을 연기할 수 있는 유연성을 제공하여 SOA(Service-Oriendted Architecture)방식의 개발에 도움을 줄 수 있다.  
  
프로그래밍에서 MQ는 프로세스 또는 프로그램 인스턴스가 데이터를 서로 교환할때 사용하는 방법이다. 서로 다른 프로세스나 프로그램 사이에 메시지를 교환할때 AMQP(Advanced Message Queueing Protocol)을 이용한다. AMQP는 메세지 지향 미들웨어를 위한 open standard application layer protocol 이다. AMQP를 이용하면 다른 벤더 사이에 메세지를 전송하는 것이 가능하다.  

## Why?
대용량 데이터를 처리하기 위한 배치 작업이나, 채팅 서비스, 비동기 데이터 처리, 어플리케이션/시스템간 통신 등에 사용된다. 프로세스 단위로 처리하는 웹 요청이나 일반적인 프로그램을 만들어서 사용하는데, 사용자가 많아지거나 데이터가 많아지면 요청에 대한 응답이 지연되므로 서비스가 정상적으로 작동하지 못하는 상황이 올 수 있다. 따라서 기존에 분산되어 있던 데이터 처리를 한곳으로 집중시키고. 브로커를 두어 작업을 분산 시키는 방법을 적용하기 위해 사용한다.    

## Pros & Cons
__Pros__
- 비동기(Asynchronous): Queue에 넣기 때문에 나중에 처리 할 수 있다.
- 비동조(Decoupling): 어플리케이션과 분리 할 수 있다.
- 탄력성(Resilience): 일부가 실패 시 전체에 영향을 받지 않는다.
- 과잉(Redundancy): 실패 할 경우 재실행이 가능하다.
- 보증(Guarantees): 작업이 처리된 걸 확인 할 수 있다.
- 확장성(Scalable): 다수의 프로세스들이 큐에 메시지를 보낼 수 있다.  

__Cons__
- 큐를 운영하기 위한 추가적인 자원 필요.
- 큐를 이용함에 따라 오버헤드 발생 가능성 있음.
- 시스템 목적에 맞는 MQ선정과 서버에 설치 필요.
- 선정된 MQ의 사용 방법 및 라이브러리 사용법도 익혀야 하고, 메시지 구조도 정의해야 한다.

## Kind


## Reference
- https://kji6252.github.io/2015/12/18/message-quere/
- https://shortstories.gitbooks.io/studybook/content/message_queue_c815_b9ac.html
