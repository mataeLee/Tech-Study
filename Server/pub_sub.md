# Pub / Sub
메시지 기반 미들웨어 시스템의 일부라고 볼 수 있으며, 메시징 패턴의 일종으로 메시지를 브로커에게 보내고(publish) 브로커로부터 받는(subscribe) 구조이다. 중간에 브로커를 두어 토픽을 통해 subscriber가 원하는 메시지를 받을 수 있기 때문에 안정적이다.

![](https://github.com/mataeLee/Study-Tech/blob/master/resource/pub_sub_model.png)
## Why?
메시지를 발행자가 보내고 구독자가 바로 받을 경우 속도는 빠르지만 여러가지 장애 사항이 존재 할 수 있다. 예를 들어 구독자측에 장애가 있을 경우 발행자가 보낸 메시지가 유실될 가능성이 있기 때문이다. 중간에 저장소(브로커 or 채널)를 거쳐 구독자가 원할 때 메시지를 가져가는 방식을 통해 안정성과 확장성을 높일 수 있기 때문에 사용된다.

## Reference
- https://m.blog.naver.com/PostView.nhn?blogId=hisukdory&logNo=50109265674&proxyReferer=https:%2F%2Fwww.google.com%2F
- https://sugerent.tistory.com/585
  
 
