# 0-2_Oracle11g

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
