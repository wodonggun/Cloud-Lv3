<Event-Stroming 참조> https://github.com/event-storming/ddd-petstore 


# Front설치
![image](https://user-images.githubusercontent.com/35188271/162121551-77001736-01d4-4f0f-b96d-51a1e8d88eeb.png)




# Back-End 설치
![image](https://user-images.githubusercontent.com/35188271/162121717-b17c7da9-f742-44c1-b0f8-02fc2fd1b61d.png)

## Chocolatey 설치 (Windows전용)

![image](https://user-images.githubusercontent.com/35188271/162121816-6aa06d76-3cf0-4602-9a31-9c7a6b41308a.png)
![image](https://user-images.githubusercontent.com/35188271/162121901-e029513a-2a98-4122-842a-64aecb1ea916.png)
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
- `설치 확인 : choco`

## 

  
  
  
  
  
  
  
  # 실습
  
  ## 유틸리티 설치(httpie)
  `pip install httpie`
  
  ## 
  
  
  
  
  ### 예시
  
  
![image](https://user-images.githubusercontent.com/35188271/162150084-94ad4996-5ea8-4629-aa2d-d920eb622d6b.png)  
domain에 우클릭 -> NEW File ->Health.java 생성 -> 

![image](https://user-images.githubusercontent.com/35188271/162150480-ee57bfd0-f07b-4bab-92e2-22247a212ea6.png)  
![image](https://user-images.githubusercontent.com/35188271/162150923-b5a0e0de-6f90-449f-bfc6-e302f35a9c08.png)  
![image](https://user-images.githubusercontent.com/35188271/162151121-daa5b562-ba9a-45a0-9511-fbe5cd76b9df.png)










# Gateway

## 실습 예시

![image](https://user-images.githubusercontent.com/35188271/162361748-54187e1d-bc0e-4917-b40f-02143e2f7c9b.png)

8080으로 들어오면 8081, 8083으로 분배해줌.

  
  
## 제이든님

![image](https://user-images.githubusercontent.com/35188271/162383355-d1ba5a99-3c3e-4819-a657-026b60c4a544.png)
kafka 

postpersist = 이벤트발행하는곳

onPostPersist() = 

policyhandler.java ? 공부해야함.

kafka consume을 통해서 확인할 수 있다. 


## 헥사고날/클린 아키텍처

![image](https://user-images.githubusercontent.com/35188271/162599108-fce75445-a069-4295-a4e7-1b9504a3b368.png)

https://www.youtube.com/watch?v=MKfSLrwLex8

![image](https://user-images.githubusercontent.com/35188271/162598905-37c72d28-18c5-4bab-b57b-f64863833ce1.png)



## 라우트

https://cheese10yun.github.io/spring-cloud-gateway/

![image](https://user-images.githubusercontent.com/35188271/162600668-625817c0-0a3d-441c-9451-117cccc5c5a3.png)

![image](https://user-images.githubusercontent.com/35188271/162600659-3ecdb6b3-a186-4d12-8a70-c1e06b7d27da.png)


## OAuth 통합 로그인
![image](https://user-images.githubusercontent.com/35188271/162600764-d36d19e7-52f7-4376-b346-b1f3e8e502ba.png)


==================================================================================================================================

# 2주차

## 시스템 환경변수
C:\Users\User\Desktop\kubeconfig.yaml

- choco 설치 (windows환경에서 필요한 패키지,설치프로그램 관련 툴) : 기존에는  Get-Package가 있었지만 현재는 choco가 편리해서 넘어감.
powershell -> 관리자권한실행 -> choco install kubernetes-cli  

- `kubectl version` 명령어를 통해 설치 확인.

## 

kubectl config set-context --current --namespace=edu001

## Orchestration

## Pod
쿠버네티스에서는 컨테이너를 pod로 생각함.
컨테이너 하나를 작업하기 보다는 여러개의 컨테이너를 사용해야하기 때문에

Pod는 컨테이너들의 모음을 모아놈.
재시작할 수 있는 Pod단위

## ReplicaSet
컨테이너 갯수를 알아서 조절함.

Deployment 생성
- `kubectl create deployment nginx002 --image=nginx`
- `kubectl get deployment`
- `kubectl get rs,pod`
![image](https://user-images.githubusercontent.com/35188271/162654487-6500bc12-8a5f-4c8e-acb7-8ed7b33e237c.png)  
- Replica이름으로 pod이름이 결정됨 -> 재시작할때마다 pod 뒤에 이름은 계속 바뀌게됨.
- `kubectl scale --replicas=2 deployment/nginx002` : replica에서 pod2개로 수정
- `kubectl delete pod nginx002-78d478bf9d-hz5zp`
- 

서비스 생성
Service는 앞단에서 pod로 통신을 이어준다.
- `kubectl create service clusterip nginx002 --tcp:80:80` : service 80생성
- `kubectl port-forward service/nginx002 30080:80` : 30080으로 요청온 서비스에서 로컬80으로 포팅하겠다?



# 
- `choco install kustomize`
- 


# ㅁㄴㅇㄹ
- edu002 수정
C:\Users\User\Desktop\awesome-shopping-master\awesome-shopping\config\overlay\dev\common\resource\application-common.yaml
C:\Users\User\Desktop\awesome-shopping-master\awesome-shopping\config\overlay\dev\account\kustomization.yaml
C:\Users\User\Desktop\awesome-shopping-master\awesome-shopping\awesome-account-service\build.bat




# Docker연결 실행 (cmd 관리자권한으로 실행)
1. windows상에 Docker프로그램이 실행중이여야함.
<Docker Restart 에러>
![image](https://user-images.githubusercontent.com/35188271/162681237-3bb143fb-d5db-43b4-aa82-839648cf1f9c.png)  
https://blog.nachal.com/1691


docker login hrd-registry.hrd.cloudzcp.net -u robot$edu002+edu002

mvnw.cmd clean install -DskipTests=true -s ../settings.xml

- 오류발생시
![image](https://user-images.githubusercontent.com/35188271/162678746-4379b13e-bcfd-4f92-8d11-ce7deb313cd5.png)
해당 version 명시

각 서비스별로 -> Build.bat 파일의 명령어 순서대로 실행.


<docker 빌드 오류시 참고>
![image](https://user-images.githubusercontent.com/35188271/162683493-b76a7b8b-5dd0-4a0b-b3a8-ed81160b65d2.png)
해당 ajr경로 위치를 이동.

해당 edu999->edu002 자신의 계정으로 변경.
C:\Users\User\Desktop\awesome-shopping-master\awesome-shopping\config\overlay\dev\account\kustomization.yaml
C:\Users\User\Desktop\awesome-shopping-master\awesome-shopping\config\overlay\dev\bff\kustomization.yaml
product..
payment...order...cart...


<k8s-all-batch파일 실행>
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/account | kubectl apply -f -
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/bff | kubectl apply -f -
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/cart | kubectl apply -f -
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/order | kubectl apply -f -
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/payment | kubectl apply -f -
kustomize build --load-restrictor LoadRestrictionsNone config/overlay/dev/product | kubectl apply -f -

![image](https://user-images.githubusercontent.com/35188271/162690158-e53cc190-c919-44b4-b986-038548c69f9e.png)
Ready 0/1에서 1/1로 올라가지않으면 자원이 꽉차서 더이상 생성 못하던가, 잘못 세팅해서 못올라갈 수 있음.

해당 명령어를 통해서 deployment를 통해 배포함.
`kubectl get deployment -n edu002`
`kubectl config get-contexts`

![image](https://user-images.githubusercontent.com/35188271/162690796-ff7f95f2-d409-4e6a-905a-60409020e37a.png)

<ingress> = 외부 로드밸런스.
`$ kubectl create –f config/ingress.yaml`
`kubectl get ingress`
`http://edu003.hrd-edu.cloudzcp.com/` : 홈페이지 접속
  

  ## 외전
  ![image](https://user-images.githubusercontent.com/35188271/162697163-0881be71-9372-4c5a-a49d-c280fb471902.png)
 
  <컨피그 패턴?>
 bff->awsome-title에 값을 넣으면 
  replicaset은 scale=1이라 최소한 1개의 정상적인 서버를 유지해야하므로,
  title값을 변경한 컨테이너는 빌드 배포가 완료되어야 이전 컨테이너(title값 변경전)를 내리고,
  즉시 title변경된 컨테이너를 구동시킴.
 
    
