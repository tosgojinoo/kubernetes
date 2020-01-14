# Kubernetes

## 역할
+ 핸들링은 docker 가, 최적화는 kubernetes
+ Container Ochestration : 스케줄링, 클러스터링, 서비스 디스커버리, 로깅/모니터링 중앙 관리

## 오케스트레이션 중 kubernetes의 선점 이유 
+ 사용하기 편한편(json 형태)
+ 커뮤니티 파워
+ 다른 서비스) docker swarm

## backup
+ ETCD 초기에는 1개로 구성, 이후 늘려줘야 함
+ Cluster 에서는 보통 백업의 개념은 없고, 서비스의 연속성을 꾀하는 방식
+ manual 형태로 cluster 증대

## Container
+ 애플리케이션과 그 실행에 필요한 라이브러리, 바이너리, 구성 파일 등을 패키지로 묶어 배포하는 것
+ 하면 노트북-테스트 환경-실제 운영환경으로 바뀌어도 실행에 필요한 파일이 함께 따라다니므로 오류를 최소화
+ 운영체제를 제외하고 애플리케이션 실행에 필요한 모든 파일을 패키징
+ '운영체제 레벨 가상화'
+ 예) docker

## docker vs VMware
+ docker 의 경우 resource 를 share 함

## for data
+ big data platform 구성 용도
+ container 위에 kafka, spark 등을 올림
+ container image 를 구성한 후에, kubernetes registry 에 등록하여 배포