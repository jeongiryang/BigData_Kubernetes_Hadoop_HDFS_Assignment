# Kubernetes 기반 Hadoop Single Node HDFS 실습 보고서

## 과제 개요

본 실습은 Kubernetes 환경에서 Hadoop Single Node HDFS를 실행하고, HDFS Web UI와 HDFS 명령어를 통해 HDFS의 기본 동작을 확인하는 것을 목표로 한다. Hadoop은 Pod 또는 Deployment로 실행하며, Web UI 접속과 HDFS 파일 저장 과정을 함께 확인한다.

## 과제 요구사항

![쿠버네티스 과제 슬라이드](screenshots/raw/00-assignment-slide.png)

- Kubernetes에서 Hadoop Single Node를 Pod 또는 Deployment로 실행한다.
- YAML 파일 기반으로 Hadoop Single Node 환경을 구성한다.
- Port-forwarding 또는 Service를 이용해 HDFS Web UI에 접속한다.
- HDFS Web UI 또는 HDFS 웹 브라우저 화면을 확인한다.
- Pod 또는 Deployment 내부에 접속해 HDFS 명령어를 실행한다.
- `hdfs put` 또는 `hdfs dfs -put` 명령어로 데이터를 HDFS에 저장한다.
- 전체 실습 내용을 PDF 보고서로 정리한다.

## 실습 환경

| 항목 | 내용 |
| --- | --- |
| OS / VM 환경 | 실습 진행 후 작성 |
| Kubernetes 환경 | 실습 진행 후 작성 |
| `kubectl` 버전 | 실습 진행 후 작성 |
| Hadoop 이미지 | 실습 진행 후 작성 |
| 실행 방식 | 실습 진행 후 작성 |
| HDFS Web UI 접속 방식 | 실습 진행 후 작성 |

## Step 1: Hadoop Single Node 실행

Kubernetes 클러스터 상태를 확인한 뒤, Pod 또는 Deployment 방식으로 Hadoop Single Node를 실행한다.

### 실행 명령어

```bash
kubectl get nodes
kubectl get pods

kubectl apply -f <hadoop-single-node-yaml>
kubectl get pods -o wide
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

### 실행 결과

```text
실습 진행 후 작성
```

### 스크린샷

```text
실습 진행 후 작성
```

## Step 2: HDFS Web UI 접속

Port-forwarding 또는 Service를 이용해 Hadoop HDFS Web UI에 접속하고, NameNode 및 HDFS 상태를 확인한다.

### 실행 명령어

```bash
kubectl port-forward pod/<pod-name> 9870:9870
kubectl get svc
```

### 접속 주소

```text
실습 진행 후 작성
```

### 실행 결과

```text
실습 진행 후 작성
```

### 스크린샷

```text
실습 진행 후 작성
```

## Step 3: HDFS 명령어 실행 및 데이터 저장

Pod 내부에 접속해 HDFS 기본 명령어를 실행하고, `hdfs dfs -put` 명령어로 샘플 데이터를 HDFS에 저장한다.

### 실행 명령어

```bash
kubectl exec -it <pod-name> -- bash

hdfs dfs -ls /
hdfs dfs -mkdir -p /user/root/input
printf "sample data\n" > /tmp/sample.txt
hdfs dfs -put -f /tmp/sample.txt /user/root/input/sample.txt
hdfs dfs -ls -R /user/root
hdfs dfs -cat /user/root/input/sample.txt
```

### 실행 결과

```text
실습 진행 후 작성
```

### 스크린샷

```text
실습 진행 후 작성
```

## 실행 결과 정리

| 구분 | 결과 |
| --- | --- |
| Hadoop Single Node 실행 | 실습 진행 후 작성 |
| HDFS Web UI 접속 | 실습 진행 후 작성 |
| HDFS 명령어 실행 | 실습 진행 후 작성 |
| HDFS 데이터 저장 | 실습 진행 후 작성 |
| 주요 문제 및 해결 | 실습 진행 후 작성 |

## 결론

실습 진행 후 작성
