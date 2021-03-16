# Nginx

## 1. nginx 저장소 추가
nginx 저장소 추가
```sh
vi /etc/yum.repos.d/nginx.repo
```
```sh
[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/centos/7/$basearch/
gpgcheck=0
enabled=1
```

## 2. nginx 설치
```sh
yum install -y nginx
```
Nginx를 실행시키고, 부팅시 자동으로 시작되게 변경한다.
```sh
systemctl start nginx
systemctl enable nginx
```
