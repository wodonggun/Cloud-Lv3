# MSA 


## 이벤트 스토밍

`DDD` : Domain Driven Design 도메인 기반으로 주도하는 디자인 패턴

>> Front-End, Back-End, UI/UX, 업무담당자, PM 등 다양한 사람들이 모여서 구상할 수 있다.


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


## 장애 차단 / 격리

1. 서킷브레이커 패턴
2. 2-phase commit 패턴
3. CQRS
4. Saga패턴

## 헥사고날 아키텍처

- `참고` : https://mesh.dev/20210910-dev-notes-007-hexagonal-architecture/  

![image](https://user-images.githubusercontent.com/35188271/164975873-a68efb7e-7ee2-4258-a109-9ddc63cf585b.png)


![image](https://user-images.githubusercontent.com/35188271/164958825-f9aa7d1c-0623-4086-92ad-c7bb8ee8ae06.png)  

1. 아키텍처 확장이 용이합니다.
2. SOLID 원칙을 쉽게 적용할 수 있습니다.
3. 모듈 일부를 배포하는 게 용이합니다.
4. 테스트를 위해 모듈을 가짜로 바꿀 수 있으므로 테스트가 더 안정적이고 쉽습니다.
5. 더 큰 비즈니스적 가치를 갖고 더 오래 지속되는 도메인 모델에 큰 관심을 둡니다.





