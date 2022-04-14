# React

- `교재` : https://bit.ly/okreact2022
- 

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


UI : 부트스트랩, 테일윈드(요즘떠오름)

- `front 배포` : https://app.netlify.com/teams/wodonggun/overview


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

## FE 배포 관련
![image](https://user-images.githubusercontent.com/35188271/163320980-1a1db260-8618-4233-a326-127d236c616a.png)


https로 호출해야함.
![image](https://user-images.githubusercontent.com/35188271/163321187-4d9d1323-c252-443d-aacf-4194587e2748.png)



[ netlify 환경변수 설정 ]
![image](https://user-images.githubusercontent.com/35188271/163321535-b2b97a85-16a7-4eb2-847b-3504acf9b3eb.png)

![image](https://user-images.githubusercontent.com/35188271/163321638-07c25aa4-d824-4879-80f9-90cf7338a5ee.png)



https://kenureact.netlify.app/

https://github.com/kenu/10ynews-spring-boot/blob/master/scripts/install-env.sh


![image](https://user-images.githubusercontent.com/35188271/163322818-9fc418a3-9d52-440e-b888-6873f91723fd.png)
이해안됨

[front]
restfrontend
npm run build

[back]
restjpa -> ./mvnw 

![image](https://user-images.githubusercontent.com/35188271/163328404-e30e5fad-a3f0-4c5b-9b0a-ffccb257b10b.png)
restjpa가 위와 같은 패턴이다.


부모 -> 자식으로 데이터전달(Props)은 가능하지만, 자식에서 부모로는 못하면서 아래와 같은 기술이 있음.
![image](https://user-images.githubusercontent.com/35188271/163333593-23703333-3c27-4e66-aa6a-9cba92e452fb.png)



## 정리

![image](https://user-images.githubusercontent.com/35188271/163334759-5f94a44a-4365-48db-9caa-140b60795b65.png)

![image](https://user-images.githubusercontent.com/35188271/163335648-da71dbcb-f095-45ad-b309-b95c2b693bd0.png)



## 한상훈 매니저 강의
1. npm run build(package.json 참고하셈) (npm run dev는 데브용으로 로컬용이라 파일들도 같이 포함안시킴)
2. asdf
3. ajax("/communication/users/profile/12345")
4. sadf




[ 서버에 FE올리기 위한 작업 ]
1. Dockerfile수정
![image](https://user-images.githubusercontent.com/35188271/163343147-f3c6701d-9782-428b-90ed-9096a817f9b8.png)  
`npm install` = packagemodules 폴더를 가져옴.
`npm run build` = app/dist폴더가 생성됨

2. ![image](https://user-images.githubusercontent.com/35188271/163343682-a68f999c-f787-4c3a-8958-ebe566b46e28.png)
캐쉬를 안받도록 처리를 해줘야함.

3. assets에 들어가는  
favicon.17e5045123 -> 뒤에 해시값을 넣음.  
![image](https://user-images.githubusercontent.com/35188271/163344266-066ed3ca-d149-4cac-afeb-df59a1bd3fc2.png)  
assets는 알아서 캐시처리를 해라.

4. AMDP  
![image](https://user-images.githubusercontent.com/35188271/163344925-8a6893f2-bb2b-40f9-b2c2-bc8520f6e842.png)
컨테이너 생성 -> SNAPSHOT말고, REACT로 변경해서 저장.
```
프론트엔드 마이크로서비스 추가 과정
* 다 동일한-데
* App Framework : React
* 기본설정 > static resource > path 기본값사용해제 후 /assets
* 프로파일 설정 > 네임스페이스 선택

프론트엔드 마이크로서비스 빌드설정 -> 설정 -> dockerfile-ci (호환프레임워크가 REACT이니까)

github.com/AMF-skcc/AMF2022

https://github.com/AMF-skcc/AMF2022/tree/main/cloud-zcp
Dockerfile과 nginx.conf
프론트엔드 애플리케이션의 루트경로에 넣어주세요
dockerfile-ci 파이프라인 활성화 하여 빌드배포
```

[ DB 추가 과정 ] 

config형상 git repo는 반드시 private으로 지정해야 한다

```
데이터베이스 추가 과정
1. 프로파일의 백엔드 탭에서 추가를 한다
2. 원하는 타입의 백엔드의 접근정보를 입력한다
3. 접속성공 여부를 확인한다.
4. 마이크로서비스 상세로 가서 수정을 한다
5. 기본설정 하단의 데이터&메세지 관리 설정
6. 에서 추가한 백엔드(DB,MQ,..)를 선택한다.
7. 저장을 한다.
8. 코드생성을 한다
9. Config git 가서 이쁘게 잘 들어갔나 본다
```

===
nginx.conf의 캐시설정 이유
* index.html이 참조하는 리소스 파일명은 버전과 같은 기능을 한다
* 파일명==컨텐츠/파일내용
* index.html은 버전업에 대응하여 웹브라우저에게 항상 새 버전을 내어주어야 함. 따라서 캐시 미사용.
* assets/* 은 버전업시 새로운 파일들이 들어가지만, 마찬가지로 파일명==컨텐츠/파일내용이기 때문에, 여기에 올라가는 파일들은 캐시처리를 해도 무방하다.
* 라우터 설정에 의해 새로운 경로로 들어가게 되더라도 실제 업무로직은 /index.html이 처리, 다만 url은 새로운 경로 기준으로 react등이 알아서 잘 처리한다.
* ingress설정시 프론트엔드 라우터들이 명칭을 침범하지 않도록 주의한다. assets와 같은 경로도 마찬가지로 주의.



