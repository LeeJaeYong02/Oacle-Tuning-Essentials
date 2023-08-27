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
