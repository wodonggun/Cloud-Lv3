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
  
  



