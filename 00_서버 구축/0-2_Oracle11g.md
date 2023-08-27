# 0-2_Oracle11g

## 0. Oracle 홈페이지 접속 및 설치 파일 다운로드

### https://www.oracle.com/database/technologies/xe-prior-release-downloads.html 접속

### Oracle Database 11gR2 Express Edition for Linux x64 Download

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/06052c5e-506b-4f1d-9f32-42e013c92fc0)


## 1. 의존 라이브러리 설치

### root 계정 접속 후

```
[root@localhost ~]# yum -y install compat-libstdc++-33.x86_64 binutils elfutils-libelf elfutils-libelf-devel
[root@localhost ~]# yum -y install glibc glibc-common glibc-devel glibc-headers gcc gcc-c++ libaio-devel
[root@localhost ~]# yum -y install libaio libgcc libstdc++ libstdc++ make sysstat unixODBC unixODBC-devel
[root@localhost ~]# yum -y install unzip
[root@localhost ~]# yum -y install compat-libstdc++-33.x86_64 binutils elfutils-libelf elfutils-libelf-devel
[root@localhost ~]# yum install binutils compat-libcap1 compat-libstdc++-33 gcc gcc-c++ glibc glibc-devel ksh libgcc libstdc++ [root@localhost ~]# libstdc++-devel libaio libaio-devel make sysstat
-> y 입력
```

## 2. Oracle 계정 생성

### 유저 생성 및 권한 설정

```
[root@localhost ~]# groupadd dba
[root@localhost ~]# useradd -g dba oracle
[root@localhost ~]# passwd oracle
[root@localhost ~]# mkdir -p /u01/app/oracle
[root@localhost ~]# chown -R oracle:dba /u01
[root@localhost ~]# chmod -R 775 /u01
```

### 환경변수 편집

```
[root@localhost ~]# su - oracle

[oracle@localhost ~]$ vi .bash_profile
export ORACLE_BASE=/u01/app/oracle
export ORACLE_HOME=$ORACLE_BASE/product/11.2.0/xe
export ORACLE_SID=XE
export PATH=$PATH:$ORACLE_HOME/bin
```

## 3. 오라클 설치 파일 업로드
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/50af2333-c6f6-49a3-a0dc-acdb6040cca8)

## 4. 오라클 설치

```
[root@localhost ~] # unzip oracle-xe-11.2.0-1.0.x86_64.rpm.zip
[root@localhost ~] # cd Disk1/
[root@localhost Disk1]# rpm -Uvh oracle-xe-11.2.0-1.0.x86_64.rpm
```

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/4f965642-56b4-4e6a-a5c9-1b35ae3b4c7c)

```
[root@localhost Disk1]# cd /etc/init.d/
[root@localhost init.d]# ./oracle-xe configure
```

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/3cae5445-ab20-4d26-8874-ee53f5a01f17)


### ORACLE_HOME과 PORT번호, SID 등 확인

```
[root@localhost init.d]# cd /u01/app/oracle/product/11.2.0/xe/network/admin/
[root@localhost admin]# vi listener.ora

[root@localhost admin]# vi tnsnames.ora
```

```
[root@localhost admin]# /etc/init.d/oracle-xe start

Starting oracle-xe (via systemctl):                        [  OK  ]
```

### 5. 방화벽 해제(필요시)

```
[root@localhost admin]# firewall-cmd --permanent --add-port=1515/tcp
success
[root@localhost admin]# firewall-cmd --reload
success
```

### 6. 오라클 접속 테스트

```
[root@localhost admin]$ su - oracle
암호:
마지막 로그인: 일  8월 27 12:57:50 KST 2023 일시 pts/0

[oracle@localhost ~]$ sqlplus "/as sysdba"

SQL*Plus: Release 11.2.0.2.0 Production on Sun Aug 27 12:59:42 2023

Copyright (c) 1982, 2011, Oracle.  All rights reserved.


Connected to:
Oracle Database 11g Express Edition Release 11.2.0.2.0 - 64bit Production
```

TEST
```
SQL> select 1 from dual;

         1
----------
         1
```

참고 https://seul96.tistory.com/419
