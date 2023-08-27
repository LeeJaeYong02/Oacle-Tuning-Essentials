
## CentOS7 iso 다운로드

URL : http://mirror.anigil.com/CentOS/7.9.2009/isos/x86_64/

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/47aab3ad-dd69-44c2-bbc2-ecaf7c8883e9)

## VMware 세팅

Create a New  Virtual Machine<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/97df804c-c0d1-4ec0-8e6c-b5b86fde345b)

이미지 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/98cf80bb-4c65-4b4c-a113-90099ff3241f)

경로<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/110c6821-6e04-4544-a550-7631814e52f8)

드라이버 용량<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/6a57c3ca-287b-4898-aba3-63f02a41355d)

메모리 4gb
프로세스 4<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/f86af3d0-724b-410a-9dd8-afdd7ebd101d)

## CentOS7 Setting

언어 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/0f18e5fd-82c3-42a8-ad6f-e054290365d5)


디스크 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/bcaea6d8-10d2-440e-b620-db2e61e9ef57)

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/996f1c54-c644-4d9a-9289-b097720b5d76)

설치 시작<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/b079f740-2a94-4aec-96d1-a0fdf3694dca)

ROOT 암호 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/33c6e5ef-9cc6-40a4-8363-fc9bc313110f)

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/f7977737-ef10-491e-8836-0ceb258755e9)

ROOT 로그인<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/d51e82d0-fd5c-481e-b12e-1c1eee1a18e6)

## MobaXterm Connect

설치 : https://mobaxterm.mobatek.net/download-home-edition.html

### IP 세팅 및 확인

/etc/sysconfig/network-scripts/ 경로 이동 후 
ifcfg-***** (이더넷 랜카드 마다 다름 본인은 ifcfg-ens33)
```
[root@localhost network-scripts]# cd /etc/sysconfig/network-scripts/
[root@localhost network-scripts]# ls
ifcfg-ens33      ifdown-bnep  ifdown-ppp     ifup-TeamPort  ifup-isdn    ifup-sit
ifcfg-ens33~     ifdown-eth   ifdown-routes  ifup-aliases   ifup-plip    ifup-tunnel
ifcfg-lo         ifdown-ippp  ifdown-sit     ifup-bnep      ifup-plusb   ifup-wireless
ifdown           ifdown-ipv6  ifdown-tunnel  ifup-eth       ifup-post    init.ipv6-global
ifdown-Team      ifdown-isdn  ifup           ifup-ippp      ifup-ppp     network-functions
ifdown-TeamPort  ifdown-post  ifup-Team      ifup-ipv6      ifup-routes  network-functions-ipv6

```

설정 변경

```
[root@localhost network-scripts]# vi ifcfg-ens33

TYPE=Ethernet
PROXY_METHOD=none
BROWSER_ONLY=no
BOOTPROTO=dhcp # <- ip 자동 할당 설정
DEFROUTE=yes
IPV4_FAILURE_FATAL=no
IPV6INIT=yes
IPV6_AUTOCONF=yes
IPV6_DEFROUTE=yes
IPV6_FAILURE_FATAL=no
IPV6_ADDR_GEN_MODE=stable-privacy
NAME=ens33
UUID=dd25487e-fa6a-427b-ba89-7a17b720005e
DEVICE=ens33
ONBOOT=yes # <- 부팅 시 네트워크가 연결되도록
```

리붓

```
[root@localhost network-scripts]# reboot

·····

[root@localhost ~]# ip addr
2: ens33: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 00:0c:29:90:5c:c3 brd ff:ff:ff:ff:ff:ff
    inet 192.168.114.128/24 brd 192.168.114.255 scope global noprefixroute dynamic ens33
       valid_lft 1788sec preferred_lft 1788sec
    inet6 fe80::301f:a185:c38d:2a06/64 scope link noprefixroute
       valid_lft forever preferred_lft forever

```

세션 세팅 & 접속

할당된 ip 입력, 기본 포트는 22<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/f85e3a40-9fad-439a-bd84-116a5ff45305)


![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/5f093638-5693-4a5e-b231-78ed05b4a149)


