## 참고 자료
`JPA 설명` : https://velog.io/@swchoi0329/Spring-Boot%EC%97%90%EC%84%9C-JPA-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0

## 



## Link vs useNavigate 차이
```
1. Link
클릭 시 바로 이동하는 로직 구현 시에 사용
ex) 상품 리스트에서 상세 페이지 이동 시

2. useNavigate
페이지 전환 시 추가로 처리해야 하는 로직이 있을 경우 useNavigate 사용
ex) 로그인 버튼 클릭 시
회원가입 되어 있는 사용자 -> Main 페이지로 이동
회원가입이 되어 있지 않은 사용자 -> SignUp 페이지로 이동
```



## yarn

- `package.json과 yarn.lock 관계` : https://www.daleseo.com/js-package-locks/

- `package lock파일은 개발자간 모듈 버전을 맞추기 위해서 사용함` :

- `yarn`은 npm에 비해 install 속도가 더 빠르고, yarn.lock`은 버전에 종속성으로 다른사람이 yarn install시에 yarn.lock에 포함된 버전을 그대로 수용하고 고정으로 사용하게됨. 이렇게 해서 팀의 버그를 방지하면서 팀 모두가 똑같은 패키지를 갖도록 보장함.

결국 팀원들은 package.json과 yarn.lock을 둘다 사용하지만 package.json은 각 팀원들마다 계속 최신화가 될 수 있지만, yarn.lock에 있는 버전들은 고정되어서 package.json의 영향을 받지 않음 = yarn.lock은 수정하거나 삭제하는건 모두의 버전 동의가 필요함.


## CI-CD 

![image](https://user-images.githubusercontent.com/35188271/176850388-2c3a4de6-87f8-4ab1-b660-baac4307ae84.png)

- CI/CD : 하나의 단어로 `사용자에게 빈번이 배포할 수 있는 환경을 말함`

- CI : 주기적으로 메인레포지토리에 빌드/배포되는것을 말함. 
 1. 코드 변경사항을 주기적으로 빈번하게 머지해야 함.
 2. 통합을 위한 단계의 자동화 (빌드, 테스트, 메인branch 머지)
 3. 지속적으로 통합을 통해 


- CD : 배포 준비 -> 개발팀/검증팀의 검증 -> 배포
 1. Continuous Delivery : CI이후에 개발팀과 검증팀 검증 + 배포가 수동으로 이루어지는 환경.
 2. Continuous Deployment : 최종 배포까지 자동화.

- `CI(Continuous Integration)=지속적 통합` : 개발자들을 위한 자동화 프로세스를 의미하며, CI환경이 성공적으로 구성되면 코드 변경 사항이 정기적으로 빌드 및 테스트되어 자동으로 공유 레포지토리에 통합되면서 (주기적으로 하면) 코드 작업에 대한 충돌 문제가 해결됨.  
![image](https://user-images.githubusercontent.com/35188271/176574781-4dbb038e-fa63-45f9-aa30-f965a8739927.png)

- `CD(Continuous Delivery)= 지속적인 제공` : 개발자들이 어플리케이션에 적용한 변경 사항이 버그 테스트를 거쳐 레포지토리에 자동으로 업로드 되는것을 뜻함.
- `CD(Continuous Deployment)=지속적인 배포` : 레포지토리의 소스를, 운영 환경까지 자동으로 배포하는것을 말함. 파이프라인의 다음 단계를 자동으로 해결.
CI에서 빌드/테스트 완료 후에 배포단계에서 `release할 준비 단계를 거치고, 수정할만한게 없는지 검증팀이 검증함`. 즉, QA환경에서 검증하고 운영에 배포하는것까지 자동으로 진행.  
![image](https://user-images.githubusercontent.com/35188271/176652903-71b34eb3-f12b-4a95-a34f-6b4e6edcf384.png)


## github action (CI/CD)

https://www.youtube.com/watch?v=iLqGzEkusIw


## GoF 디자인 패턴
![image](https://user-images.githubusercontent.com/35188271/176984284-8cc3aeea-1b7d-4de4-a736-9da563b384bf.png)
![image](https://user-images.githubusercontent.com/35188271/176984290-5fa38589-4093-46b7-86b8-9694a91976cd.png)
![image](https://user-images.githubusercontent.com/35188271/176984296-b6d133d6-d832-4d1e-82e9-3e7f4008c06b.png)


## 기술부채
![image](https://user-images.githubusercontent.com/35188271/176984405-b04c2c6e-5c38-4ee0-88af-e6a195f61048.png)  
  
    
![image](https://user-images.githubusercontent.com/35188271/176984440-7df8055d-8eb9-4af2-bd2b-1e0c3daeda25.png)  
  
  
![image](https://user-images.githubusercontent.com/35188271/176984464-6104b8e4-3913-4446-93b5-7852cde72fd9.png)  
  
  





## 클라우드 공부
```
각각 시스템은 자동화 되어있지만 현장 업무의 연속성 측면에서는 메뉴얼 업무가 다수임.
클라우드는 아니지만 클라우드 환경으로 넘어가려고 할때 바로 넘어갈 수 있는 환경으로 만들자.
그래서 MSA를 통해 개발함.

담당자가 클라우드는 안된다. 아직 리스크가 있다. 하지만 나중에 클라우드로 넘어가려고 할때 바로 넘어갈 수 있는 환경으로 개발하자.
그래서 MSA방식을 채택함.


```

```
12 Factors
1.코드베이스 : 버전 관리되는 하나의 코드베이스와 다양한 배포 = bitbucket
2.종속성 : 명시적으로 선언되고 분리된 종속성 = Maven (Pom.xml)
3.설정 : 환경에 저장된 설정(DB정보,인증,서버IP) = Application.yml, application-local.yml, application-dev.yml, qa,prod
4.백엔드 서비스 : 백엔드 서비스를 연결된 리소스로 취급 = 외부 Rest API, DB MQ 약결합
5.빌드, 릴리즈, 실행 : 철저하게 분리된 빌드와 실행 단계 = 빌드 후 동일 버전 반복 사용, 유니크가 릴리즈ID 부여, 이전 버전으로 롤백 지원 
6. 프로세스 : 애플리케이션 또는 여러개의 무상태(Stateless) 프로세스로 실행 = 일반서비스는 stateless, 일반 서비스는 실시간 동기화
7. 포트바인딩 : 포트 바인딩을 사용해서 서비스를 공개함 = A서비스가 B서비스를 HTTP로 호출
8. 동시성(Concurrency) : 프로세스 모델을 사용한 확장 = 프로세스별 최소/최대 개수 조정, 필요 시 추가로 기동 가능.
9. 폐기가능(Disposability) : 빠른1시작과 그레이스풀 셧다안정성 극대화 = Spring boot의 gracefulshutdown 적용
10.개발/프로덕션환경 일치 : 개발, 스테이징, 프로덕션 환경을 최대한 비슷하게 유지 = App. server, DBserver 등 동일/유사한 구조로 시스템 자원을 할당.
11. 로그 : 로그를 이벤트 스트림으로 취급. application은 output Stream에 관여 x = LogBack을 이용하여 server에1남긴1후, fileBeat로 전송.
12.Admin 프로세스 : admin/maintaenance 작업을 일회성 프로세스로 실행
```

- API GateWay : Netflix oss Zuul 
- Service Discovery : netlifx oss Eureka
- Load Balancing : netflix oss Ribbon
- Circuit Breaker : netflix oss Hystrix
- Service Orchestration : In-House
- Distributed Tracing : Zipkin, Spring Cloud Sleuth(또는 Jaeger)
- 모니터링 : Prometheus, Grafana 
- 로그 : Filebeat, Logstash, Elasticsearch, kibana
- CI/CD :젠킨스
- Provision Tool : Ansible
- ETL : innoQuartz
- Source Code Repository : 비트버킷
- 협업 도구 : 지라 컨플루언스
- FE : React, Vue 
- BE : Spring 

```
배포 자동화를 위해서 젠킨스
Vue.js는 이쁜 컴포넌트가 많아서 추가함.
오케스트레이션은 사용률에따라서 instance를 알아서 조절함.
프로매태우스는 모니터링 도구이고, 시각화를 위해 그라파나를 사용
유레카는 MSA서버가 배포되고 추가된게 어디 포트에 있는지 관리/추적함.(IP/port 등록하여 서비스 목록을 관리) 
RIBBON은 로드밸런싱
히스트릭스 : 서비스간 장애 발생시 장애가 전파되지 않도록 서킷브레이커 역할
```

고가용성을 위해서 2개씩 서버를 만듬(HPA?)
이중화를 위해서 2개의 장비를 사용하는데, L4 스위칭 장비를 사용(외부에서 들어오는건 L4를 무조건 지나감

C#으로 만든 차트서버나 스마트DSP는1유레카에서 등록/해제를 하기위해 따로 세팅해줘야함(기본적으로는 Spring에서는 유레카클라이언트가 지원해줌


```
Ribbon - Client-side Load balaner 
S/W기반으로 비용이 저렴함. 어플리케이션에서 서버리스트를 관리하여 유연하게 대응 가능.

일반적인 서버사이드 로드밸런서는 H/W기반이여서 비용 많이 소모됨. 
H/W가 서버 목록을 알고있어야 로드밸런싱 가능.
H/W 스위치의 서버 목록을 수동으로 추가해서 유연성 저하.
```

```
서킷브레이커 - hystix
A서비스에서 B서비스를 호출할때 동기형식으로 호출하는데 기존에는 A에서 B를 호출하면 응답이 올때까지 대기하면서 죽어버림.

```


```
흐름 : 외부에서 서비스 요청(예약서비스 요청) -> Zuul(API gate)에서 받아서 유레카서버에서 서비스 목록 확인 -> 서비스 라우팅 -> 서비스 호출
-> 비지니스 로직 수행 

엘라스틱에 스위치에서 ServicePool을 호출했던 로그를 가지고있다가 바로 해당 service pool이 있는 장비로 연결해줌.

```

- Ansible : 배포하는 서버가 여러개인 경우 도입하는걸 고려해볼만함. (DEV, QA, PROD가 있고 해당 서버들이 각각 여러개라면?)



```
<로그>
beat(비치)는 로그스태쉬로 로그를 전송하고,
로그스태쉬는 수집
엘라스틱서치는 정제하고
키바나는 
```
