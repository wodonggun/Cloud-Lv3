# MSA 

- `K-MOOC 강의(MSA 개념용 강추)` : http://www.kmooc.kr/courses/course-v1:KAISTk+2018_K14+2021_K14_01/video
- ㅁㄴㅇㄹ


## 이벤트 스토밍

`DDD` : Domain Driven Design 도메인 기반으로 주도하는 디자인 패턴(크고 복잡한 비즈니스 도메인을 이해 및 탐구하는 활동)
![image](https://user-images.githubusercontent.com/35188271/165102129-01f86c9a-b792-4508-9906-22c43bfdde72.png)  
>> Front-End, Back-End, UI/UX, 업무담당자, PM 등 다양한 사람들이 모여서 구상할 수 있다.

![image](https://user-images.githubusercontent.com/35188271/165102880-965a86c4-8550-48e0-9975-7dbe3334dc49.png)  

![image](https://user-images.githubusercontent.com/35188271/165103772-939dde01-5767-4039-a889-9961bdb21545.png)

![image](https://user-images.githubusercontent.com/35188271/165102938-3f33c277-7c51-403e-b40d-e4a45345e680.png)  

![image](https://user-images.githubusercontent.com/35188271/165103533-c41f397a-2619-45c9-a7d7-a26a66769399.png)



--- 
![image](https://user-images.githubusercontent.com/35188271/164958428-655e2aed-6806-410e-b26e-aa9dc8f5fbf6.png)

![image](https://user-images.githubusercontent.com/35188271/164958558-adcccaa5-cb48-472a-bcac-5ca2de30012c.png)

![image](https://user-images.githubusercontent.com/35188271/164958562-6fb3c628-9771-4ff3-b06f-61d18bbdc54d.png)

![image](https://user-images.githubusercontent.com/35188271/164958593-7f5989da-3fd0-4bab-9db7-236d862cd9ff.png)

![image](https://user-images.githubusercontent.com/35188271/164958605-db89da35-f5b1-4407-ba61-16031bc6c514.png)

![image](https://user-images.githubusercontent.com/35188271/164958685-9eab50c9-344a-4267-960d-876b09ee4f72.png)


![image](https://user-images.githubusercontent.com/35188271/164973797-7213c67b-6b2f-41a8-ab9b-7f08f68ee033.png)


![image](https://user-images.githubusercontent.com/35188271/164973841-89484287-0811-4a2a-a612-ad2aaaadfd83.png)

![image](https://user-images.githubusercontent.com/35188271/164973869-fb2f26c8-90b2-4527-b5db-1e6027680b9e.png)

![image](https://user-images.githubusercontent.com/35188271/164973888-a8dd943d-1bff-4c2f-b9b0-6c321352903d.png)



--- 

## 예시 정리
![image](https://user-images.githubusercontent.com/35188271/164975663-be09e71e-2f22-435e-b57e-50019694a47f.png)




## Agile이란

![image](https://user-images.githubusercontent.com/35188271/164953057-51500de2-5f5d-44dc-b2b0-99b3e8a2bd96.png)  
`작은 단위의 목표를 잡고, 실패를 통해 계속 성장하는 문화 / 비용 중심 보다는 고객 중심의 사고`


## HTTP/REST API

![image](https://user-images.githubusercontent.com/35188271/164953177-e54e9f4a-5049-4570-b7ca-b5cd063ffffd.png)  
`동기화 방식으로 약결합`

## 메세지큐

![image](https://user-images.githubusercontent.com/35188271/164953481-ebe0a7b9-2c87-4c2c-a554-1fb672d68d9b.png)  
`비동기 방식으로 메세지큐에 데이터를 쌓아놓고 처리되면 결과를 리턴받음`




## MSA 장점

1. 서비스단위로 쪼개서 작은 코드량으로 이해하기 쉽고, 오류 찾기 쉬움.
2. 수정된 서비스에 대한 국지적 단위 테스트와 배포가 용이하다.
3. 장애 격리가 좋아짐
4. 여러가지 혼재된 기술 스택(신기술) 도입이 쉽다.
5. 개발환경을 구축하기 쉽고, 빠르게 기동
6


## 장애 격리

1. 서킷브레이커 패턴(Circuit Breaker)  
A서비스가 B서비스 호출을 했는데, 연속 실패 및 임계값을 초과하면 회로 차단기가 작동 -> B서비스에 대한 모든 호출을 즉시 실패로 반환함.

2. Fallback 처리
Fallback함수를 지정해놓으면, 장애감지 및 발생시 Fallback함수를 호출하여 서비스에 대한 호출을 막음.  
![image](https://user-images.githubusercontent.com/35188271/165090019-3f91bdc3-b3a4-490d-b6bd-bd0b95e0686c.png)  




## 분산 트랜잭션

1. 2-phase commit 패턴(2PC) : 다른 서비스에 장애가 발생하거나, Locking상태에 빠지면 영향을 줌.


2. Saga패턴 : 각 서비스의 Local DB를 업데이트하고, 다른 서비스의 Local DB를 변경하라고 트리거 이벤트를 발생.
하지만 위의 같은 상황에서 마지막 서비스의 DB가 실패하게되면 어떻게 롤백해서 데이터 일괄성을 유지할거냐? 
![image](https://user-images.githubusercontent.com/35188271/165097679-a674f2e5-6507-4a39-b44a-31a842f0d390.png)
  SAGA패턴 내에있는 서비스끼리 서로 보상 트랜잭션 이벤트를 발생시킴.

- `Choreography SAGA 패턴` : 트랜잭션 처리하고, 처리 이벤트가 승인되었는지, 거부되었는지 이벤트로 발행함(메세지큐)  
![image](https://user-images.githubusercontent.com/35188271/165098879-414b05ad-3454-4ac6-9be0-1f86c8e0fff2.png)  
  
` `Orchestration SAGA 패턴 ` : Orchestrater클래스가 따로 API호출하여 데이터 처리 요청 -> 처리후 다시 클래스로 반환됨(API=동기방식)  
![image](https://user-images.githubusercontent.com/35188271/165099328-d898e8d0-7a11-4212-93fd-34811416cd8e.png)



## CQRS 패턴

명령과 조회의 역할을 분리(쓰기/읽기용으로 DB 또는 테이블을 나눔)  
![image](https://user-images.githubusercontent.com/35188271/165100215-a88e442c-6b34-4600-9a94-4fcbbe416918.png)

- `이벤트 소싱` : 모든 C,U,D에 대한 작업을 DB수정후 이벤트로 발생시켜 이벤트 스트림 저장소(메세지큐)에 저장하는 방식.
- `이벤트 스트림 저장소` : 이벤트 들이 쌓이다가 특정 시점에서 축적된 데이터를 Read전용 DB에 업데이트  
(순간적으로는 DB가 불일치 하더라도 어차피 일치하게됨 = 결과적 일관성 Eventual Consistency)





## 롤백

보상트랜잭션 : 어떤 서비스에서 트랜잭션 처리에 실패한 경우, 서비스의 앞선 다른 서비스에서 처리된 트랜잭션을 되돌리게 하는 트랜잭션.




## 헥사고날 아키텍처


`Hexagonal의 필요성 제기 : 아래와 같이 기존 Layered아키텍처는 DB를 변경하려면 DAO 및 Business Logic Layer를 건드려야하는 경우가 생김.`  
![image](https://user-images.githubusercontent.com/35188271/165091609-641e3d3d-a4d3-476f-a899-12d07b6ebd59.png)  

![image](https://user-images.githubusercontent.com/35188271/165093221-8cf2b855-e0f1-4046-93dc-351b44659e83.png)


--- 

- `참고` : https://mesh.dev/20210910-dev-notes-007-hexagonal-architecture/  

![image](https://user-images.githubusercontent.com/35188271/164975873-a68efb7e-7ee2-4258-a109-9ddc63cf585b.png)


![image](https://user-images.githubusercontent.com/35188271/164958825-f9aa7d1c-0623-4086-92ad-c7bb8ee8ae06.png)  

1. 아키텍처 확장이 용이합니다.
2. SOLID 원칙을 쉽게 적용할 수 있습니다.
3. 모듈 일부를 배포하는 게 용이합니다.
4. 테스트를 위해 모듈을 가짜로 바꿀 수 있으므로 테스트가 더 안정적이고 쉽습니다.
5. 더 큰 비즈니스적 가치를 갖고 더 오래 지속되는 도메인 모델에 큰 관심을 둡니다.






## MSA 정리

`필수시청(강추)` : https://www.youtube.com/watch?v=BnS6343GTkY 

![image](https://user-images.githubusercontent.com/35188271/164983194-1bdf1898-bed9-43a2-b634-590ac95246a2.png)

```
배달의 민족의 경우에, 사장님이 가게정보를 수정하게 되면
모든 서비스에서 메세지큐에서 가져가서 알아서 수정함.
충전소/충전기 정보도 수정되면, Kafka 또는 Rest API를 통해서 전체다 알아서 받아서 수정하도록 설계해도 될듯.

가게/업주 정보 변경은 메세지큐에 ID와 조회, 삭제,수정 등 간단한 정보만 넣음(전체 데이터 또는 변경된값들은 넣지않음 = ZERO-PAYLOAD)

변경된/모든 데이터를 담아서 싣으면, 각 서비스마다 패킷의 크기가 너무 커짐.
각 서비스마다 원하는 정보 데이터도 다름.
(A가게정보를 짧은시간/트래픽몰릴때 여러번 수정하게되면, 메세지가 발행되어도 메세지큐에 순서대로 들어간다는 보장이 없음
= 메세지큐에 담겨있는 정보순서대로 가져왔다가 각 서비스DB를 수정했는데 알고보니 순서대로 메세지큐에 안들어옴
= 크게보면 어차피 각 서비스마다 필요에 의한 정보를 DB컬럼에 가지고있는게 다르기때문에, 어차피 다시 데이터를 다시 API던져서 봐야함)

각 서비스마다 정의된 API를 통해서 데이터 수정 정보를 가게/업주 서비스에 던져서 조회하고, 알아서 각 서비스DB를 업데이트 함.

<CQRS 쿼리모델>
배민 가게정보를 보면 메뉴,정보,리뷰 탭 등 가게ID당 엄청나게 서로다른 서비스의 정보를 보여줘야함(리뷰서비스,가게정보서비스, 가게목록 등)
가게정보를 읽어올때 각 여러정보를 미리 View전용(유저 서비스용 가게DB)에 가공해서 넣어서 가지고있다가
유저가 요청이오면 빠르게 보여줌.

가게목록조회 -> 광고 서비스(CQRS Query전용), 검색 서비스(CQRS Query전용), 찜 서비스(CQRS Query전용)에 해당 조회조건에 맞는 가게들 ID를 리턴해줌.
그 리턴된 ID + 가공된 데이터(Local DB에 해당ID로 조회함)를 key,value로 묶어서 빠르게 Front에 던져줌.
비동기+Non블로킹으로 설계됨.




```


## Eventual Consistency / Strong Consistency

`분산 시스템을 구성하려면, 일관성(Strong Consisttency)과 가용성(Eventual Consistency) 중 하나를 포기해야하는 상황이 올 수 있음`

>> 새로운 추가, 수정이 발생하더라도 조금 늦게 보여주거나 이전정보(수정전)를 보여주더라도 크게 문제없는 시스템에 사용 가능합니다.
>> 예를 들어서 SNS같은 서비스는 글자나 사진을 수정하더라도 몇초,길게는 몇분 수정전 내용을 보여주더라도 크게 리스크가 없다.(DNS서비스, 소셜미디어)
>> 하지만 은행, 결제, 실시간성이 중요한 정보에서는 

![image](https://user-images.githubusercontent.com/35188271/165011047-874d5404-4d4f-4a97-b6f6-f055e02d3eeb.png)

![image](https://user-images.githubusercontent.com/35188271/165011287-5cd3d986-8eb2-49f4-995c-13c8e51de811.png)

![image](https://user-images.githubusercontent.com/35188271/165011456-55d6f9eb-9d9e-4776-9938-dbc07013b666.png)

## OSI 7 Layer

![image](https://user-images.githubusercontent.com/35188271/165087927-4271f1a4-e868-4499-9502-d5fbb6552945.png)


## Netflix OSS

- `서비스 라우팅` : zuul, 리본  
![image](https://user-images.githubusercontent.com/35188271/165087678-27908fb1-2932-467c-aa71-6383877f0922.png)


## BFF(Backend For Front-end)

모든 Front(웹페이지,앱,응용프로그램 등)에서 하나의 Backend로 가지않고, 각 Front별로 최적화된 처리로 서비스

![image](https://user-images.githubusercontent.com/35188271/165088113-f51fc096-6a88-4c26-ad2d-12ccadce6f25.png)

## Service Registry

- `유레카` :   
![image](https://user-images.githubusercontent.com/35188271/165088804-7ac703b5-77af-44e8-8e5f-6f0c21afcfb4.png)


## Oauth

![image](https://user-images.githubusercontent.com/35188271/165089095-d0f4bb4c-e0ec-49cf-886f-5b21b5875db8.png)

로그인하면 Oauth를 통해 권한이 있는지 확인하고, Accesstoken 발급
이후에 Web에서 각 서비스들을 호출할때 엑세스토큰을 확인하고 접근을 허용해줌.


## Hyxstrix

장애 격리 및 모니터링 지원

## ELK

- `장애 서비스에 대한 로그 및 추적` : Elasticsearch(분석 엔진), Logstash(로그집합기), Kibana(대시보드) 3가지를 가지고, 로그서비스를 구성한것.



## Spring 정리

- Layer간 구분
![image](https://user-images.githubusercontent.com/35188271/165091365-77e78b01-d14a-452a-aaa8-dcd212aea0b8.png)


![image](https://user-images.githubusercontent.com/35188271/165091146-f96b3ea3-802d-4570-9977-5bcec89f4f80.png)  



## Front-End MSA로 나누기

`Server-side Page Fragment 컴포지션 방식` : 한페이지에 각 컴포넌트마다 각 서비스에 화면정보를 요청해서 읽어옴.  
![image](https://user-images.githubusercontent.com/35188271/165094535-a8b3d7fc-cba2-4eb8-b347-68a90d60b75d.png)



## Transaction Script 패턴 vs Domain Model 패턴

- `초보자도 쉽지만 비슷한 로직이 중복되는 현상이 생김`  
![image](https://user-images.githubusercontent.com/35188271/165095543-73648c0d-93c8-4b60-9bce-d2e7651a6a35.png)


- `복잡하지만 중복을 줄일 수 있음.`
![image](https://user-images.githubusercontent.com/35188271/165095659-0a085fab-7cd1-41bf-b96f-84f1a0daac81.png)


## DB

- `SQL Mapping방식` : 세밀한 SQL 튜닝 및 가공 가능.
- `OR Mapping방식(ORM)` : 간단하고, 개발자는 개발에 더 집중할 수 있음, 서로 다른 관계형 데이터베이스 전환 및 No-SQL 변경도 가능함.

