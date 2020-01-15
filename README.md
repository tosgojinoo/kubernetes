# Kubernetes

## 역할
+ 컨테이너 운영은 docker , docker를 관리해 주는 플랫폼이 kubernetes
+ Container Ochestration : 스케줄링, 클러스터링, 서비스 디스커버리, 모니터링 중앙 관리
+ 최소 10대 이상 사용할 때 효과적임

## 오케스트레이션 중 kubernetes의 선점 이유
+ 사용하기 편한편(json 형태)
+ 배포 편함
+ 자동화 관리 성능 및 연속성 좋음(health check 자동화 가능)
+ MSA(micro service archetecher)에 최적화
+ 커뮤니티 파워
+ 다른 서비스) docker swarm

## backup
+ ETCD 초기에는 1개로 구성, 이후 늘려줘야 함
+ Cluster 에서는 보통 백업의 개념은 없고, 서비스의 연속성을 꾀하는 방식
+ manual 형태로 cluster 증대

## Container
+ 애플리케이션과 그 실행에 필요한 라이브러리, 바이너리, 구성 파일 등을 패키지로 묶어 배포하는 것
+ 서비스를 배포할때 의존성을 최소화할수 있고 문제가 발생시 롤백이 간편함
+ 운영체제를 제외하고 애플리케이션 실행에 필요한 모든 파일을 패키징
+ '운영체제 레벨 가상화'
+ 예) docker

## docker vs VMware
+ docker 의 경우 resource 를 share 함

## for data
+ big data platform 구성 용도
+ container 위에 kafka, spark 등을 올림
+ container image 를 구성한 후에, kubernetes registry 에 등록하여 배포

## cluster
+ master & worker 로 구성
+ 3 ~ 50개 노드 커버함
+ 기본적으로 상호간 backup을 해주는 효과

## 고성능 단일 vs 저성능 멀티
+ 정부 : 고성능, 저탄소 규제 관련, 컨테이너간 간섭 문제 발생 가능
+ 기업 : 저성능, 전체 퍼포먼스는 올라감

## 향후 사용할 것들
kubespray
Rancher (Managed Kubernetes Platform)
CNI (Container Network Interface) : 칼리코, 플라넬

## 기타
### cloud vs on-promise
+ 초기의 경우 cloud 비용이 적음
+ 장기적으로 볼 경우 on-promise 비용 적음
+ cloud 의 경우가 비용이 더 발생, Out-bound 비용이 생각보다 큼
+ on-promise 구성시, 저사양으로 많이 넣어서 구성

