# Stateless
클라이언트간의 세션 정보를 서버에 저장하지 않고, 세션 상태에 무관한 요청 및 응답을 만족하는 통신 방식이다.
## Why?
- 서버에 세션 정보를 저장하지 않으므로 scale out 상황에 유리하다.
- 진행 중인 송수신 정보를 처리하기 위해 저장 공간을 동적으로 할당할 필요가 없기 때문에, 서버 디자인을 단순하게 만들 수 있다.

## Stateful 과의 비교
Stateful 은 Stateless와 반대로 세션정보를 서버에 저장하고, 세션 상태에 따른 응답을 진행한다.  
- scale out 상황에서의 두 방식의 차이를 표현한 사진이다.  
![stateful architectuer](https://github.com/mataeLee/Study-Tech/blob/master/resource/stateful.png)  
![stateless architectuer](https://github.com/mataeLee/Study-Tech/blob/master/resource/stateless.png)  
사진 출처 ▶︎ https://5equal0.tistory.com/entry/StatefulStateless-Stateful-vs-Stateless-%EC%84%9C%EB%B9%84%EC%8A%A4%EC%99%80-HTTP-%EB%B0%8F-REST
