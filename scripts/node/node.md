# Node

**Node.js LTS (14.x)**
```sh
# As root
curl -fsSL https://rpm.nodesource.com/setup_lts.x | bash -

# No root privileges
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
```

SSL certificate 발생 시 `yum repository` 설정 파일 (`/etc/yum.repos.d/` 디렉토리에 있는 .repo 파일)에 `sslverify=0` 내용을 추가 해주면 됩니다.

```sh
sudo yum clean all && sudo yum makecache fast

sudo yum install -y gcc-c++ make

sudo yum install -y nodejs
```

```sh
node -v
```

```sh
npm -v
```

**yarn 1.22.x**
```sh
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
```

```sh
sudo yum install yarn
```

```sh
yarn -v
```
