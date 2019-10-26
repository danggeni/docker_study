# Docker Install Ubuntu 18.04

## Docker Install 

### 설치 OS : Ubuntu 18.04.03 (2019.10.26 기준 작성)

## apt 목록 패키지 업데이트
---

 ```
    sudo apt update -y
 ```
 
## docker ce 의존 패키지 설치
---
```
    sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

## docker 패키지 장소 apt 지정
---
```
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) \ stable"
```

## apt 목록 패키지 업데이트
---
```
    sudo apt update -y
```

## 설치버전을 지정해 Docker CE 설치 
---
설치할 버전을 지정하지 않는 경우 최신버전으로 설치된다.
버전 선택하여 설치하는경우예시 \
ex) sudo apt install -y docker-ce=18.03 ce-0 ubuntu
```
    sudo apt install -y docker-ce
```

정상적으로 잘설치된 경우 docker version 명령을 실행해 버전정보 표기시
설치 완료

## docker 설치 완료 및 버전확인
---
아래 처럼 버전이 확인 된다면 정상적으로 설치 확인

![docker-version](docker_version.png)

## docker 명령어 Sudo 없이 사용하기
---
$USER 정보는 현재사용자 정보 \
직접 사용자 정보를 입력해도 됩니다.
```
sudo usermod -aG docker $USER
```
