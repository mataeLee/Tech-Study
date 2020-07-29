# Stateless
서버와 클라이언트간의 세션 정보를 서버에 저장하지 않고, 세션 상태에 무관한 요청 및 응답을 만족하는 통신 방식이다. 통신의 동작 상태를 정의하지 않고, 항상 클라이언트로 부터 독립적인 요청에 의해 서비스를 제공한다.  

## Why?
- 서버에 세션 정보를 저장하지 않으므로 scale out 상황에 유리하다.
- 진행 중인 송수신 정보를 처리하기 위해 저장 공간을 동적으로 할당할 필요가 없기 때문에, 서버 디자인을 단순하게 만들 수 있다.

## Stateful과의 비교
Stateful 은 Stateless와 반대로 세션정보를 서버에 저장한다. 저장된 상태정보를 계속 추적하며 이 상태 정보를 서비스 제공에 이용하는 서버를 stateful 서버라고 한다.  
- 클라이언트가 stateless 서버로 보내는 request는 서버가 동작하기에 필요한 모든 정보를 가지고 있어야 하므로 메시지의 길이가 stateful 서버의 경우보다 길어질 수 있다.  
- stateless 서버를 사용하게되면 상태 정보를 사용할 가능성을 줄이므로써 비교적 서버가 안정적이다.  
- scale out 상황에서 두 방식의 차이를 표현한 사진이다.  
![stateful architectuer](https://github.com/mataeLee/Study-Tech/blob/master/resource/stateful.png)  
- ClientA의 요청이 server2로 진행할 경우 ClientA와의 상태정보를 다시 저장해야하는 번거로움이 생길 가능성이 있다.
![stateless architectuer](https://github.com/mataeLee/Study-Tech/blob/master/resource/stateless.png) 
- 상태정보를 따로 저장하여 이용하기 때문에 유연하게 scale-out이 가능하다.
사진 출처 ▶︎ https://5equal0.tistory.com/entry/StatefulStateless-Stateful-vs-Stateless-%EC%84%9C%EB%B9%84%EC%8A%A4%EC%99%80-HTTP-%EB%B0%8F-REST
