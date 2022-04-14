# React

https://okdevtv.com/

[ 라우터 관련 정보 ] 
https://reactrouter.com/docs/en/v6/getting-started/overview#overview  
https://okdevtv.com/mib/react/router  


- `웹 모듈 오픈소스 사용량` : http://www.modulecounts.com/
- `웹 기초 접근` : https://www.w3schools.com/
- `react` : https://ko.reactjs.org/docs/components-and-props.html
- 'javascript' : https://developer.mozilla.org/ko/docs/Web/JavaScript
- 'CORS 지식' : https://developer.mozilla.org/ko/docs/Web/HTTP/CORS



Pakcage.json이 있으면 `npm i` 명령어는 기본으로 해야함.





## ReactDOM

툴체인 = 자동으로 프로젝트 환경 소스를 구성해줌.  
Vite.js(



## react
npm create vite firstreact
cd firstreact
npm i
npm run build

npx(설치는 안하고 기능만 다운받아서 실행)



- `그냥 올리는거보다  빌드해서 배포를 해야 난독화+최적화 된 상태로 동작함.`
- ㅁㄴㅇㄹ



- 자바스크립트 공부 : https://ko.javascript.info/
- 라우터 관련 : https://reactrouter.com/docs/en/v6/getting-started/overview#overview
- 라우터 관련 : https://okdevtv.com/mib/react/router



# front 2일차

1. `thunder Extension 설치` : http던져줄때 편한 툴.

[ restjpa ]
okreact-> restjpa폴더 -> spring-boot:run 진행.

- `데이터 푸쉬` : 
![image](https://user-images.githubusercontent.com/35188271/163293429-814e6198-e4c1-4d1d-b37d-cf8b1041851b.png)

- `데이터 조회` : 
![image](https://user-images.githubusercontent.com/35188271/163293450-6da882a2-8db8-46fc-bbc7-1f2076ccd74d.png)

- `데이터 삭제` : 
![image](https://user-images.githubusercontent.com/35188271/163294105-562e9a85-4bca-4ea4-a570-41a7e2f36b0f.png)




[ restfrontend ]
`restfrontend 폴더이동`
`npm i`
`npm run dev`
`http://localhost:3000/`


[ 타임리프 ] 
```
restjpa->templates(폴더생성) -> index.html

restjpa
./mvnw
mvn spring-boot:run

```

[ 서버 구조 ]

![image](https://user-images.githubusercontent.com/35188271/163297861-d3fdd4d4-58ed-4d23-947d-7f6871d61b03.png)   

![image](https://user-images.githubusercontent.com/35188271/163298156-a4ce1235-30e3-4748-91a2-94524d244d7b.png)  

![image](https://user-images.githubusercontent.com/35188271/163298276-9deaceeb-e55a-4fb1-98e6-ac5c84310c30.png)  
CORS설정이 제대로 되어있어야 확인할 수 있다?

FE, BE 서버를 나눠서 사용하는게 좋다.

```
화면 넘어갈때 파라미터 전달?
localStorage.setItem('token','1234123asdf123');
localStorage.getItem('token');

jwt토큰 -> jwt.io에서 토큰 json형식 보여줌.
서버를 요청할때마다 쿠키를 날림.
```

