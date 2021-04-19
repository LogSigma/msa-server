# Jenkins

### 운영환경
* CentOS 7.6
* openJDK 1.8

### git 설치
```sh
sudo yum install git
```

### jenkins.ropo 파일 설정
```sh
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
```

인터넷 연결이 안될경우 직접 파일을 설정한다.
```sh
sudo vi /etc/yum.repos.d/jenkins.repo
```
**jenkins.repo 내용**
```sh
[jenkins-stable]
name=Jenkins-stable
baseurl=https://pkg.jenkins.io/redhat-stable
gpgcheck=1
sslverify=0
repo_gqgcheck=0
gpgkey=https://pkg.jenkins.io/rehat-stable/jenkins.io.key

[jenkins]
name=Jenkins
baseurl=https://pkg.jenkins.io/redhat
gpgcheck=1
sslverify=0
repo_gqgcheck=0
gpgkey=https://pkg.jenkins.io/rehat/jenkins.io.key
```

### 설치
```sh
sudo yum install jenkins
```

### Jenkins 구동
```sh
# 시작
sudo service jenkins start
# 재시작
sudo service jenkins restart
```

Centos7 재시작 시에 항상 Jenkins를 구동하게 설정
```sh
sudo systemctl enable jenkins
```
