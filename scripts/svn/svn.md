# SVN(SubVersion)

## 1. SVN 설치
svn 설치 여부 확인 및 설치

```sh
[root@localhost ~]# svn
-bahs: svn: command not found
[root@localhost ~]# rpm -eq | grep subversion
```

```sh
yum -y install subversion
```

## 2. SVN 저장소 생성 및 설정하기

```sh
mkdir 폴더경로
cd 폴더경로
svnadmin create --fe-type fsfs 폴더경로
```

## 3. svnserve.conf 수정
svnserve.conf 파일을 svnserve.conf.old 로 변경하여 보존해두고 새로 작성한다.

```sh
cd /svn/repos/conf/
cat svnserve.conf
mv svnserve.conf svnserve.conf.old
vi svnserve.conf
```
```sh
[general]
#익명 접근의 권한은 none 없음
anon-access = none 

#인증 접근의 권한은 write 읽기/쓰기
auth-access = write

#사용자 패스워드 저장 파일 위치
password-db = passwd

#프로젝트 명칭
realm = My_First_Repository

#인증 접근의 권한 설정 파일 위치
authz-db = authz
```
