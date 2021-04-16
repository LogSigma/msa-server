# Node

**Node.js LTS (14.x)**
```sh
# As root
curl -fsSL https://rpm.nodesource.com/setup_lts.x | bash -

# No root privileges
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
```

SSL 에러 발생 시 `/etc/yum.repos.d/`에서 `sss=0` 추가할 것 


```sh
sudo yum clean all && sudo yum makecache fast

sudo yum install -y gcc-c++ make

sudo yum install -y nodejs
```
