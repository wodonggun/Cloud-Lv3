# MSA 


## 이벤트 스토밍

`DDD` : Domain Driven Design 도메인 기반으로 주도하는 디자인 패턴

>> Front-End, Back-End, UI/UX, 업무담당자, PM 등 다양한 사람들이 모여서 구상할 수 있다.


![image](https://user-images.githubusercontent.com/35188271/164958428-655e2aed-6806-410e-b26e-aa9dc8f5fbf6.png)

![image](https://user-images.githubusercontent.com/35188271/164958558-adcccaa5-cb48-472a-bcac-5ca2de30012c.png)

![image](https://user-images.githubusercontent.com/35188271/164958562-6fb3c628-9771-4ff3-b06f-61d18bbdc54d.png)

![image](https://user-images.githubusercontent.com/35188271/164958593-7f5989da-3fd0-4bab-9db7-236d862cd9ff.png)

![image](https://user-images.githubusercontent.com/35188271/164958605-db89da35-f5b1-4407-ba61-16031bc6c514.png)

--- 
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


