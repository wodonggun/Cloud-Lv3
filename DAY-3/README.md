# 3일차

Repository 패턴 - 


## JPA
이번 글에서는 JPA(Java Persistence API)가 무엇인지 알아보려고한다. JPA는 자바 진영에서 ORM(Object-Relational Mapping) 기술 표준으로 사용되는 인터페이스의 모음이다. 그 말은 즉, 실제적으로 구현된것이 아니라 구현된 클래스와 매핑을 해주기 위해 사용되는 프레임워크이다. JPA를 구현한 대표적인 오픈소스로는 Hibernate가 있다.

ORM(Object-Relational Mapping)
우리가 일반 적으로 알고 있는 애플리케이션 Class와 RDB(Relational DataBase)의 테이블을 매핑(연결)한다는 뜻이며, 기술적으로는 어플리케이션의 객체를 RDB 테이블에 자동으로 영속화 해주는 것이라고 보면된다.

JPA(Java Persistence API)
Java 진영에서 ORM(Object-Relational Mapping) 기술 표준으로 사용하는 인터페이스 모음
자바 어플리케이션에서 관계형 데이터베이스를 사용하는 방식을 정의한 인터페이스
인터페이스 이기 때문에 Hibernate, OpenJPA 등이 JPA를 구현함

![image](https://user-images.githubusercontent.com/35188271/161879222-e57ad1fe-f3ea-4677-8c7e-7183430c7a0c.png)

![image](https://user-images.githubusercontent.com/35188271/161879246-64702e5f-ba17-4911-b888-1d7bfeb1b7b5.png)



## 실습

- mvn install



### SAGA 패턴

Saga Pattern 2PC를 사용할 수 없는 분산 환경에서 데이터 일관성을 위한 방안이다.

예전에 분산 트랜잭션은 2PC(Two-Phase Commit)을 많이 사용했다. 이는 Prepare-Commit의 두 단계로 이루어져 있습니다. 그리고 2PC는 DB가 분산 트랜잭션을 지원해야 한다. 그리고 같은 DB여야 한다.

하지만 MSA 환경에서는 서로 다른 앱이 API를 통해 트랜잭션을 처리하기 때문에 2PC와 같은 방식은 사용할 수 없다. NoSQL은 분산 트랜잭션을 지원하는 경우가 거의 없다.

그래서 Saga Pattern은 트랜잭션의 관리 주체가 DBMS가 아닌 앱이다. 앱(=마이크로서비스)끼리 이벤트를 주고 받는다. 그리고 각 앱은 자기에게 붙어있는 로컬 DB의 트랜잭션만 신경쓴다. 따라서 각 DB는 다른 제품을 써도 된다.

단 2PC와 다르게 데이터의 원자성이 보장되거나 동기식으로 처리되지 않는다. 그래서 Eventually Consistency만 보장한다. 또한 보상 트랜잭션 처리도 해줘야 합니다.





# 4일차

![image](https://user-images.githubusercontent.com/35188271/162097519-63ca67a3-c29b-452b-ad51-f49157121eee.png)  
  트랜잭션 완료후 커밋하도록 구현되어있음.


