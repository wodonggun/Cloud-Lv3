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

## netlify 배포방법
https://velog.io/@ksmfou98/React-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Netlify%EC%97%90-%EB%B0%B0%ED%8F%AC%ED%95%98%EA%B8%B0

