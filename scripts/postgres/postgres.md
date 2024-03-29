# PostgreSQL

### 운영환경
* CentOS 7.6
* PostgreSQL 11.11

### RPM 다운로드
외부 환경에서 PostgreSQL Database Server 11 PGDG 페이지에 접속해서 RPM 파일들을 다운로드 하고 리눅스 환경으로 이동시킨다.
* postgresql11-11.11-1PGDG.rhel7.x86_64.rpm
* postgresql11-contrib-11.11-1PGDG.rhel7.x86_64.rpm
* postgresql11-libs-11.11-1PGDG.rhel7.x86_64.rpm
* postgresql11-server-11.11-1PGDG.rhel7.x86_64.rpm

### 설치
postgresql11-libs -> postgresql11 -> (postgresql11-server, postgresql11-contrib) 순으로 설치한다.
```sh
sudo rpm -ivh postgresql11-libs-11.11-1PGDG.rhel7.x86_64.rpm
sudo rpm -ivh postgresql11-11.11-1PGDG.rhel7.x86_64.rpm
sudo rpm -ivh postgresql11-server-11.11-1PGDG.rhel7.x86_64.rpm
sudo rpm -ivh postgresql11-contrib-11.11-1PGDG.rhel7.x86_64.rpm
```

### 설치된 패키지 확인
```sh
rpm -qa | grep postgresql
```

### 기본 Database 생성
`initdb` 명령어를 통해 기본 데이터베이스를 설치합니다. 기본 데이터베이스는 `postgres` 라는 이름으로 생성됩니다.
```sh
sudo /usr/pgsql-11/bin/postgresql-11-setup initdb
```

### 서비스 등록 및 실행
```sh
sudo systemctl enable postgresql-11
sudo systemctl start postgresql-11
```

### postgresql 접속
```sh
sudo -u postgres psql
```

### DB 계정 추가
```sql
postgres=# create user test1;
CREATE ROLE
postgres=# \du;
```

### DB 계정 Role 권한 추가
```sql
postgres=# alter role test1 superuser createdb;
ALTER ROLE
postgres=# \du;
```

### DB 계정 Password 추가
```sql
postgres=# alter user test1 with password 'test1';
ALTER ROLE
```
