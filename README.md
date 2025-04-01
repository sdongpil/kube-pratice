eks 클러스터 생성 (역할 생성) -> 워커 노드 생성 -> 로컬에서 eks 연결

# AWS EKS - 로컬 연결

```bash
kubectl config get-contexts
```

### AWS EKS 클러스터 연결 (kubeconfig 업데이트)

```bash
aws eks --region ap-northeast-2 update-kubeconfig --name <EKS_클러스터_이름>
```

### 다른 클러스터로 전환

```bash
kubectl config use-context <컨텍스트_이름>
```

### 특정 컨텍스트 삭제

```bash
kubectl config unset contexts.<컨텍스트_이름>
```




### 매니페스트 변경 후 실행 순서

```bash
$ kubectl apply -f spring-secret.yaml
$ kubectl apply -f spring-config.yaml
$ kubectl apply -f spring-deployment.yaml
$ kubectl apply -f spring-service.yaml
```
