# Cloud-Lv3

4월 : 4/4 ~ 4/15 

5월 : 중간평가 W/S 

최종평가 : 7월말~8월초

https://miro.com/app/dashboard/ 

https://app.gather.town/app/9HTmUf3uGr7IR3To/AMF-L3    비번 : 0404

## 일정

![image](https://user-images.githubusercontent.com/35188271/163151315-dc66d963-8a0e-4b10-9fae-08944ec3db60.png)

![image](https://user-images.githubusercontent.com/35188271/163151519-2cfe6cef-f96a-4c67-be50-f07786f7a843.png)

## 상세 일정
![image](https://user-images.githubusercontent.com/35188271/163078148-53d33a95-4cac-4d2e-b40e-4acf9ab9b92c.png)

![image](https://user-images.githubusercontent.com/35188271/163078217-db32d23c-d550-4f6c-9fdb-71434fba49d4.png)





# 


# MSA 교육


![image](https://user-images.githubusercontent.com/35188271/161655449-eaaa2feb-6477-4c90-8c7d-6d371346f6a0.png)



1. 고객-공급자(Customer-supplier)
ㅎㅇ
ㅎㅇ
2. 준수자(Conformist)

3. 충돌방지계층

=========================================
CQRS(Command and Query Responsibility Segregation) = 조회성(R)과 CUD를 분리

마이크로 서비스 9가지 특징
컨테이너 Docker
Docker : 대표적인 컨테이너
컨테이너 관리 : 컨테이너 오케스트레이션
DevOps 환경
CI(Continuous Integration) 지속적 통합 - 자동으로 통합하고 테스트하고 레포트로 남기는 활동

CD 지속적 배포

CD(Continuous Delivery) - 배포담당자가 중간에 승인하고 배포.
CD(Continuous Deployment) - 자동 배포
파이프라인
통합 및 배포까지 일련의 프로세스를 하나로 연계하여 자동화하고, 시각화된 프로세스를 구축하는 것.

Spring Cloud = Netflix OSS

===========================================

U - 제공자 D - 받는자.

전략적 설계 - 바운디드 컨텍스트, 유비쿼터스 언어(바운디드 컨텍스트를 유비쿼터스 언어로 모델링 하는것이 핵심) 전술적 설계

도메인 주도 설계 중요 세가지

바운디드 컨텍스트 - 비지니스내에서 서로 경계영역을 만듬
서브도메인 -
유비쿼터스 언어 - 모든 팀원이 사용하는 공통 언어(책임자,개발자,도메인전문가 서로가 이해할 수 있는 언어)
공유커널 - 바운디드컨텍스트 사이에 교집합.

충돌방지계층 ACL(Anti Coruuption Layer) - Legacy와 같이 제거,변경할때 사용

공개 호스트 서비스 - 바운디드 컨텍스트와 결합하고 싶어하는 모든 서비스에게 줄 수 있는 프로토콜이나 인터페이스 공개

발행된 언어 -

도메인 이벤트 - 비지니스 관점의 중요한것을 따로 독립적인 호출형태로 만듬? (호출사용으로 결합도를 낮추고, 독립성 높힘)

DDD 패턴(Domain Drive Design) - 핵심 비지니스가 변화가 잦음, 복잡함, 핵심 서브 도메인 Simple CRUD Pattern - 간단하고, 규칙이 적음, 데이터 조회성 업무, 지원/일반 서브도메인




## MSA란
1.

2. microservice.io 들어가면 예시 할 수 있음.


- Domain Event : 메인 이벤트들(상품 등록, 회원가입, 구매 요청, 배송 요청 등)
- External System : 리뷰,포인트 같은 시스템(외부시스템)
- Hot Spot : 어떤 이슈가 생겨서 추가적인 예외 상황 처리
- ㅁㄴㅇㄹ
- Actor / Roll : 게스트,사용자 정의
- Entity / Aggregation : 
- Bounded Context 찾기 : 비슷한 영역끼리 묶기
- Microservice 찾기 : Bounded Context에서는 구매와 결제를 묶었는데, 실제로 보니 구매와 결제는 분리해야한다고 판단할 수 있음.
- Service Mapping Diagram : 
- Service Specification : API, Data, Stories, Risk, UI 등 세부화.





# 2일차

## 이벤트 스토밍

주황색 = 행위주체(회원가입됨)
파란색 - 회원가입요청
노랑색(작은거) - 행위자
핑크 - 외부와 연결
![image](https://user-images.githubusercontent.com/35188271/161656010-f16fdc99-d0b8-4afa-b519-a079e31b6e75.png)
초록색 - 속성(컬럼)목록


## User Story

