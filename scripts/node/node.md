# Node

**Node.js LTS (14.x)**
```sh
# As root
curl -fsSL https://rpm.nodesource.com/setup_lts.x | bash -

# No root privileges
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
```

```sh
Curl error (60): Peer certificate cannot be authenticated with given CA certificates for ...... [SSL certificate problem: unable to get local issuer certificate]
```
`yum repository` 설정 파일 (`/etc/yum.repos.d/` 디렉토리에 있는 .repo 파일)에 다음의 내용을 추가 해주면 됩니다.
```sh
sslverify=0
```

```sh
sudo yum clean all && sudo yum makecache fast

sudo yum install -y gcc-c++ make

sudo yum install -y nodejs
```
