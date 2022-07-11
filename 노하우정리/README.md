

`성수석님 프로젝트` : https://github.com/hyejinsklearning/mybnb_hyejin


```
성수석님 DT lv3 질의
1. microservice design - strategic design.ppt 1, 27 페이지 참조
2. microservice development Hands -On_v1.1.ppt 21, 31 페이지 참조
3. 전자정부 프레임워크 가이드에서 polyglot 참조

//////////// 질문

1. TCL 에서 자신이 맡은 부분 설명 
(설명하다가 심사위원이 궁금한거 있으면 질문함)

2. 왜 래빗엠큐 안쓰고 카프카 사용했는지?
(다른 프로젝트의 경우 시스템 특성 상 래빗엠큐가 좋아서 질문)

3. JPA 사용 시 본인이 느낀 장단점

4. 현재 맡은 운영업무 설명 / MSA 로 전환 시 무엇이 필요한가 ? 
(공통질문같음)

1. 본인이 한 일
2. CQRS 패턴 적용시  consumer가 집중되면 문제가 발생할텐데 해결법? 인벤트 소싱 패턴 적용으로 설명하였음
3. 이벤트 스토밍이 DDD 설계에 도움이 되던가? 기존 데이터 과점 개발과 MSA 관점을 비교하여 설명함
4. 현장에서 MSA 도입했을 때 우려점? 기존 싯ㅡ템 마이그레이션시 장애 발생 가능. 가벼운 시스템부터 적용하면서 기존 시스템은 ACL 을 둬서 차츰 변경하자고 함
```




```
영민이 DT lv3 질의
Polyglot
고가용성
무중단배포
세션 쿠키 차이

1. 인증 인가는 어떻게하냐?
ifact는 IAM인증인가 서비스가 따로있다.
로그인할떄 jwt토큰 생성(쿠키로 가지고있어야함)
리엑트 axios에서 UI인터셉터에 기능을 넣어서 자동으로 쿠키를 던질 수 있음.

세션은 메모리db라 크리티컬하다? = Reddis
https를 왜 안올렸냐 ? - ssl 설정이 귀찮고, 


세션 메모리db에 SSID(세션아이디)로  관리해야하는데
jwt토큰을 쿠키에 넣음.
---
CSR SSR = UI쪽
왜 react를 사용하였느냐? react랑 view랑 차이 장단점
Istio = 서비스메쉬 
API Gateway 장단점 = 로드밸런싱, 

zuul -> istio로 변경했는데 그 이유는 서비스가 죽으면 zuul이 알아차리는 시간이 좀 느려서 장애가 발생했을때 순간적으로
 고가용성 처리가 안됨.
istio는 pod에 사이드카 엔보이라는게 떠있는데 죽자마자 gateway에 던져버림.
유레카는 api gateway를 관리하는 서비스디스커버리.

View = 러닝커브가 짧고, 쓰기 쉬움.
React는 jsx = react는 범용성이 좋고, 오픈소스, 

서버사이드는 캐시에 렌더링된 파일을 가지고 있음.
(react,view)클라이언트사이드는 

request body를 암호화해서 던짐.
https 

https적용하던가

react쓰다가 힘든적은 없었는지? 

SPA(Single page Application) 처음에 미리 다 불러와서 client단에서 렌더링을 다 진행하기 때문에 느림.
레이지로깅 화면을 다 분할된 리소스로 관리하였다.

DOM = 브라우저가 알고있는 마크업 객체 구초.
react나 view는 Virtual Dom을 사용하는데, 효율적으로 돔을 관리하려고 한다.

vanilla.js는 순수 자바스크립트 기반 코딩방식.

html5 마크업 패턴
```
