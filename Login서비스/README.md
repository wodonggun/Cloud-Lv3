## MSA 로그인 도메인

```
Account는 로그인서비스의 핵심 엔티티로 설정. 엔티티는 다른 엔티티와 구별되는 값과 값변경이 일어나는 객체여야함.
Address는 한글 주소와 우편번호가 존재하므로, 따로 VO(Value Object)로 빼서 관리(VO는 값을 수정하려면 삭제하였다가 새로 만들어야함)
계정마다 회원 등급이나 멤머타입이 있는데 이러한 값들은 따로 표준타입(Standard Type)으로 지정해서 관리함.
```


![image](https://user-images.githubusercontent.com/35188271/165228658-3b6e0e82-4d6d-47a2-b7a3-0ae83b17de3d.png)





```

```


## MSA Product 도메인

![image](https://user-images.githubusercontent.com/35188271/165231566-4293c797-26cc-49d2-a47c-e89402e4663b.png)

상품마다 가격이 정해지지만, 혹시 색상에 따라 가격이 변하고 싶다면
Prodct엔티티에 ProductDescription이라는 엔티티를 넣고, 그 엔티티는 색상과 가격을 가지고 있는다.

