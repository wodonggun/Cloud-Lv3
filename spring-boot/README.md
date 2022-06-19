## Spring-boot

![image](https://user-images.githubusercontent.com/35188271/174466360-08e3540e-930d-4b0b-a7b5-6c266fba7a66.png)


- 'controller` : API요청에 따라 어디로 보낼지 결정
- `Service` : Controller에서 온 데이터를 처리함(비지니스 로직을 담음)
- `DAO` : Repository로 Service에서 가공된 데이터를 Entity형식으로 받아서 DB랑 1:1매핑을 저장
- 



```
VO와 DTO는 혼용되어서 사용하지만, VO는 값 객체로 불변이 라는 Read only라는 특성을 가진다.
하지만 DTO경우에는 
```
