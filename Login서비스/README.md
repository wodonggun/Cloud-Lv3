# EV POWER GUARD

![image](https://user-images.githubusercontent.com/35188271/168420890-0d406419-bf78-46ff-b5e5-a82befa83a38.png)
![image](https://user-images.githubusercontent.com/35188271/168421044-09e0a99e-f1a9-4cc0-86bd-c24b1aef906e.png)



# 리엑트 강의
- 로그인 구현 : https://www.youtube.com/watch?v=WLdbsl9UwDc
- 리엑트 라우터 : https://www.youtube.com/watch?v=WLdbsl9UwDc
- 리엑트 router 버전 다운 : npm install react-router-dom@5.3.0
- 리엑트 MUI : https://www.youtube.com/watch?v=or3np70c7zU




# Oauth2

```
<참고 : https://www.youtube.com/watch?v=HtJKUQXmtok>

npx create-react-app client


(npm install gapi-script react-google-login --save --legacy-peer-deps)
npm install gapi-script react-google-login

```




# JWT
![image](https://user-images.githubusercontent.com/35188271/193027801-92991516-5dfa-4ae9-85b7-cdbbe0e41234.png)  

1. 쿠키 - .env파일로 쿠키시크릿키를 가지고있고, gitignore에 .env랑 node_modules 포함해야함. 쿠키에 모든걸 담으면 무거워지고, 임의 조작 및 탈취 가능함. 사용자 Client단에서
이러한 criticla한 정보는 담으면 안됨.
2. 세션 - 쿠키에 세션ID를 보관함. 서버에서 세션 관련 정보를 저장하고 DB에 접근해야해서 자원 많이 잡아먹음(분산서비스에서는 부적절)
3. JWT - Json Web Token
![image](https://user-images.githubusercontent.com/35188271/193028229-0506624a-b492-4642-a5e0-991236da3ad0.png)




## MUI

- npm install @mui/material @emotion/react @emotion/styled @types/react
- `가이드문서` : https://mui.com/material-ui/react-button/
- npm install @mui/icons-material






## MSA 로그인 도메인

```
Account는 로그인서비스의 핵심 엔티티로 설정. 엔티티는 다른 엔티티와 구별되는 값과 값변경이 일어나는 객체여야함.
Address는 한글 주소와 우편번호가 존재하므로, 따로ㅇ VO(Value Object)로 빼서 관리(VO는 값을 수정하려면 삭제하였다가 새로 만들어야함)
계정마다 회원 등급이나 멤머타입이 있는데 이러한 값들은 따로 표준타입(Standard Type)으로 지정해서 관리함.
```


![image](https://user-images.githubusercontent.com/35188271/165228658-3b6e0e82-4d6d-47a2-b7a3-0ae83b17de3d.png)





```

```


## MSA Product 도메인

![image](https://user-images.githubusercontent.com/35188271/165231566-4293c797-26cc-49d2-a47c-e89402e4663b.png)

상품마다 가격이 정해지지만, 혹시 색상에 따라 가격이 변하고 싶다면
Prodct엔티티에 ProductDescription이라는 엔티티를 넣고, 그 엔티티는 색상과 가격을 가지고 있는다.


## 인증구현


토큰 만료 구분 

```addSignOutIntercettor: (signOut: ()=> void, refreshToken: (payload: SignResponsePayload) => void) => {
  ajax.interceptors.response.eject(curInterceptors.response)
  curInterceptors.response= ajax.interceptors.response.use(
   (response) =>response,
   (error)=> {
      const isSignInRequest = error.config.url === '${baseURL}/users/signIn';
      const isRefreshResponse: boolean = error.response.data && error.response.data && error.respnse.data.token;
      const expired= error.response && error.response.status ===401 && !isSignInRequest;
      
      if(isRefreshResponse && expired){
        refreshToken(error.response.data);
        return ajax.request(error.config);
      } else if(expired) {
          signOut();
          interact.snack({ message:'Session Expired. please signin again...', variant: 'error'});
      } else {
          interact.snack({ message : error.response.data.message, variant : 'error'});
      }
      return Promise.reject(error)
```

## 인증만료시 세션 연장
```
public Object run() throws zuulException{
try{
  String jwtToken = this.getJwtTokenInContext();
  Claims claims = Jwts.parser().setSigningkey(FilterConfig.JWT_SIGNING_KEY).parseClaimsJws(jwtToken).getBody();
  this.verifyAuthorization(claims));
  this.setHeaderToRequest(claims);
  }
  catch(ExpiredJwtExceptionex) {
  this.forwardingSessionExtendEndPoint(ex.getClaims());
  }
}
```

인증서비스에서 토큰 만료 혹은 세션 연장 시 401code와 함께 리턴 
```
@ApiOperation(value = "Acecess 토큰 재발급");
@RequestMapping( 
    value= "/auth/sign/refresh",
    method = {ReqeustMethod.DELETE, RequestMethod.OPTIONS, RequestMethod.GET, RequestMethod.POST, RequestMethod.PUT}
    }
public ResponseEntity<SignResponse> refreshToken(
  HttpServiceRequest request,
  @RequestHeader(AccessTokenField.MEMBER_ID_KEY) String userId,
  @RequestHeader("Authorization") String accessToken
  ){
    String requestIp = WebHelper.getIpAddress(request);
    return new ResponseEntity<>(signService.extendSession(userId, requestIp, accessToken), HttpStatus.UNAUTHORIZED);
    
  }

@ExceptionHandler(ExpiredJwtException.class)
protected ResponseEntity<String> handleExpiredJwtException(){
  return new ResponseEntity<>( body: "Session expired! please login again.", HttpStatus.UNAUTHORIZED);  //UNAUTHORIZED = 401 code
}
```

## 나중에 참고할거
- 로그인 구현 
https://github.com/LeoHeo/collect/tree/develop/src/main/java/com/collect/domain/user
