# MSA(Micro Service Architecture)
어플리케이션을 느슨히 결합된 서비스의 모임으로 구조화하는 서비스 지향 아키텍처(SOA) 스타일의 일종인 소프트웨어 개발 기법이다. 모놀리틱 구조로 된 하나의 큰 어플리케이션을 쪼개어 다수의 작은 어플리케이션(한 가지 일만 수행하는)으로 나누고, 서로에게 영향을 미치지 않고 독립적으로 역할을 수행하게 만드는 구조이다.  
<img src="https://github.com/mataeLee/Study-Tech/blob/master/resource/msa.png" width="65%" height ="55%" display='block' margin='auto'>  
## Why?
하나의 복잡한 웹 시스템을 여러개로 나누어 관리하고, 각 서비스마다 유연한 개발 및 운영이 필요한 상황일 때 적용되어야 하는 아키텍처이다. 각 팀의 역할 담당자들은 인프라에 대한 이해와 기본적인 업무 이해도가 요구된다. 

## Pros & Cons
__Pros__  
- 어플리케이션간 결합도가 낮기 때문에 확장이 쉽다. 따라서 개발자의 생산성과 속도가 증가되고 오래된 기술을 최신 기술로 쉽게 교체 가능하다.  
- 각각의 서비스가 자신과 상호작용하는 DB를 가지기 때문에, 서비스마다 DB의 종류도 다르게 가져갈 수 있어서 유연하다. 
- 작은 서비스 여러개로 나뉘어진 어플리케이션들은 단일 책임 원칙(SRP)를 따르고, 쉽게 교체할 수 있고 독립적으로 개발 및 배포를 할 수 있다.  
  
__Cons__  
- 지속적인 통합(CI)과 지속적인 배포(CD), 자동화된 테스트가 필수이다.
- 서비스간 호출 시 API를 사용하기 때문에 통신 비용이나 지연율이 그만큼 늘어난다.
- 데이터가 여러 서비스에 걸쳐 분산되기 때문에 한번에 조회하기 어렵고, 데이터의 정합성 또한 관리하기 어렵다.
  
## Reference
- https://medium.com/webeveloper/microservice-architecture%EB%9E%80-ca9825087050
- https://velog.io/@tedigom/MSA-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-1-MSA%EC%9D%98-%EA%B8%B0%EB%B3%B8-%EA%B0%9C%EB%85%90-3sk28yrv0e
